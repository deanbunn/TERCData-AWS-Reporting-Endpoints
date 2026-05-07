## TERCData AWS Reporting Endpoints

The non-QuickSight endpoints require the user to submit at least "id" and "rptdate". "rptend" (optional and used for a range of dates). 

The times are filtered so only the 0, 20, and 40 minute values of the hour are returned. 

For the State of the Lake API, "id" is the year of the report and "rptend" (optional and used for a range of years).


## Reporting Endpoints
- [State of the Lake](#state-of-the-lake)
- [Met USCG 2020](#met-uscg-2020)
- [USGS](#usgs)
- [Near Shore](#near-shore)
- [Met](#met)
- [NASA](#nasa)
- [Met Weatherlink](#met-weatherlink)
- [Clear Lake Creeks](#clear-lake-creeks)
- [TC Homewood](#tc-homewood)
- [QuickSight Near Shore](#quicksight-near-shore)
- [QuickSight NASA](#quicksight-nasa)
- [QuickSight Met Stations](#quicksight-met-stations)



### State of the Lake
URL: https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/state-of-lake?id=2020

```bash
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/state-of-lake?id=2020'
```
```json
[
  {
    "Year": "2020",
    "Max_Air_Temp_Ave": "58.2396694214876",
    "Min_Air_Temp_Ave": "32.4159779614325",
    "Annual_Precipitation": "20.12",
    "Annual_Snow": "9.07",
    "Snow_Propotion": "45.08",
    "Monthly_Max_Air_Temp_Jan": "40.5483870967742",
    "Monthly_Max_Air_Temp_Feb": "44.6923076923077",
    "Monthly_Max_Air_Temp_Mar": "41.0967741935484",
    "Monthly_Max_Air_Temp_Apr": "51.7666666666667",
    "Monthly_Max_Air_Temp_May": "60.9354838709677",
    "Monthly_Max_Air_Temp_Jun": "68.6333333333333",
    "Monthly_Max_Air_Temp_July": "79.0645161290323",
    "Monthly_Max_Air_Temp_Aug": "80.4193548387097",
    "Monthly_Max_Air_Temp_Sep": "73.8",
    "Monthly_Max_Air_Temp_Oct": "65.7741935483871",
    "Monthly_Max_Air_Temp_Nov": "47.5666666666667",
    "Monthly_Max_Air_Temp_Dec": "42.6774193548387",
    "Monthly_Min_Air_Temp_Jan": "22.8064516129032",
    "Monthly_Min_Air_Temp_Feb": "21.7307692307692",
    "Monthly_Min_Air_Temp_Mar": "23.0967741935484",
    "Monthly_Min_Air_Temp_Apr": "29.0666666666667",
    "Monthly_Min_Air_Temp_May": "35.0",
    "Monthly_Min_Air_Temp_Jun": "40.0666666666667",
    "Monthly_Min_Air_Temp_July": "45.5483870967742",
    "Monthly_Min_Air_Temp_Aug": "48.5161290322581",
    "Monthly_Min_Air_Temp_Sep": "42.7333333333333",
    "Monthly_Min_Air_Temp_Oct": "34.2903225806452",
    "Monthly_Min_Air_Temp_Nov": "23.7333333333333",
    "Monthly_Min_Air_Temp_Dec": "20.8709677419355",
    "Monthly_Precipitation_Jan": "2.22",
    "Monthly_Precipitation_Feb": "0.12",
    "Monthly_Precipitation_Mar": "4.73",
    "Monthly_Precipitation_Apr": "1.76",
    "Monthly_Precipitation_May": "1.3",
    "Monthly_Precipitation_Jun": "0.21",
    "Monthly_Precipitation_July": "0.0",
    "Monthly_Precipitation_Aug": "0.28",
    "Monthly_Precipitation_Sep": "0.01",
    "Monthly_Precipitation_Oct": "0.0",
    "Monthly_Precipitation_Nov": "2.89",
    "Monthly_Precipitation_Dec": "2.24",
    "Surface_Water_Temp_Ave": "52.84116761",
    "Secchi_Annual_Ave": "62.992125984252",
    "Secchi_Winter_Ave": "63.9763779527559",
    "Secchi_Summer_Ave": "59.0551181102362",
    "Chla_Ave": "0.7815"
  }
]
```

### Met USCG 2020
URL: https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/met-uscg2020?id=1&rptdate=20260501

ID Numbers:
- 1 = USCG2020

```bash
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/met-uscg2020?id=1&rptdate=20260501&rptend=20260504'
```
```json
[
  {
    "ID": "1",
    "Station_Name": "USCG2020",
    "TmStamp": "2026-05-04 23:40:00",
    "Batt_V": "13.93",
    "LoggerTemp_C": "6.733",
    "AirTemp_C": "5.497",
    "RH_percent": "87.5",
    "WindSpd_ms": "3.369",
    "WindDir_deg": "246.6",
    "WindSpdMax_ms": "5.5",
    "Precip_mm": "0.6",
    "WaterTemp_C": "9.763958",
    "BP_mbar": "805.392",
    "ShortWaveIn_wm2": "8.71",
    "ShortWaveOut_wm2": "3.505",
    "LongWaveInRaw_wm2": "-0.528",
    "LongWaveOutRaw_wm2": "13.88",
    "LongWaveInCorr_wm2": "338.6",
    "LongWaveOutCorr_wm2": "353.0",
    "NR01TC_Avg": "4.95",
    "NR01TK_Avg": "278.1",
    "NetRs_Avg": "5.205",
    "NetRl_Avg": "-14.41",
    "Albedo_Avg": "0.407",
    "UpTot_Avg": "8.18",
    "DnTot_Avg": "17.38",
    "NetTot_Avg": "-9.2"
  },
  {
    "ID": "1",
    "Station_Name": "USCG2020",
    "TmStamp": "2026-05-04 23:20:00",
    "Batt_V": "13.96",
    "LoggerTemp_C": "6.87",
    "AirTemp_C": "5.348",
    "RH_percent": "88.2",
    "WindSpd_ms": "3.07",
    "WindDir_deg": "270.0",
    "WindSpdMax_ms": "4.75",
    "Precip_mm": "0.1",
    "WaterTemp_C": "9.775947",
    "BP_mbar": "805.3583",
    "ShortWaveIn_wm2": "28.81",
    "ShortWaveOut_wm2": "4.47",
    "LongWaveInRaw_wm2": "-0.383",
    "LongWaveOutRaw_wm2": "14.1",
    "LongWaveInCorr_wm2": "338.0",
    "LongWaveOutCorr_wm2": "352.4",
    "NR01TC_Avg": "4.784",
    "NR01TK_Avg": "277.9",
    "NetRs_Avg": "24.34",
    "NetRl_Avg": "-14.48",
    "Albedo_Avg": "0.192",
    "UpTot_Avg": "28.42",
    "DnTot_Avg": "18.57",
    "NetTot_Avg": "9.86"
  }
]
```

### USGS
URL: https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/usgs-ws?id=103366092&rptdate=20260501&rptend=20260504

ID Numbers:  
- 103366092 = Upper Truckee River near Meyers
- 10336610 = Upper Truckee River at South Lake Tahoe
- 10336645 = General Creek
- 10336660 = Blackwood Creek
- 10336674 = Ward Creek near Tahoe City
- 10336676 = Ward Creek near Tahoe Pines
- 10336698 = Third Creek
- 10336700 = Incline Creek
- 10336730 = Glenbrook Creek
- 10336780 = Trout Creek
- 10337500 = Truckee River at Tahoe City
- 10337000 = Lake Tahoe Water Level

```bash
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/usgs-ws?id=103366092&rptdate=20260501&rptend=20260504'
```
```json
[
  {
    "ID": "103366092",
    "Location": "Upper Truckee River near Meyers",
    "TmStamp": "2026-05-01 00:00:00",
    "Latitude": "38.848",
    "Longitude": "-120.028",
    "Lake_Level": "None",
    "Streamflow": "108.0"
  },
  {
    "ID": "103366092",
    "Location": "Upper Truckee River near Meyers",
    "TmStamp": "2026-05-02 00:00:00",
    "Latitude": "38.848",
    "Longitude": "-120.028",
    "Lake_Level": "None",
    "Streamflow": "126.0"
  },
  {
    "ID": "103366092",
    "Location": "Upper Truckee River near Meyers",
    "TmStamp": "2026-05-03 00:00:00",
    "Latitude": "38.848",
    "Longitude": "-120.028",
    "Lake_Level": "None",
    "Streamflow": "144.0"
  },
  {
    "ID": "103366092",
    "Location": "Upper Truckee River near Meyers",
    "TmStamp": "2026-05-04 00:00:00",
    "Latitude": "38.848",
    "Longitude": "-120.028",
    "Lake_Level": "None",
    "Streamflow": "148.0"
  }
]
```

### Near Shore
URL: https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/ns-station-range?id=2&rptdate=20260501&rptend=20260504

ID Numbers:
- 1 = Cascade
- 2 = Dollar Point
- 3 = Glenbrook
- 4 = Homewood
- 5 = Meeks
- 6 = Rubicon
- 7 = Sand Harbor
- 8 = Tahoe Vista
- 9 = Tahoe City
- 10 = Camp Richardson
- 11 = Timber Cove
- 12 = Cedar Point

```bash
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/ns-station-range?id=2&rptdate=20260501&rptend=20260504'
```
```json
[
  {
    "ID": "2",
    "Station_Name": "Dollar Point",
    "TmStamp": "2026-05-01 00:00:00",
    "LS_Chlorophyll_Avg": "42.78786",
    "LS_Temp_Avg": "9.526819",
    "LS_Turbidity_Avg": "13.08994",
    "WaveHeight": "0.003069878",
    "Conductivity25C_Avg": "0.1077411",
    "LS_DO_Avg": "57.33315"
  },
  {
    "ID": "2",
    "Station_Name": "Dollar Point",
    "TmStamp": "2026-05-01 00:20:00",
    "LS_Chlorophyll_Avg": "41.85686",
    "LS_Temp_Avg": "9.44304",
    "LS_Turbidity_Avg": "13.15956",
    "WaveHeight": "0.003813744",
    "Conductivity25C_Avg": "0.1096699",
    "LS_DO_Avg": "55.95044"
  },
  {
    "ID": "2",
    "Station_Name": "Dollar Point",
    "TmStamp": "2026-05-01 00:40:00",
    "LS_Chlorophyll_Avg": "41.7959",
    "LS_Temp_Avg": "9.624419",
    "LS_Turbidity_Avg": "13.02172",
    "WaveHeight": "0.003863335",
    "Conductivity25C_Avg": "0.1100411",
    "LS_DO_Avg": "55.47226"
  }
]
```

### Met
URL: https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/met?id=1&rptdate=20260501&rptend=20260504

ID Numbers:
- 1 = Cave Rock
- 2 = Rubicon
- 3 = Sunnyside
- 4 = Timber Cove
- 5 = Tahoe Vista
- 6 = TDR1 (Buoy)
- 7 = TDR2 (Buoy)
- 8 = US Coast Guard Pier

```bash
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/met?id=1&rptdate=20260501&rptend=20260504'
```
```json
[
  {
    "ID": "1",
    "Station_Name": "Cave Rock",
    "TmStamp": "2026-05-01 00:00:00",
    "Wind_Spd1": "1.792",
    "Wind_Spd2": "None",
    "Wind_Dir": "332.4",
    "Air_Temp": "14.04"
  },
  {
    "ID": "1",
    "Station_Name": "Cave Rock",
    "TmStamp": "2026-05-01 00:20:00",
    "Wind_Spd1": "1.789",
    "Wind_Spd2": "None",
    "Wind_Dir": "337.0",
    "Air_Temp": "14.46"
  },
  {
    "ID": "1",
    "Station_Name": "Cave Rock",
    "TmStamp": "2026-05-01 00:40:00",
    "Wind_Spd1": "1.284",
    "Wind_Spd2": "None",
    "Wind_Dir": "335.4",
    "Air_Temp": "14.1"
  }
]
```

### NASA
URL: https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/nasa-tb?id=4&rptdate=20260501&rptend=20260504

ID Numbers:
- 1 = tb1
- 2 = tb2
- 3 = tb3
- 4 = tb4

```bash
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/nasa-tb?id=4&rptdate=20260501&rptend=20260504'
```
```json
[
  {
    "ID": "4",
    "Station_Name": "tb4",
    "TmStamp": "2026-05-01 00:00:00",
    "RBR_0p5_m": "11.48",
    "WindSpeed_1": "1.8",
    "AirTemp_1": "13.9",
    "WindDir_1": "266.4",
    "WindSpeed_2": "2.3",
    "AirTemp_2": "13.6",
    "WindDir_2": "243.5"
  },
  {
    "ID": "4",
    "Station_Name": "tb4",
    "TmStamp": "2026-05-01 00:20:00",
    "RBR_0p5_m": "11.72",
    "WindSpeed_1": "1.9",
    "AirTemp_1": "14.1",
    "WindDir_1": "290.4",
    "WindSpeed_2": "2.3",
    "AirTemp_2": "14.0",
    "WindDir_2": "267.2"
  },
  {
    "ID": "4",
    "Station_Name": "tb4",
    "TmStamp": "2026-05-01 00:40:00",
    "RBR_0p5_m": "11.54",
    "WindSpeed_1": "1.0",
    "AirTemp_1": "14.8",
    "WindDir_1": "310.3",
    "WindSpeed_2": "1.6",
    "AirTemp_2": "14.2",
    "WindDir_2": "285.3"
  }
]
```

### Met Weatherlink
URL: https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/metweatherlink?id=8&rptdate=20260501&rptend=20260504 

ID Numbers:
- 1 = Buckingham Point
- 2 = Clearlake Oaks 
- 4 = Konocti Bay
- 5 = Nice
- 6 = North Lakeport
- 7 = Big Valley Rancheria
- 8 = Beakbane Island

```bash
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/metweatherlink?id=8&rptdate=20260501&rptend=20260504'
```
```json
[
  {
    "Station_ID": "Beakbane Island",
    "DateTime_UTC": "2026-05-04 23:45:00",
    "Air_Temp": "14.0",
    "Hi_Air_Temp": "14.1",
    "Low_Air_Temp": "13.9",
    "Rel_Humidity": "79.0",
    "Dew_Point": "10.4",
    "Wind_Speed": "5.0",
    "Wind_Dir": "W",
    "Hi_Wind_Speed": "11.0",
    "Hi_Wind_Speed_Dir": "W",
    "Atm_Pres": "29.957",
    "Rain": "0.0",
    "Rain_Rate": "0.0",
    "Solar_Rad": "83.0",
    "Solar_Energy": "1.78"
  },
  {
    "Station_ID": "Beakbane Island",
    "DateTime_UTC": "2026-05-04 23:30:00",
    "Air_Temp": "14.1",
    "Hi_Air_Temp": "14.1",
    "Low_Air_Temp": "13.9",
    "Rel_Humidity": "78.0",
    "Dew_Point": "10.3",
    "Wind_Speed": "8.0",
    "Wind_Dir": "W",
    "Hi_Wind_Speed": "11.0",
    "Hi_Wind_Speed_Dir": "W",
    "Atm_Pres": "29.964",
    "Rain": "0.0",
    "Rain_Rate": "0.0",
    "Solar_Rad": "76.0",
    "Solar_Energy": "1.63"
  },
  {
    "Station_ID": "Beakbane Island",
    "DateTime_UTC": "2026-05-04 23:15:00",
    "Air_Temp": "13.9",
    "Hi_Air_Temp": "14.0",
    "Low_Air_Temp": "13.8",
    "Rel_Humidity": "79.0",
    "Dew_Point": "10.3",
    "Wind_Speed": "7.0",
    "Wind_Dir": "W",
    "Hi_Wind_Speed": "11.0",
    "Hi_Wind_Speed_Dir": "W",
    "Atm_Pres": "29.959",
    "Rain": "0.0",
    "Rain_Rate": "0.0",
    "Solar_Rad": "73.0",
    "Solar_Energy": "1.57"
  }
]
```

### Clear Lake Creeks
URL: https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/cl-creeks?id=1&rptdate=20260501&rptend=20260504 

ID Numbers:
- 1 = Kelsey
- 2 = Middle
- 3 = Scotts

```bash
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/cl-creeks?id=1&rptdate=20260501&rptend=20260504'
```
```json
[
  {
    "RecNum": "25098",
    "Creek": "Kelsey",
    "Turb_BES": "0.63",
    "Turb_Var": "0.011",
    "Turb_Min": "0.35",
    "TmStamp": "2019-06-12 23:50:00",
    "Turb_Temp": "24.8",
    "Turb_Max": "0.83",
    "Turb_Mean": "0.63",
    "Turb_Median": "0.63"
  }
]
```

### TC Homewood
URL: https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/tc-homewood?rptdate=20260501&rptend=20260504

```bash
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/tc-homewood?rptdate=20260501&rptend=20260504'
```
```json
[
  {
    "TmStamp": "2022-06-27 00:00:00", 
    "LS_RawPressure_Avg": "130.2856", 
    "LS_DO_Avg": "71.22476", 
    "LS_T1_Avg": "11.27003", 
    "LS_T2_Avg": "10.4212", 
    "LS_T3_Avg": "9.682767", 
    "LS_T4_Avg": "8.6129", 
    "LS_T5_Avg": "7.871133", 
    "LS_T6_Avg": "7.254966", 
    "LS_T7_Avg": "7.010283", 
    "LS_T8_Avg": "6.61455", 
    "LS_T9_Avg": "6.299917", 
    "LS_T10_Avg": "6.1826", 
    "LS_T11_Avg": "6.047166", 
    "LS_T12_Avg": "5.99755", 
    "LS_T13_Avg": "5.966233", 
    "LS_T14_Avg": "5.869967", 
    "LS_T15_Avg": "5.750333", 
    "LS_T16_Avg": "5.66885", 
    "O2_uM_corr_T16_Avg": "78.35", 
    "Pct_Sat_T1_Avg": "0.284", 
    "O2_uM_cal_T1_Avg": "97.0", 
    "LakeSensor_BattV_Min": "12.57", 
    "BP_mmHg": "612.8552", 
    "Depth_m4C_Avg": "124.5109"
   }
]
```

## TERC QuickSight Report

These endpoints display entries that were recorded in the last 30 days. 

### QuickSight Near Shore
URLs:
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-camprichardson
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-dollarpoint
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-glenbrook
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-homewood
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-rubicon
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-sandharbor
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-tahoecity
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-tahoevista
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-timbercove



```bash
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-camprichardson'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-dollarpoint'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-glenbrook'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-homewood'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-rubicon'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-sandharbor'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-tahoecity'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-tahoevista'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-ns-timbercove'
```
```json
[
  {
    "TmStamp": "2026-05-06 21:00:30",
    "LS_Temp_Avg": "10.97926",
    "Depth_m4C_Avg": "2.491468",
    "WaveHeight": "0.009767532",
    "Conductivity25C_Avg": "0.1054884",
    "LS_DO_Avg": "59.38074",
    "LS_Turbidity_Avg": "6.49562",
    "LS_Chlorophyll_Avg": "40.67024",
    "LS_CDOM_Avg": "0.0",
    "LS_Conductivity_Avg": "0.07194",
    "LS_DO_Conc_Avg": "None"
  },
  {
    "TmStamp": "2026-05-06 22:00:30",
    "LS_Temp_Avg": "11.18694",
    "Depth_m4C_Avg": "2.491777",
    "WaveHeight": "0.006563187",
    "Conductivity25C_Avg": "0.1058833",
    "LS_DO_Avg": "59.20036",
    "LS_Turbidity_Avg": "6.505759",
    "LS_Chlorophyll_Avg": "40.53908",
    "LS_CDOM_Avg": "0.0",
    "LS_Conductivity_Avg": "0.07262",
    "LS_DO_Conc_Avg": "None"
  },
  {
    "TmStamp": "2026-05-06 23:00:30",
    "LS_Temp_Avg": "11.06048",
    "Depth_m4C_Avg": "2.494557",
    "WaveHeight": "0.008675575",
    "Conductivity25C_Avg": "0.107332",
    "LS_DO_Avg": "58.81744",
    "LS_Turbidity_Avg": "6.491779",
    "LS_Chlorophyll_Avg": "40.64984",
    "LS_CDOM_Avg": "0.0",
    "LS_Conductivity_Avg": "0.07336",
    "LS_DO_Conc_Avg": "None"
  }
]
```

### QuickSight NASA
URLs:
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/nasa-tb1
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/nasa-tb2
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/nasa-tb3
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/nasa-tb4

```bash
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/nasa-tb1'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/nasa-tb2'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/nasa-tb3'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/nasa-tb4'
```
```json
[
 {
    "ID": "1",
    "Station_Name": "tb1",
    "TmStamp": "2026-05-06 21:00:00",
    "RBR_0p5_m": "11.17",
    "WindSpeed_1": "1.1",
    "AirTemp_1": "12.9",
    "WindDir_1": "141.2",
    "WindSpeed_2": "0.7",
    "AirTemp_2": "12.2",
    "WindDir_2": "156.4"
  },
  {
    "ID": "1",
    "Station_Name": "tb1",
    "TmStamp": "2026-05-06 21:20:00",
    "RBR_0p5_m": "11.08",
    "WindSpeed_1": "2.5",
    "AirTemp_1": "12.8",
    "WindDir_1": "190.7",
    "WindSpeed_2": "1.7",
    "AirTemp_2": "12.7",
    "WindDir_2": "198.7"
  },
  {
    "ID": "1",
    "Station_Name": "tb1",
    "TmStamp": "2026-05-06 21:40:00",
    "RBR_0p5_m": "10.8",
    "WindSpeed_1": "2.3",
    "AirTemp_1": "13.5",
    "WindDir_1": "208.6",
    "WindSpeed_2": "1.9",
    "AirTemp_2": "13.1",
    "WindDir_2": "219.4"
  }
]
```

### QuickSight Met Stations
URLs:
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-caverock
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-rubicon
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-sunnyside
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-tahoevista
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-tdr1buoy
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-tdr2buoy
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-timbercove
- https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-uscg

```bash
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-caverock'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-rubicon'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-sunnyside'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-tahoevista'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-tdr1buoy'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-tdr2buoy'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-timbercove'
curl 'https://tepfsail50.execute-api.us-west-2.amazonaws.com/v1/report/qs-met-uscg'
```
```json
[
  {
    "ID": "1",
    "Station_Name": "Cave Rock",
    "TmStamp": "2026-05-06 22:00:00",
    "Wind_Spd1": "1.173",
    "Wind_Spd2": "None",
    "Wind_Dir": "233.6",
    "Air_Temp": "16.15"
  },
  {
    "ID": "1",
    "Station_Name": "Cave Rock",
    "TmStamp": "2026-05-06 22:20:00",
    "Wind_Spd1": "0.699",
    "Wind_Spd2": "None",
    "Wind_Dir": "230.7",
    "Air_Temp": "16.96"
  },
  {
    "ID": "1",
    "Station_Name": "Cave Rock",
    "TmStamp": "2026-05-06 22:40:00",
    "Wind_Spd1": "0.636",
    "Wind_Spd2": "None",
    "Wind_Dir": "254.3",
    "Air_Temp": "18.76"
  }
]
```