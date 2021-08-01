---
layout: default
title: Event matches
parent: Event
grand_parent: API Reference
nav_order: 4
---

# List matches from an event
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
https://theorangealliance.org/api/event/:toa-event-id/matches
```

## URL Paramaters

| Key | Description | Examples |
| --- | --- | --- |
| toa-event-id | ID of the event you want information about. NOTE: The official FIRST ID and the TOA ID | `2021-AB-AFACR` |

## Model

[View the match model](/reference/event/models.html#match)

## Response

The `:toa-event-id` used for this request was `2021-AB-AFACR`

```json
[
    {
        "match_key": "2021-AB-AFACR-Q001-1-10015",
        "event_key": "2021-AB-AFACR",
        "tournament_level": 1,
        "scheduled_time": "2001-01-01T00:00:00.000Z",
        "match_name": "Quals 1",
        "play_number": 0,
        "field_number": -1,
        "prestart_time": null,
        "match_start_time": null,
        "prestart_count": null,
        "cycle_time": null,
        "red_score": 0,
        "blue_score": -1,
        "red_penalty": 0,
        "blue_penalty": -1,
        "red_auto_score": 0,
        "blue_auto_score": -1,
        "red_tele_score": 0,
        "blue_tele_score": -1,
        "red_end_score": 0,
        "blue_end_score": -1,
        "video_url": null,
        "participants": [
            {
                "match_participant_key": "2021-AB-AFACR-Q001-1-10015-R1",
                "match_key": "2021-AB-AFACR-Q001-1-10015",
                "team_key": "10015",
                "station": 11,
                "station_status": 2,
                "ref_status": 0,
                "team": {
                    "team_key": "10015",
                    "region_key": "AB",
                    "league_key": null,
                    "team_number": 10015,
                    "team_name_short": "Hyper Droid",
                    "team_name_long": "Neighborhood Group",
                    "robot_name": null,
                    "last_active": "2021",
                    "city": "Calgary",
                    "state_prov": "AB",
                    "zip_code": "T2C 4Z6",
                    "country": "Canada",
                    "rookie_year": 2015,
                    "website": "http://ataarobotics.ca/firsttechchallenge/"
                }
            }
        ]
    },
    {
        "match_key": "2021-AB-AFACR-Q001-1-11712",
        "event_key": "2021-AB-AFACR",
        "tournament_level": 1,
        "scheduled_time": "2001-01-01T00:00:00.000Z",
        "match_name": "Quals 1",
        "play_number": 0,
        "field_number": -1,
        "prestart_time": null,
        "match_start_time": null,
        "prestart_count": null,
        "cycle_time": null,
        "red_score": 0,
        "blue_score": -1,
        "red_penalty": 0,
        "blue_penalty": -1,
        "red_auto_score": 0,
        "blue_auto_score": -1,
        "red_tele_score": 0,
        "blue_tele_score": -1,
        "red_end_score": 0,
        "blue_end_score": -1,
        "video_url": null,
        "participants": [
            {
                "match_participant_key": "2021-AB-AFACR-Q001-1-11712-R1",
                "match_key": "2021-AB-AFACR-Q001-1-11712",
                "team_key": "11712",
                "station": 11,
                "station_status": 2,
                "ref_status": 0,
                "team": {
                    "team_key": "11712",
                    "region_key": "AB",
                    "league_key": null,
                    "team_number": 11712,
                    "team_name_short": "Aberhart Robotics Republic (Orange)",
                    "team_name_long": "WILLIAM ABERHART HIGH SCHOOL",
                    "robot_name": null,
                    "last_active": "2021",
                    "city": "Calgary",
                    "state_prov": "AB",
                    "zip_code": "T2M 4G9 ",
                    "country": "Canada",
                    "rookie_year": 2016,
                    "website": "https://aberobotics.github.io/AbeRoboticsWebsite/"
                }
            }
        ]
    },
    ...
]
```

## Examples

### cURL

```
curl --location --request GET 'https://theorangealliance.org/api/event/:toa-event-id/matches' \
--header 'X-TOA-Key: :toa-api-key' \
--header 'X-Application-Origin: :toa-application-origin'
```

### JavaScript

```javascript
var axios = require('axios');

var config = {
  method: 'get',
  url: 'https://theorangealliance.org/api/event/:toa-event-id/matches',
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