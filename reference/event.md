---
layout: default
title: Event
parent: API Reference
nav_order: 2
---


# Event
{: .no_toc}

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## List all events

GET
{: .label .label-green .m-1 }

### Description
{: .mt-1 }

Returns all events based upon the given query.	

### Endpoint

```
https://theorangealliance.org/api/event
```

### Queries

| Key | Description | Examples |
| --- | --- | --- |
| league_key | **TODO** | `0506-IA-MAND`, `1920-IA-BATU` [How to list leagues](/reference/api-methods.html#leagues) |
| region_key | State / region the event takes palce | `OH`, `CA`, `AB` |
| season_key | Season the event takes place | `2021` |

### Response

```json
[
    {
        "event_key": "2021-AB-AFACR",
        "season_key": "2021",
        "region_key": "AB",
        "league_key": null,
        "event_code": "AFACR",
        "first_event_code": "CAABALCT1",
        "event_type_key": "OTHER",
        "event_region_number": 0,
        "division_key": 0,
        "division_name": null,
        "event_name": "AB Alberta Championship REMOTE",
        "start_date": "2021-05-23T00:00:00.000Z",
        "end_date": "2021-05-29T00:00:00.000Z",
        "week_key": "May",
        "city": "Remote Event ",
        "state_prov": "AB",
        "country": "Canada",
        "venue": "Remote Event",
        "website": "https://ftcalberta.ca/",
        "time_zone": "",
        "is_public": true,
        "active_tournament_level": "",
        "alliance_count": 0,
        "field_count": 0,
        "advance_spots": 0,
        "advance_event": "",
        "data_source": 3
    },
    {
        "event_key": "2021-AB-AFMR1",
        "season_key": "2021",
        "region_key": "AB",
        "league_key": null,
        "event_code": "AFMR1",
        "first_event_code": "CAABALM1",
        "event_type_key": "OTHER",
        "event_region_number": 0,
        "division_key": 0,
        "division_name": null,
        "event_name": "AB Meet- Round 1 REMOTE",
        "start_date": "2020-12-06T00:00:00.000Z",
        "end_date": "2020-12-12T00:00:00.000Z",
        "week_key": "December",
        "city": "Remote Event ",
        "state_prov": "AB",
        "country": "Canada",
        "venue": "Remote Event",
        "website": "https://ftcalberta.ca/",
        "time_zone": "",
        "is_public": true,
        "active_tournament_level": "",
        "alliance_count": 0,
        "field_count": 0,
        "advance_spots": 0,
        "advance_event": "",
        "data_source": 0
    },
    ...
]
```

### Examples

#### cURL

```
curl --location --request GET 'https://theorangealliance.org/api/event' \
--header 'X-TOA-Key: :toa-api-key' \
--header 'X-Application-Origin: :toa-application-origin'
```

#### JavaScript

```javascript
var axios = require('axios');

var config = {
  method: 'get',
  url: 'https://theorangealliance.org/api/event',
  headers: { 
    'X-TOA-Key': ':toa-api-key', 
    'X-Application-Origin': ':toa-application-origin'
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

## List information for a specific event

GET
{: .label .label-green .m-1 }

### Description
{: .mt-1 }

Returns information for only the specific requested event

### Endpoint

```
https://theorangealliance.org/api/event/:toa-event-id
```

### URL Paramaters

| Key | Description | Examples |
| --- | --- | --- |
| toa-event-id | ID of the event you want information about. NOTE: The official FIRST ID and the TOA ID | `2021-AB-AFACR` |

### Response

```json
[
    {
        "event_key": "2021-AB-AFACR",
        "season_key": "2021",
        "region_key": "AB",
        "league_key": null,
        "event_code": "AFACR",
        "first_event_code": "CAABALCT1",
        "event_type_key": "OTHER",
        "event_region_number": 0,
        "division_key": 0,
        "division_name": null,
        "event_name": "AB Alberta Championship REMOTE",
        "start_date": "2021-05-23T00:00:00.000Z",
        "end_date": "2021-05-29T00:00:00.000Z",
        "week_key": "May",
        "city": "Remote Event ",
        "state_prov": "AB",
        "country": "Canada",
        "venue": "Remote Event",
        "website": "https://ftcalberta.ca/",
        "time_zone": "",
        "is_public": true,
        "active_tournament_level": "",
        "alliance_count": 0,
        "field_count": 0,
        "advance_spots": 0,
        "advance_event": "",
        "data_source": 3
    },
    {
        "event_key": "2021-AB-AFMR1",
        "season_key": "2021",
        "region_key": "AB",
        "league_key": null,
        "event_code": "AFMR1",
        "first_event_code": "CAABALM1",
        "event_type_key": "OTHER",
        "event_region_number": 0,
        "division_key": 0,
        "division_name": null,
        "event_name": "AB Meet- Round 1 REMOTE",
        "start_date": "2020-12-06T00:00:00.000Z",
        "end_date": "2020-12-12T00:00:00.000Z",
        "week_key": "December",
        "city": "Remote Event ",
        "state_prov": "AB",
        "country": "Canada",
        "venue": "Remote Event",
        "website": "https://ftcalberta.ca/",
        "time_zone": "",
        "is_public": true,
        "active_tournament_level": "",
        "alliance_count": 0,
        "field_count": 0,
        "advance_spots": 0,
        "advance_event": "",
        "data_source": 0
    },
    ...
]
```

### Examples

#### cURL

```
curl --location --request GET 'https://theorangealliance.org/api/event' \
--header 'X-TOA-Key: :toa-api-key' \
--header 'X-Application-Origin: :toa-application-origin'
```

#### JavaScript

```javascript
var axios = require('axios');

var config = {
  method: 'get',
  url: 'https://theorangealliance.org/api/event',
  headers: { 
    'X-TOA-Key': ':toa-api-key', 
    'X-Application-Origin': ':toa-application-origin'
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