# IWF Event Results, Athletes, anaylsis

## Data Sources

athletes:  
<https://iwf.sport/results/results-by-events/?athlete_name=&athlete_gender=all&athlete_nation=all>

events:  
Weight classes changed recently, so there are two different pages  
<https://iwf.sport/results/results-by-events/?event_type=all&event_age=all&event_nation=all>  
<https://iwf.sport/results/results-by-events/results-by-events-old-bw/?event_type=all&event_age=all&event_nation=all>

results:  
where "?event_id=" comes from events, old classes page is id < 441  
<https://iwf.sport/results/results-by-events/results-by-events-old-bw/?event_id=300>  
<https://iwf.sport/results/results-by-events/?event_id=522>

There are also a few unlisted results pages. They are ids = [1, 87, 101, 136, 169, 316, 377, 505]

## Data Info

### Athletes

**variable**|**description**|**key**
:-----:|:-----:|:-----:
athlete_id | id |
name| name |
name_alt| alternate name if more than one were used|
birthday| date of birth | YYYY-MM-DD
gender | gender | M = man, W = woman
nations | all nations athlete has compteted under | SO 3166 country code

### Results

**variable**|**description**|**key**
:-----:|:-----:|:-----:
total\_rank|rank in the total|
snatch\_rank|rank in the snatch|all NA if no medal given at event (ex: Olympics)
cleanjerk\_rank|rank in the clean and jerk|all NA if no medal given at event
name|athlete name|
athlete\_id|athlete id|key to athletes data
birthday|date of birth| YYYY-MM-DD
gender|gender|M = Man, W = Woman
nation|country they are competing for|ISO 3166 country code
group|group session|A=final=best
bw|body weight|in KG
category|weight class/category| + = lower limit
dq|was disqualified|0 = no, 1 = yes
old\_classes|is category from the old weight classes|0 = no, 1 = yes
event\_id|event id|key to events data
snatch\_lift1|absolute value is 1st snatch attempt|negative = miss
snatch\_lift2|2nd snatch attempt|negative = miss
snatch\_lift3|3rd snatch attempt|negative = miss
snatch\_best|best snatch out of three attempts|
cleanjerk\_lift1|1st clean and jerk attempt|negative = miss
cleanjerk\_lift2|2nd clean and jerk attempt|negative = miss
cleanjerk\_lift3|3rd clean and jerk attempt|negative = miss
cleanjerk\_best|best clean and jerk out of three attempts|
total|sum of best snatch and best clean and jerk|

### Events

**variable**|**description**|**key**
:-----:|:-----:|:-----:
event_id | id |
event | event name |
date | date of event | YYYY-MM-DD
location | all nations athlete has compteted under | city, ISO 3166 country code
