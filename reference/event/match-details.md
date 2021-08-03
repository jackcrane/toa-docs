---
layout: default
title: Event match details
parent: Event
grand_parent: API Reference
nav_order: 5
---

# List match details from an event
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

Returns all the matches from a specified event

## Endpoint

```
https://theorangealliance.org/api/event/:toa-event-id/matches/details
```

## URL Paramaters

| Key | Description | Examples |
| --- | --- | --- |
| toa-event-id | ID of the event you want information about. NOTE: The official FIRST ID and the TOA ID | `2021-AB-AFACR` |

## Model

[View the match details model](/reference/event/models.html#match-details)

## Response

The `:toa-event-id` used for this request was `2021-AB-AFACR`

```json
[
    {
        "match_detail_key": "2021-AB-AFACR-Q001-1-10015-DTL",
        "match_key": "2021-AB-AFACR-Q001-1-10015",
        "red_min_pen": 0,
        "blue_min_pen": -1,
        "red_maj_pen": 0,
        "blue_maj_pen": -1,
        "red": {
            "auto_wobble_delivered_1": false,
            "auto_wobble_delivered_2": false,
            "auto_navigated_1": false,
            "auto_navigated_2": false,
            "auto_nav_pts": null,
            "auto_tower_low": 0,
            "auto_tower_mid": 0,
            "auto_tower_high": 0,
            "auto_tower_points": 0,
            "auto_power_shot_left": false,
            "auto_power_shot_center": false,
            "auto_power_shot_right": false,
            "auto_power_shot_points": 0,
            "auto_wobble_points": 0,
            "tele_tower_low": 0,
            "tele_tower_mid": 0,
            "tele_tower_high": 0,
            "end_wobble_rings_1": 0,
            "end_wobble_rings_2": 0,
            "end_wobble_1": 0,
            "end_wobble_2": 0,
            "end_wobble_points": 0,
            "end_wobble_ring_points": 0,
            "end_power_shot_left": false,
            "end_power_shot_center": false,
            "end_power_shot_right": false,
            "end_power_shot_points": 0,
            "end_nav_points": null
        },
        "blue": {
            "auto_wobble_delivered_1": false,
            "auto_wobble_delivered_2": false,
            "auto_navigated_1": false,
            "auto_navigated_2": false,
            "auto_nav_pts": null,
            "auto_tower_low": null,
            "auto_tower_mid": null,
            "auto_tower_high": null,
            "auto_tower_points": null,
            "auto_power_shot_left": false,
            "auto_power_shot_center": false,
            "auto_power_shot_right": false,
            "auto_power_shot_points": null,
            "auto_wobble_points": null,
            "tele_tower_low": null,
            "tele_tower_mid": null,
            "tele_tower_high": null,
            "end_wobble_rings_1": null,
            "end_wobble_rings_2": null,
            "end_wobble_1": null,
            "end_wobble_2": null,
            "end_wobble_points": null,
            "end_wobble_ring_points": null,
            "end_power_shot_left": false,
            "end_power_shot_center": false,
            "end_power_shot_right": false,
            "end_power_shot_points": null,
            "end_nav_points": null
        }
    },
    ...
]
```

## Examples

### cURL

```
curl --location --request GET 'https://theorangealliance.org/api/event/:toa-event-id/matches/details' \
--header 'X-TOA-Key: :toa-api-key' \
--header 'X-Application-Origin: :toa-application-origin'
```

### JavaScript

```javascript
var axios = require('axios');

var config = {
  method: 'get',
  url: 'https://theorangealliance.org/api/event/:toa-event-id/matches/details',
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