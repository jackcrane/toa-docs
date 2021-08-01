---
layout: default
title: Single Event
parent: Event
grand_parent: API Reference
nav_order: 3
---

# Get information for a single event
{: .no_toc}

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

GET
{: .label .label-green .m-1 }

## Description
{: .mt-1 }

Returns information for only the specific requested event

## Endpoint

```
https://theorangealliance.org/api/event/:toa-event-id
```

## URL Paramaters

| Key | Description | Examples |
| --- | --- | --- |
| toa-event-id | ID of the event you want information about. NOTE: The official FIRST ID and the TOA ID | `2021-AB-AFACR` |

## Model

[View the event model](/reference/event/models.html#event)

## Response

The `:toa-event-id` used for this request was `2021-AB-AFACR`

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
    }
]
```

## Examples

### cURL

```
curl --location --request GET 'https://theorangealliance.org/api/event' \
--header 'X-TOA-Key: :toa-api-key' \
--header 'X-Application-Origin: :toa-application-origin'
```

### JavaScript

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