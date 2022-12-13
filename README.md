# super-duper-parakeet

An exercise in weather control for EVIL

## Files needed

- yaml file with location information (lat, long, name)
- yaml file for common data store (URL's to scrape, API keys/creds, etc )

### data file storage

YAML files should be stored in /etc/super-duper-parakeet/ with file names of locations.yaml and config.yaml

### urls needed

- Text only: `https://forecast.weather.gov/MapClick.php?lat={LATITUDE}&lon={LONGITUDE}&unit=0&lg=english&FcstType=text&TextType=1`

- Tabular Hourly: `https://forecast.weather.gov/MapClick.php?lat={LATITUDE}&lon={LONGITUDE}&lg=english&&FcstType=digital`

- Tabular Hourly XML: `https://forecast.weather.gov/MapClick.php?lat={LATITUDE}&lon={LONGITUDE}&FcstType=digitalDWML`

### API

## code behavior

code should read in the yaml files, and retrieve the weather data for the locations.
When proccessing a location, The first URI should retrieve the text for the next 2 time periods, and proccess the sentances within into a set of flags:

- Chance of precipitation: numeric, default 0
- showers: bool default false
- thunderstorm: bool default false
- snow: bool default false
- sleet: bool default false
- tornado: bool default false
- wind direction: enum {n,e,s,w,nne,sse, ssw, nnw, null} default null
- wind speed: numeric, default 0
- rainfall_modifier: {null, lt, gt}
- rainfall_amount: numeric, default 0
- rainfall exceptions: string, default ''

## some logical magic

## take over the world
