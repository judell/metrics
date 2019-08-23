# edu_classifier

    create or replace function edu_classifier(string text) returns boolean as $$
    begin
      return 
        lower(string) like '%fall%' or
        lower(string) like '%winter%' or
        lower(string) like '%spring%' or
        lower(string) like '%summer%' or
        lower(string) like '%honors%' or
        lower(string) like '%human%' or
        lower(string) like '%engl%' or
        lower(string) like '%liter%' or
        lower(string) like '%phil%' or
        lower(string) like '%anth%' or
        lower(string) like '%arch%' or
        lower(string) like '%rhet%' or
        lower(string) like '%socio%' or
        lower(string) like '%relig%' or
        lower(string) like '%femin%' or
        lower(string) like '%govern%' or
        lower(string) like '%democ%' or
        lower(string) like '%justice%' or
        lower(string) like '%culture%' or
        lower(string) like '%compos%' or
        lower(string) like '%poetry%' or
        lower(string) like '%poem%' or
        lower(string) like '%journal%' or
        lower(string) like '%story%' or
        lower(string) like '%stories%' or
        lower(string) like '%media%' or
        lower(string) like '%film%' or
        lower(string) like '%crit%' or
        lower(string) like '%reading%' or
        lower(string) like '%writing%' or
        lower(string) like '%politic%' or
        lower(string) like '%contemp%' or
        lower(string) like '%shakespeare%' or
        lower(string) like '%hist%' or
        lower(string) like '%french%' or
        lower(string) like '%spanish%' or
        lower(string) like '%italian%' or
        lower(string) like '%russian%' or
        lower(string) like '%chinese%' or
        lower(string) like '%japanese%' or
        lower(string) like '%german%' or
        lower(string) like '%latin%' or
        lower(string) like '%narrative%' or
        lower(string) like '%african%' or
        lower(string) like '%american%' or
        lower(string) like '%women%' or
        lower(string) like '%linguistics%' or
        lower(string) like '%language%' or
        lower(string) like '%science%' or
        lower(string) like '%neuro%' or
        lower(string) like '%biol%' or
        lower(string) like '%chem%' or
        lower(string) like '%physics%' or
        lower(string) like '%geology%' or
        lower(string) like '%math%' or
        lower(string) like '%computer%' or
        lower(string) like '%medical%' or
        lower(string) like '%statistic%' or
        lower(string) like '%techno%' or
        lower(string) like '%econo%' or
        lower(string) like '%research%' or
        lower(string) like '%disease%' or
        lower(string) like '%physio%' or
        lower(string) like '%astro%' or
        lower(string) like '%behavior%' or
        lower(string) like '%ecolog%' or
        lower(string) like '%mechan%' or
        lower(string) like '%engineer%' or
        lower(string) like '%climate%' or
        lower(string) like '%hydro%' or
        lower(string) like '%genetics%' 
                ;
    end;
    $$ language plpgsql;

