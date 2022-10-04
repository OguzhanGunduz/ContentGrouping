# ContentGrouping
Content Grouping for some sites, Destination &amp; SQL



Page path - Query Exclude


```SQL

REGEXP_REPLACE(Page path,'\\?.*','')

```
-------------------------

```SQL

CASE
WHEN REGEXP_MATCH(Page path - Query Exclude, '^/$|^/en$|^/es$|^/de$|^/ae$|^/ru$|^/ua$') THEN 'Homepage' 
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/cost-optimization/.*|.*/monetization/.*|.*/telco-cloud/.*|.*/from-traditional-to-digital-business-support-systems/.*|.*/revenue-growth/.*') THEN 'Solutions'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/telenity-digital-services-platform/.*|.*/campaign-management/.*|.*/telenity-direct-carrier-billing/.*|.*/partner-management/.*|.*/telenity-service-subscription-manager/.*') THEN 'Digital Services'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/telenity-vas-consolidation-platform/.*|.*/telenity-bulk-messaging-suite/.*|.*/telenity-call-completion-suite/.*|.*/telenity-ipsm-gateway/.*|.*/telenity-mmsc/.*|.*/telenity-ring-back-tone/.*|.*/sms-anti-spam/.*|.*/telenity-smsc/.*|.*/telenity-ussd-service-center/.*|.*/telenity-ussi-gateway/.*') THEN 'VAS Consolidation'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/rcs-business-messaging/.*') THEN 'Rich Communication Suite'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/managed-services/.*') THEN 'Managed Services'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/enkudo/.*') THEN 'Enkudo'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/tracking/.*') THEN 'Tracking'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/open-positions.*') THEN 'Open Positions'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/ooreedo-qatar/.*|.*/azercell/.*|.*/smartfren/.*|.*/vodafone-turkey/.*') THEN 'Case Studies'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/blog/.*|.*/cost-optimization-in-the-telecom/.*|.*/how-to-increase-your-revenue-with-direct-carrier-billing/.*|.*/revenue-sharing-business-model-guide/.*|.*/metaverse-and-telecommunications/.*|.*/how-to-increase-your-revenue-with-direct-carrier-billing/.*|.*/supply-chain-planning/.*|.*/direct-carrier-billing-operator-based-billing-solution-for-digital-merchants/.*|.*/network-function-virtualization/.*') THEN 'Resources - Blogs'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/careers/.*|.*/application-process/.*|.*/corporate-social-responsibility/.*|.*/internship-opportunities/.*|.*/telenity-today/.*|.*/why-join-telenity/.*|.*/your-career-at-telenity/.*') THEN 'Career'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/about/.*|.*/board-of-directors/.*|.*/management/.*|.*/customers/.*|.*/contact/.*|.*/support/.*') THEN 'About'
WHEN REGEXP_MATCH(Page path - Query Exclude, '.*/category/press-releases/.*|.*/category/latest-news/.*') THEN 'News' ELSE 'Others'

END
```
```SQL
SELECT * FROM film 
WHERE  replacement_cost BETWEEN 12.99 AND 16.99;
```
