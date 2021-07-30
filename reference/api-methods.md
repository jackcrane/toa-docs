---
layout: default
title: API Methods & Background
parent: API Reference
nav_order: 1
---


# API Methods & Background
{: .no_toc}

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Event Types

Returns all the event types provided by or supported by TOA.

GET
{: .label .label-green .m-1 }


### Endpoint
{: .mt-1 }

```
https://theorangealliance.org/api/event-types
```

<!-- ### Queries

| Key | Description | Examples |
| --- | --- | --- |
| league_key | **TODO** | `0506-IA-MAND`, `1920-IA-BATU` [How to list leagues](/reference/api-methods.html#leagues) |
| region_key | State / region the event takes palce | `OH`, `CA`, `AB` |
| season_key | Season the event takes place | `2021` | -->

### Response

This is the API response on 7/30/2021. This particular response is not expected to change.

```json
[
    {
        "event_type_key": "LGCMP",
        "description": "League Championship"
    },
    {
        "event_type_key": "LGMEET",
        "description": "League/Meet"
    },
    {
        "event_type_key": "OFFSSN",
        "description": "Off Season"
    },
    {
        "event_type_key": "OTHER",
        "description": "Other"
    },
    {
        "event_type_key": "QUAL",
        "description": "Qualifier"
    },
    {
        "event_type_key": "RCMP",
        "description": "Region Championship"
    },
    {
        "event_type_key": "SCRIMMAGE",
        "description": "Scrimmage"
    },
    {
        "event_type_key": "SPRING",
        "description": "Spring Event"
    },
    {
        "event_type_key": "SPRQUAL",
        "description": "Super Qualifier"
    },
    {
        "event_type_key": "SPRRGNL",
        "description": "Super Regional"
    },
    {
        "event_type_key": "WRLDCMP",
        "description": "World Championship"
    }
]
```

### Examples

#### cURL
```
curl --location --request GET 'https://theorangealliance.org/api/event-types' \
--header 'X-TOA-Key: :your-toa-key' \
--header 'X-Application-Origin: FTC Explorer app'
```

#### JavaScript

```javascript
var axios = require('axios');

var config = {
  method: 'get',
  url: 'https://theorangealliance.org/api/event-types',
  headers: { 
    'X-TOA-Key': ':your-toa-key', 
    'X-Application-Origin': 'FTC Explorer app'
  }
};

axios(config)
  .then(function (response) {
    console.log(JSON.stringify(response.data));
  })
  .catch(function (error) {
    console.log(error);
  });
```


---

## Seasons

Returns all the seasons supported by TOA.

GET
{: .label .label-green .m-1 }


### Endpoint
{: .mt-1 }

```
https://theorangealliance.org/api/seasons
```

### Response

This is the API response on 7/30/2021. This particular response is only expected to change once a year.

```json
[
    {
        "season_key": "0506",
        "description": "Half-Pipe Hustle",
        "is_active": false
    },
    {
        "season_key": "0607",
        "description": "Hangin-A-Round",
        "is_active": false
    },
    {
        "season_key": "0708",
        "description": "Quad Quandary",
        "is_active": false
    },
    {
        "season_key": "0809",
        "description": "Face Off",
        "is_active": false
    },
    {
        "season_key": "0910",
        "description": "Hot Shot!",
        "is_active": false
    },
    {
        "season_key": "1011",
        "description": "Get Over It!",
        "is_active": false
    },
    {
        "season_key": "1112",
        "description": "Bowled Over!",
        "is_active": false
    },
    {
        "season_key": "1213",
        "description": "Ring It Up!",
        "is_active": false
    },
    {
        "season_key": "1314",
        "description": "Block Party!",
        "is_active": false
    },
    {
        "season_key": "1415",
        "description": "Cascade Effect",
        "is_active": false
    },
    {
        "season_key": "1516",
        "description": "FIRST RES-Q",
        "is_active": false
    },
    {
        "season_key": "1617",
        "description": "Velocity Vortex",
        "is_active": false
    },
    {
        "season_key": "1718",
        "description": "Relic Recovery",
        "is_active": true
    },
    {
        "season_key": "1819",
        "description": "Rover Ruckus",
        "is_active": true
    },
    {
        "season_key": "1920",
        "description": "SKYSTONE",
        "is_active": true
    },
    {
        "season_key": "2021",
        "description": "Ultimate Goal",
        "is_active": true
    }
]
```

### Examples

#### cURL
```
curl --location --request GET 'https://theorangealliance.org/api/seasons' \
--header 'X-TOA-Key: :your-toa-key' \
--header 'X-Application-Origin: FTC Explorer app'
```

#### JavaScript

```javascript
var axios = require('axios');

var config = {
  method: 'get',
  url: 'https://theorangealliance.org/api/seasons',
  headers: { 
    'X-TOA-Key': ':your-toa-key', 
    'X-Application-Origin': 'FTC Explorer app'
  }
};

axios(config)
  .then(function (response) {
    console.log(JSON.stringify(response.data));
  })
  .catch(function (error) {
    console.log(error);
  });
```

---

## Regions

Returns all the regions supported by TOA.

GET
{: .label .label-green .m-1 }


### Endpoint
{: .mt-1 }

```
https://theorangealliance.org/api/regions
```

### Response

This is the API response on 7/30/2021. This particular response is only expected to change once a year.

```json
[
    {
        "region_key": "AB",
        "description": "Alberta - Canada"
    },
    {
        "region_key": "AE",
        "description": "Department of Defense Education Activity"
    },
    {
        "region_key": "AK",
        "description": "Alaska"
    },
    {
        "region_key": "AL",
        "description": "Alabama"
    },
    {
        "region_key": "AR",
        "description": "Arkansas"
    },
    {
        "region_key": "ATG",
        "description": "Antigua and Barbuda"
    },
    {
        "region_key": "AUS",
        "description": "Australia"
    },
    {
        "region_key": "AZ",
        "description": "Arizona"
    },
    {
        "region_key": "BC",
        "description": "British Columbia"
    },
    {
        "region_key": "BRA",
        "description": "Brazil"
    },
    {
        "region_key": "CA",
        "description": "California"
    },
    {
        "region_key": "CALA",
        "description": "California - Los Angeles"
    },
    {
        "region_key": "CANAB",
        "description": "Alberta - Canada"
    },
    {
        "region_key": "CANBC",
        "description": "British Colombia"
    },
    {
        "region_key": "CASD",
        "description": "California - San Diego"
    },
    {
        "region_key": "CHE",
        "description": "Switzerland"
    },
    {
        "region_key": "CHN",
        "description": "China"
    },
    {
        "region_key": "CHNHK",
        "description": "China - Hong Kong"
    },
    {
        "region_key": "CMP",
        "description": "Championship"
    },
    {
        "region_key": "CO",
        "description": "Colorado"
    },
    {
        "region_key": "CT",
        "description": "Connecticut"
    },
    {
        "region_key": "CYP",
        "description": "Cyprus"
    },
    {
        "region_key": "CZE",
        "description": "Czech Republic"
    },
    {
        "region_key": "DC",
        "description": "District of Columbia"
    },
    {
        "region_key": "DE",
        "description": "Delaware"
    },
    {
        "region_key": "DEU",
        "description": "Baden-Württemberg, Germany"
    },
    {
        "region_key": "EGY",
        "description": "Egypt"
    },
    {
        "region_key": "ESP",
        "description": "Spain"
    },
    {
        "region_key": "FIM",
        "description": "FIRST in Michigan"
    },
    {
        "region_key": "FL",
        "description": "Florida"
    },
    {
        "region_key": "FRN",
        "description": "France"
    },
    {
        "region_key": "GA",
        "description": "Georgia"
    },
    {
        "region_key": "GBR",
        "description": "United Kingdom"
    },
    {
        "region_key": "GEO",
        "description": "Georgia"
    },
    {
        "region_key": "GHA",
        "description": "Ghana"
    },
    {
        "region_key": "HI",
        "description": "Hawaii"
    },
    {
        "region_key": "IA",
        "description": "Iowa"
    },
    {
        "region_key": "ID",
        "description": "Idaho"
    },
    {
        "region_key": "IL",
        "description": "Illinois"
    },
    {
        "region_key": "IN",
        "description": "Indiana"
    },
    {
        "region_key": "IND",
        "description": "India"
    },
    {
        "region_key": "ISR",
        "description": "Israel"
    },
    {
        "region_key": "ITA",
        "description": "Italy"
    },
    {
        "region_key": "JAM",
        "description": "Jamaica"
    },
    {
        "region_key": "JPN",
        "description": "Japan"
    },
    {
        "region_key": "KS",
        "description": "Kansas"
    },
    {
        "region_key": "KY",
        "description": "Kentucky"
    },
    {
        "region_key": "LA",
        "description": "Louisiana"
    },
    {
        "region_key": "LBN",
        "description": "Lebanon"
    },
    {
        "region_key": "LBY",
        "description": "Libya"
    },
    {
        "region_key": "MA",
        "description": "Massachusetts"
    },
    {
        "region_key": "MAR",
        "description": "Morocco"
    },
    {
        "region_key": "MD",
        "description": "Maryland"
    },
    {
        "region_key": "MDA",
        "description": "Moldova"
    },
    {
        "region_key": "MEX",
        "description": "Mexico"
    },
    {
        "region_key": "MIHIS",
        "description": "Michigan - HIS"
    },
    {
        "region_key": "MN",
        "description": "Minnesota"
    },
    {
        "region_key": "MO",
        "description": "Missouri"
    },
    {
        "region_key": "MS",
        "description": "Mississippi"
    },
    {
        "region_key": "MT",
        "description": "Montana"
    },
    {
        "region_key": "NC",
        "description": "North Carolina"
    },
    {
        "region_key": "NCAL",
        "description": "Northern California"
    },
    {
        "region_key": "ND",
        "description": "North Dakota"
    },
    {
        "region_key": "NE",
        "description": "Nebraska"
    },
    {
        "region_key": "NGA",
        "description": "Nigeria"
    },
    {
        "region_key": "NH",
        "description": "New Hampshire"
    },
    {
        "region_key": "NJ",
        "description": "New Jersey"
    },
    {
        "region_key": "NLD",
        "description": "Netherlands"
    },
    {
        "region_key": "NM",
        "description": "New Mexico"
    },
    {
        "region_key": "NV",
        "description": "Nevada"
    },
    {
        "region_key": "NY",
        "description": "New York"
    },
    {
        "region_key": "NYC",
        "description": "New York - NYC"
    },
    {
        "region_key": "NYEXC",
        "description": "New York - Excelsior"
    },
    {
        "region_key": "NYHV",
        "description": "New York - Hudson Valley"
    },
    {
        "region_key": "NYLI",
        "description": "New York - Long Island"
    },
    {
        "region_key": "NZL",
        "description": "New Zealand"
    },
    {
        "region_key": "OH",
        "description": "Ohio"
    },
    {
        "region_key": "OK",
        "description": "Oklahoma"
    },
    {
        "region_key": "ON",
        "description": "Ontario"
    },
    {
        "region_key": "OR",
        "description": "Oregon"
    },
    {
        "region_key": "PA",
        "description": "Pennsylvania"
    },
    {
        "region_key": "PAK",
        "description": "Pakistan"
    },
    {
        "region_key": "POL",
        "description": "Poland"
    },
    {
        "region_key": "QAT",
        "description": "Qatar"
    },
    {
        "region_key": "RI",
        "description": "Rhode Island"
    },
    {
        "region_key": "ROU",
        "description": "Romania"
    },
    {
        "region_key": "RUS",
        "description": "Russia"
    },
    {
        "region_key": "SAU",
        "description": "Saudi Arabia"
    },
    {
        "region_key": "SC",
        "description": "South Carolina"
    },
    {
        "region_key": "SD",
        "description": "South Dakota"
    },
    {
        "region_key": "SK",
        "description": "Saskatchewan - Canada"
    },
    {
        "region_key": "SKR",
        "description": "South Korea"
    },
    {
        "region_key": "SWZ",
        "description": "Swaziland"
    },
    {
        "region_key": "TEST",
        "description": "TEST"
    },
    {
        "region_key": "THA",
        "description": "Tailand"
    },
    {
        "region_key": "TN",
        "description": "Tennessee"
    },
    {
        "region_key": "TWN",
        "description": "Taiwan"
    },
    {
        "region_key": "TX",
        "description": "Texas"
    },
    {
        "region_key": "TXARL",
        "description": "Texas - Arlington"
    },
    {
        "region_key": "TXHOU",
        "description": "Texas - Houston"
    },
    {
        "region_key": "TXLUB",
        "description": "Texas - Lubbock"
    },
    {
        "region_key": "TXSA",
        "description": "Texas - San Antonio"
    },
    {
        "region_key": "UT",
        "description": "Utah"
    },
    {
        "region_key": "VA",
        "description": "Virginia"
    },
    {
        "region_key": "VT",
        "description": "Vermont"
    },
    {
        "region_key": "WA",
        "description": "Washington"
    },
    {
        "region_key": "WI",
        "description": "Wisconsin"
    },
    {
        "region_key": "WV",
        "description": "West Virginia"
    },
    {
        "region_key": "WY",
        "description": "Wyoming"
    },
    {
        "region_key": "ZAF",
        "description": "South Africa"
    }
]
```

### Examples

#### cURL
```
curl --location --request GET 'https://theorangealliance.org/api/regions' \
--header 'X-TOA-Key: :your-toa-key' \
--header 'X-Application-Origin: FTC Explorer app'
```

#### JavaScript

```javascript
var axios = require('axios');

var config = {
  method: 'get',
  url: 'https://theorangealliance.org/api/regions',
  headers: { 
    'X-TOA-Key': ':your-toa-key', 
    'X-Application-Origin': 'FTC Explorer app'
  }
};

axios(config)
  .then(function (response) {
    console.log(JSON.stringify(response.data));
  })
  .catch(function (error) {
    console.log(error);
  });
```

---

## Leagues

Returns all the leagues supported by TOA.

GET
{: .label .label-green .m-1 }


### Endpoint
{: .mt-1 }

```
https://theorangealliance.org/api/leagues
```

### Response

This is the API response on 7/30/2021. This particular response is only expected to change once a year.

```json
[
    {
        "league_key": "0506-IA-MAND",
        "region_key": "IA",
        "season_key": "0506",
        "league_description": "Mandalore League"
    },
    {
        "league_key": "1920-GA-NGL",
        "region_key": "GA",
        "season_key": "1920",
        "league_description": "North Georgia League"
    },
    {
        "league_key": "1920-IA-ALDE",
        "region_key": "IA",
        "season_key": "1920",
        "league_description": "Alderaan League"
    },
    {
        "league_key": "1920-IA-BATU",
        "region_key": "IA",
        "season_key": "1920",
        "league_description": "Batuu League"
    },
    {
        "league_key": "1920-IA-BES",
        "region_key": "IA",
        "season_key": "1920",
        "league_description": "Bespin League"
    },
    {
        "league_key": "1920-IA-CORE",
        "region_key": "IA",
        "season_key": "1920",
        "league_description": "Corellia League"
    },
    {
        "league_key": "1920-IA-CORU",
        "region_key": "IA",
        "season_key": "1920",
        "league_description": "Coruscant League"
    },
    {
        "league_key": "1920-IA-KASH",
        "region_key": "IA",
        "season_key": "1920",
        "league_description": "Kashyyyk League"
    },
    {
        "league_key": "1920-IA-LOTH",
        "region_key": "IA",
        "season_key": "1920",
        "league_description": "Lothal League"
    },
    {
        "league_key": "1920-IA-MAND",
        "region_key": "IA",
        "season_key": "1920",
        "league_description": "Mandalore League"
    },
    {
        "league_key": "1920-TX-AML",
        "region_key": "TX",
        "season_key": "1920",
        "league_description": "Austin Metro League"
    }
]
```

### Examples

#### cURL
```
curl --location --request GET 'https://theorangealliance.org/api/leagues' \
--header 'X-TOA-Key: :your-toa-key' \
--header 'X-Application-Origin: FTC Explorer app'
```

#### JavaScript

```javascript
var axios = require('axios');

var config = {
  method: 'get',
  url: 'https://theorangealliance.org/api/leagues',
  headers: { 
    'X-TOA-Key': ':your-toa-key', 
    'X-Application-Origin': 'FTC Explorer app'
  }
};

axios(config)
  .then(function (response) {
    console.log(JSON.stringify(response.data));
  })
  .catch(function (error) {
    console.log(error);
  });
```

---

## Livestreams

Returns a list of active live streams.

GET
{: .label .label-green .m-1 }


### Endpoint
{: .mt-1 }

```
https://theorangealliance.org/api/streams
```

### Response

This is the API response on 7/30/2021. This particular response is only expected to change once a year.

```json
[
    {
        "stream_key": "2021-FIM-MFCQR-LS1",
        "event_key": "2021-FIM-MFCQR",
        "channel_name": "theorangealliance1",
        "stream_name": "MI Coloma Qualifier REMOTE",
        "stream_type": "1",
        "is_active": true,
        "url": "https://player.twitch.tv/?channel=theorangealliance1",
        "start_datetime": "2021-03-14T05:00:00.000Z",
        "end_datetime": "2021-03-20T04:00:00.000Z",
        "channel_url": "https://twitch.tv/theorangealliance1"
    },
    {
        "stream_key": "2021-FIM-MFFSC-LS1",
        "event_key": "2021-FIM-MFFSC",
        "channel_name": "firstinmi01",
        "stream_name": "MI FiM State Championship REMOTE",
        "stream_type": "1",
        "is_active": true,
        "url": "https://player.twitch.tv/?channel=firstinmi01",
        "start_datetime": "2021-05-16T04:00:00.000Z",
        "end_datetime": "2021-05-22T04:00:00.000Z",
        "channel_url": "https://twitch.tv/firstinmi01"
    },
    {
        "stream_key": "2021-FIM-MFHUQ-LS1",
        "event_key": "2021-FIM-MFHUQ",
        "channel_name": "theorangealliance1",
        "stream_name": "MI Howell Ultimate Qualifier REMOTE",
        "stream_type": "1",
        "is_active": true,
        "url": "https://player.twitch.tv/?channel=theorangealliance1",
        "start_datetime": "2021-04-25T04:00:00.000Z",
        "end_datetime": "2021-05-01T04:00:00.000Z",
        "channel_url": "https://twitch.tv/theorangealliance1"
    },
    {
        "stream_key": "2021-ISR-ICTR-LS1",
        "event_key": "2021-ISR-ICTR",
        "channel_name": "firstisrael",
        "stream_name": "Israel Championship",
        "stream_type": "1",
        "is_active": true,
        "url": "https://player.twitch.tv/?channel=firstisrael",
        "start_datetime": "2021-06-09T21:00:00.000Z",
        "end_datetime": "2021-06-09T21:00:00.000Z",
        "channel_url": "https://twitch.tv/firstisrael"
    },
    {
        "stream_key": "2021-UT-UFFPA-LS1",
        "event_key": "2021-UT-UFFPA",
        "channel_name": "",
        "stream_name": "UT Freedom Prep Academy Qualifier",
        "stream_type": "0",
        "is_active": false,
        "url": "https://www.youtube.com/embed/aa1V2QYaY6c",
        "start_datetime": "2021-03-12T05:00:00.000Z",
        "end_datetime": "2021-03-13T05:00:00.000Z",
        "channel_url": "https://www.youtube.com/watch?v=aa1V2QYaY6c"
    },
    {
        "stream_key": "2021-UT-UFHHQ-LS1",
        "event_key": "2021-UT-UFHHQ",
        "channel_name": "",
        "stream_name": "FTC Hurricane High School Qualifier",
        "stream_type": "0",
        "is_active": true,
        "url": "https://www.youtube.com/embed/7SoAlofhHM0",
        "start_datetime": "2021-03-26T06:00:00.000Z",
        "end_datetime": "2021-03-27T06:00:00.000Z",
        "channel_url": "https://www.youtube.com/watch?v=7SoAlofhHM0"
    },
    {
        "stream_key": "2021-UT-UFPCH-LS1",
        "event_key": "2021-UT-UFPCH",
        "channel_name": "kwstoudt",
        "stream_name": "UT Park City High School Qualifier",
        "stream_type": "1",
        "is_active": true,
        "url": "https://player.twitch.tv/?channel=kwstoudt",
        "start_datetime": "2021-04-02T00:00:00.000Z",
        "end_datetime": "2021-04-03T00:00:00.000Z",
        "channel_url": "https://twitch.tv/kwstoudt"
    },
    {
        "stream_key": "2021-UT-UFSC-LS1",
        "event_key": "2021-UT-UFSC",
        "channel_name": "",
        "stream_name": "First Tech Challenge Utah State Championship",
        "stream_type": "0",
        "is_active": true,
        "url": "https://www.youtube.com/embed/VXjavOMdZU8",
        "start_datetime": "2021-04-09T06:00:00.000Z",
        "end_datetime": "2021-04-10T06:00:00.000Z",
        "channel_url": "https://www.youtube.com/watch?v=VXjavOMdZU8"
    },
    {
        "stream_key": "andymarkinc",
        "event_key": null,
        "channel_name": "AndyMark",
        "stream_name": "AndyMark Live",
        "stream_type": "1",
        "is_active": true,
        "url": "https://player.twitch.tv/?channel=andymarkinc",
        "start_datetime": "2020-09-21T21:16:31.000Z",
        "end_datetime": "2021-09-21T21:16:40.000Z",
        "channel_url": "https://twitch.tv/andymarkinc"
    },
    {
        "stream_key": "firstinspires",
        "event_key": null,
        "channel_name": "firstinspires",
        "stream_name": "FIRST Inspires",
        "stream_type": "1",
        "is_active": false,
        "url": "https://player.twitch.tv/?channel=firstinspires",
        "start_datetime": "2019-09-07T15:00:00.000Z",
        "end_datetime": "2019-09-07T18:00:00.000Z",
        "channel_url": "https://twitch.tv/firstinspires"
    },
    {
        "stream_key": "firstupdatesnow",
        "event_key": null,
        "channel_name": "firstupdatesnow",
        "stream_name": "FIRST Update Now",
        "stream_type": "1",
        "is_active": true,
        "url": "https://player.twitch.tv/?channel=firstupdatesnow",
        "start_datetime": "2019-06-29T13:30:00.000Z",
        "end_datetime": "2019-06-29T19:30:00.000Z",
        "channel_url": "https://twitch.tv/firstupdatesnow"
    },
    {
        "stream_key": "theorangealliance1",
        "event_key": null,
        "channel_name": "TOA 1",
        "stream_name": "TOA Live 1",
        "stream_type": "1",
        "is_active": false,
        "url": "https://player.twitch.tv/?channel=theorangealliance1",
        "start_datetime": "2020-09-21T21:16:31.000Z",
        "end_datetime": "2021-09-21T21:16:40.000Z",
        "channel_url": "https://twitch.tv/theorangealliance1"
    },
    {
        "stream_key": "theorangealliance2",
        "event_key": null,
        "channel_name": "TOA 2",
        "stream_name": "TOA Live 2",
        "stream_type": "1",
        "is_active": false,
        "url": "https://player.twitch.tv/?channel=theorangealliance2",
        "start_datetime": "2020-09-21T21:16:31.000Z",
        "end_datetime": "2021-09-21T21:16:40.000Z",
        "channel_url": "https://twitch.tv/theorangealliance2"
    },
    {
        "stream_key": "theorangealliance3",
        "event_key": null,
        "channel_name": "TOA 3",
        "stream_name": "TOA Live 3",
        "stream_type": "1",
        "is_active": false,
        "url": "https://player.twitch.tv/?channel=theorangealliance3",
        "start_datetime": "2020-09-21T21:16:31.000Z",
        "end_datetime": "2021-09-21T21:16:40.000Z",
        "channel_url": "https://twitch.tv/theorangealliance3"
    },
    {
        "stream_key": "theorangealliance4",
        "event_key": null,
        "channel_name": "TOA 4",
        "stream_name": "TOA Live 4",
        "stream_type": "1",
        "is_active": false,
        "url": "https://player.twitch.tv/?channel=theorangealliance4",
        "start_datetime": "2020-09-21T21:16:31.000Z",
        "end_datetime": "2021-09-21T21:16:40.000Z",
        "channel_url": "https://twitch.tv/theorangealliance4"
    },
    {
        "stream_key": "theorangealliance5",
        "event_key": null,
        "channel_name": "TOA 5",
        "stream_name": "TOA Live 5",
        "stream_type": "1",
        "is_active": false,
        "url": "https://player.twitch.tv/?channel=theorangealliance5",
        "start_datetime": "2020-09-21T21:16:31.000Z",
        "end_datetime": "2021-09-21T21:16:40.000Z",
        "channel_url": "https://twitch.tv/theorangealliance5"
    },
    {
        "stream_key": "theorangealliance6",
        "event_key": null,
        "channel_name": "TOA 6",
        "stream_name": "TOA Live 6",
        "stream_type": "1",
        "is_active": false,
        "url": "https://player.twitch.tv/?channel=theorangealliance6",
        "start_datetime": "2020-09-21T21:16:31.000Z",
        "end_datetime": "2021-09-21T21:16:40.000Z",
        "channel_url": "https://twitch.tv/theorangealliance6"
    },
    {
        "stream_key": "theorangealliance7",
        "event_key": null,
        "channel_name": "TOA 7",
        "stream_name": "TOA Live 7",
        "stream_type": "1",
        "is_active": false,
        "url": "https://player.twitch.tv/?channel=theorangealliance7",
        "start_datetime": "2020-09-21T21:16:31.000Z",
        "end_datetime": "2021-09-21T21:16:40.000Z",
        "channel_url": "https://twitch.tv/theorangealliance7"
    },
    {
        "stream_key": "theorangealliance8",
        "event_key": null,
        "channel_name": "TOA 8",
        "stream_name": "TOA Live 8",
        "stream_type": "1",
        "is_active": false,
        "url": "https://player.twitch.tv/?channel=theorangealliance8",
        "start_datetime": "2020-09-21T21:16:31.000Z",
        "end_datetime": "2021-09-21T21:16:40.000Z",
        "channel_url": "https://twitch.tv/theorangealliance8"
    }
]
```

### Examples

#### cURL
```
curl --location --request GET 'https://theorangealliance.org/api/streams' \
--header 'X-TOA-Key: :your-toa-key' \
--header 'X-Application-Origin: FTC Explorer app'
```

#### JavaScript

```javascript
var axios = require('axios');

var config = {
  method: 'get',
  url: 'https://theorangealliance.org/api/streams',
  headers: { 
    'X-TOA-Key': ':your-toa-key', 
    'X-Application-Origin': 'FTC Explorer app'
  }
};

axios(config)
  .then(function (response) {
    console.log(JSON.stringify(response.data));
  })
  .catch(function (error) {
    console.log(error);
  });
```