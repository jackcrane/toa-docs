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
    ...
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
    ...
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
    ...
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
    ...
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
    ...
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