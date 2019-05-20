## EONET Scraper
Metadata scraper for the EONET Event Feed
----
There are 3 associated jobs:
- EONET - Scrape
- EONET - Scrape Timeframe
- EONET - Test Event

### EONET - Scrape
-----
Job is of type individual. Inputs are gejson polygon and lookback days. Geojson polygon represents the time period queried by the scraper. Lookback days represents the number of days in the past the query will construct a search over. Eg, lookback days of 3 will query from 3 days in the past until present. Lookback day input of 'redis' will use redis as a data store, and lookback will be the timestamp of the last successfully completed query.

### EONET - Scrape Timeframe
-----
Job is of type individual. The inputs are geojson polygon, starttime, and endtime. The job scrapes the EONET feed over the input timerands, over the input geojson, and publishes EONET event products to GRQ.

### EONET - Test Event
-----
Job is of type individual. This pulls the json blob in the code directory and issues a test event. There are no inputs.

Metadata product spec is the followingc:

      EONET-<product_prefix>-<event_category>-<event_source>-<event_id>-<event_datetime>-<version>

