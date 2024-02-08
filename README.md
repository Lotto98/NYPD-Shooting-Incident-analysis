# NYPD-Shooting-Incident-analysis

Project for STATISTICAL INFERENCE AND LEARNING exam. (Master's degree)

## Description of the data
"List of every shooting incident that occurred in NYC going back to 2006 through the end of the previous calendar year.

This is a breakdown of every shooting incident that occurred in NYC going back to 2006 through the end of the previous calendar year. This data is manually extracted every quarter and reviewed by the Office of Management Analysis and Planning before being posted on the NYPD website. Each record represents a shooting incident in NYC and includes information about the event, the location and time of occurrence. In addition, information related to suspect and victim demographics is also included. This data can be used by the public to explore the nature of shooting/criminal activity. Please refer to the attached data footnotes for additional information about this dataset."

Each row is a Shooting Incident.

There are 21 columns:
1) INCIDENT_KEY: Randomly generated persistent ID for each arrest (text)
2) OCCUR_DATE: Exact date of the shooting incident (date)
3) OCCUR_TIME: Exact time of the shooting incident (time)
4) BORO: Borough where the shooting incident occurred (categorical)
5) LOC_OF_OCCUR_DESC: where the shooting incident took place: "inside", "outside" or not specified. (categorical)
6) PRECINCT: Precinct where the shooting incident occurred. (categorical)
7) JURISDICTION_CODE: Jurisdiction where the shooting incident occurred. Jurisdiction codes 0(Patrol), 1(Transit) and 2(Housing) represent NYPD whilst codes 3 and more represent non NYPD jurisdictions. (categorical)
8) LOC_CLASSFCTN_DESC: description of the classification of the location of the shooting incident: COMMERCIAL, DWELLING, HOUSING, OTHER, PARKING LOT, PLAYGROUND, STREET, TRANSIT, VEHICLE or not specified. (categorical)
9) LOCATION_DESC: Location of the shooting incident (categorical)
10) STATISTICAL_MURDER_FLAG: Shooting resulted in the victim’s death which would be counted as a murder (categorical, binary)
11) PERP_AGE_GROUP: Perpetrator’s age within a category (categorical)
12) PERP_SEX: Perpetrator’s sex description (categorical)
13) PERP_RACE: Perpetrator’s race description (categorical)
14) VIC_AGE_GROUP: Victim’s age within a category (categorical)
15) VIC_SEX: Victim's sex description (categorical)
16) VIC_RACE: Victim’s race description (categorical)
17) X_COORD_CD: Midblock X-coordinate for New York State Plane Coordinate System, Long Island Zone, NAD 83, units feet (FIPS 3104) (text)
18) Y_COORD_CD: Midblock Y-coordinate for New York State Plane Coordinate System, Long Island Zone, NAD 83, units feet (FIPS 3104) (text)
19) Latitude: Latitude coordinate for Global Coordinate System, WGS 1984, decimal degrees (EPSG 4326) (numerical)
20)Longitude: Longitude coordinate for Global Coordinate System, WGS 1984, decimal degrees (EPSG 4326) (numerical)
21) Lon_Lat: Longitude and Latitude Coordinates for mapping (point)

link to the data: https://data.cityofnewyork.us/Public-Safety/NYPD-Shooting-Incident-Data-Historic-/833y-fsy8

## Analysis description

For this dataset I would propose a binary classification task: I would like to predict the victim survival based on the available information.

Specifically, I would like to answer the following questions:

-is survival more likely in a specific neighborhood?

-is it more likely to survive based on gender/age of the victim? (obviously younger victims should be more likely to survive.)

-is it more likely to survive based on the victim's ethnicity?

-is it more likely to survive if the shooter belongs to a different/same ethnicity than the victim?

-is it more likely to survive based on sex/age/ethnicity of the perpetrator?

-Is there a trend with respect to the date on which the incident occurred?

-Is survival less likely in late hours?

-Is it more likely to survive on a weekday?

-What happened during the pandemic period?

Also, as I work through the data, I will probably try to answer additional questions as well.

## Other analysis found

I found 8 public analyses on kaggle: https://www.kaggle.com/search?q=NYPD+Shooting+Incident+Data+in%3Anotebooks

The analyses found are only descriptive. In one of them a simple linear regression on the number of deaths by year was also applied without further development. In another I found an analysis using time series.

I found another descriptive analysis where a logistic regression was applied without further elaboration:
https://github.com/korkridake/nypdshooting

I also found a paper with  another descriptive analysis (a little more elaborated):
https://infowiz.gmu.edu/server/api/core/bitstreams/2e8114a7-4c94-41e9-9322-966074c32e80/content

Therefore, my analysis will differ from these ones as I will use the statistical models that we have seen during classes.

