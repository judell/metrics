# queries

with group_user_counts as (

  with raw_counts as (

  select count(*) as user_count, group_id  from user_group 
  group by group_id 
  order by user_count desc 
  )

  select raw_counts.user_count, "group".pubid, "group".name, "group".description from raw_counts  
  inner join "group" on raw_counts.group_id = "group".id 
  where 

    edu_classifier("group".name) = 't'
    and raw_counts.user_count > 10 
    and raw_counts.user_count < 100)
  
  )

select count(*), lower(substring("user".email from '(\.+[^\.]+$)')) = '.edu' as is_edu, (count(*) / sum(count(*)) over ()) as "% of total"
from group_user_counts
inner join annotation 
on group_user_counts.pubid = annotation.groupid 
inner join "user"
on replace( replace(annotation.userid, 'acct:', ''), '@hypothes.is','')  = "user".username 
group by is_edu  
order by count(*) desc 
 

# functions

