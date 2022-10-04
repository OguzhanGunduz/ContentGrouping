# ContentGrouping
Content Grouping for some sites, Destination &amp; SQL



Page path - Query Exclude

```SQL

REGEXP_REPLACE(Page path,'\\?.*','')

```
-------------------------


Content Grouping
```SQL

CASE
WHEN REGEXP_MATCH(Page path - Query Exclude, '^/$|^/en$|^/es$|^/de$|^/ae$|^/ru$|^/ua$') THEN 'Homepage' 
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*.*|.*.*|.*.*|.*.*|.*/revenue-growth/.*') THEN 'Solutions'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/rcs-business-messaging/.*') THEN 'Rich Communication Suite'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/managed-services/.*') THEN 'Managed Services'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/category/press-releases/.*|.*/category/latest-news/.*') THEN 'News' ELSE 'Others'

END
```

