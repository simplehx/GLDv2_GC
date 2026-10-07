# GLDv2_GC
Geographic coordinates corresponding to the Google Landmarks Dataset v2


## Data Details
* Data collection time: October 7, 2026
* GLDv2_CG contains geographic coordinate data for 182,824 landmarks, accounting for 182,824/203,094 ≈ 90.01% of the original data.

## Data Collection API
| Endpoint | Method | Purpose |
|---|---|---|
| Wikimedia Commons: `https://commons.wikimedia.org/w/api.php` | `action=query`, `prop=pageprops` | Given an input Category page, retrieves its `wikibase_item` (Wikidata QID). |
| Wikidata: `https://www.wikidata.org/w/api.php` | `action=wbgetentities`, `props=claims` | Retrieves entity claims in batches, identifies the corresponding topic via **P301**, and then reads the latitude and longitude from **P625** of either the topic entity or the original entity. |


## GLDv2_CG Data Sample

| landmark_id | category | wikidata_id | latitude | longitude |
|---:|---|---|---:|---:|
| 0 | http://commons.wikimedia.org/wiki/Category:Happy_Valley_Racecourse | Q837662 | 22.2728 | 114.182 |
| 2 | http://commons.wikimedia.org/wiki/Category:Grand_Ventron | Q3114629 | 47.959444444444 | 6.9255555555556 |
| 3 | http://commons.wikimedia.org/wiki/Category:Tweed_Heads,_New_South_Wales | Q606344 | -28.1833 | 153.55 |
| 4 | http://commons.wikimedia.org/wiki/Category:Santa_Maria_Immacolata_della_Concezione_(Rome) | Q3355127 | 41.895916666667 | 12.5005 |
| 5 | http://commons.wikimedia.org/wiki/Category:Lakeside_International_Raceway | Q2973998 | -27.2281 | 152.965 |
| 6 | http://commons.wikimedia.org/wiki/Category:Firehouse_Center_and_Gallery | Q5123214 | 30.9064 | -84.577 |
| 7 | http://commons.wikimedia.org/wiki/Category:Sparkassen-Arena,_G%C3%B6ttingen | Q19309291 | 51.542186 | 9.921973 |
| 8 | http://commons.wikimedia.org/wiki/Category:White_Monuments_of_Vladimir_and_Suzdal | Q838264 | 56.15 | 40.4167 |


## Related links
* Google Landmarks Dataset v2: https://github.com/cvdfoundation/google-landmark
* train_label_to_category.csv: https://s3.amazonaws.com/google-landmark/metadata/train_label_to_category.csv