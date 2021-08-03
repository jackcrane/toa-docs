---
layout: default
title: Event Models
parent: Event
grand_parent: API Reference
nav_order: 0
---

# Models relevant to events
{: .no_toc}

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Event

| Key | Explanation | Data Type |
| --- | --- | --- |
| `event_key` | The TOA event ID. Can be used as a parameter for other requests | `string` |
| `season_key` | The TOA season ID. Note this is not just the year. [List of supported seasons](/reference/api-models.html#seasons) [How to programatically request supported seasons](/reference/api-methods.html#seasons) | `string` |
| `region_key` | The TOA region ID. [How to programatically request supported regions](/reference/api-methods.html#regions) | `string` |
| `league_key` | The TOA league key. [How to programatically request supported leagues](/reference/api-methods.html#leagues) | `string` |
| `event_code` | **TODO** | `string` |
| `first_event_code` | The FIRST event code. This can be used to reconcile with the FIRST API | `string` |
| `event_type_key` | The TOA event type. [List of supported event types](/reference/api-models.html#event-types)
| `event_region_number` | **TODO** | `number` |
| `division_key` | **TODO** | `number` |
| `event_name` | Official name of the event | `string` |
| `start_date` | Date and time of the event's start. NOTE: Time and date are in zulu time and in the ISO-8601 format. | `string` |
| `end_date` | Date and time of the event's end. NOTE: Time and date are in zulu time and in the ISO-8601 format. | `string` |
| `week_key` | The month (yes, month, *not week* of the event). Just roll with it. | `string` |
| `city` | Location of the tournament. | `string` |
| `state_prov` | Location of the tournament. | `string` |
| `country` | Location of the tournament. | `string` |
| `venue` | Location of the tournament. During COVID-19, remote events were classified here as `Remote Event`. | `string` |
| `website` | Tournament or region's website. | `string` |
| `time_zone` | Presumably the time zone of the event, but always `` (empty). | `string` |
| `is_public` | Presumably to state if the event is public or private, but always `true` | `boolean` |
| `active_tournament_level` | Presumably to state the level of the tournament, but always `` (empty) | `string` |
| `alliance_count` | Presumably to state number of alliances in an event, but always `0` | `number` |
| `field_count` | Presumably to state number of fields in an event, but always `0` | `number` |
| `advance_count` | Presumably to state number of advancement slots in an event, but always `0` | `number` |
| `advance_event` | Presumably the tournament the event advances to, but always `` | `string` |
| `data_source` | Source of the data. [List of data sources](/reference/api-models.html#data-sources) | `number` |

## Match

| Key | Explanation | Data Type |
| --- | --- | --- |
| `match_key` | The TOA ID for the match | `string` |
| `event_key` | The TOA event ID. Can be used as a parameter for other requests | `string` |
| `tournament_level` | Presumably the level of the tournament, but seems to always be `1` | `number` |
| `scheduled_time` | Presumably the time a match is set to start. Always seems to be `2001-01-01T00:00:00.000Z`. NOTE: Time and date are in zulu time and in the ISO-8601 format. | `string` |
| `match_name` | Name of the match in the tournament | `string` |
| `play_number` | **TODO** | `number` |
| `field_number` | The field the match was played on | `number` |
| `prestart_time` | **TODO** | `string` |
| `match_start_time` | The time the match is scheduled to start. | `string` |
| `prestart_count` | **TODO** | `number` |
| `cycle_time` | **TODO** | `string` |
| `red_score` | The score of the red alliance | `number` |
| `blue_score` | The score of the blue alliance | `number` |
| `red_penalty` | The penalties assessed against the red alliance | `number` |
| `blue_penalty` | The penalties assessed against the blue alliance | `number` |
| `red_auto_score` | The red alliance's autonomous score | `number` |
| `blue_auto_score` | The blue alliance's autonomous score | `number` |
| `red_tele_score` | The red alliance's teleop score | `number` |
| `blue_tele_score` | The blue alliance's teleop score | `number` |
| `red_end_score` | The red alliance's endgame score | `number` |
| `blue_end_score` | The blue alliance's endgame score | `number` |
| `video_url` | A URL for a match video | `string` |
| `participants` | An array holding [participant objects](#participant) | `array` |

## Match Details

| Key | Explanation | Data Type |
| --- | --- | --- |
| `match_detail_key` | The TOA ID for the match detail | `string` |
| `match_key` | The TOA ID for the match | `string` |
| `red_min_pen` | Minor penalties assessed against the red alliance | `number` |
| `blue_min_pen` | Minor penalties assessed against the blue alliance | `number` |
| `red_maj_pen` | Major penalties assessed against the red alliance | `number` |
| `blue_maj_pen` | Major penalties assessed against the blue alliance | `number` |
| `red` | An object following the [alliance match detail](#alliance-match-details) schema | `object` |
| `blue` | An object following the [alliance match detail](#alliance-match-details) schema | `object` |

## Alliance Match Detail

This particular schema is only applicable to Ultimate Goal; it will change each year.

| Key | Explanation | Data Type |
| --- | --- | --- |
| `auto_wobble_delivered_1` | If the first wobble was delivered in autonomous | `boolean` |
| `auto_wobble_delivered_2` | If the second wobble was delivered in autonomous | `boolean` |
| `auto_navigated_1` | If a robot navigated (parked) during auto | `boolean` |
| `auto_navigated_2` | If the other robot navigated (parked) during auto | `boolean` |
| `auto_nav_pts` | Points awarded for navigation in auto | `number` |
| `auto_tower_low` | Number of shots to the low goal during auto | `number` |
| `auto_tower_mid` | Number of shots to the mid goal during auto | `number` |
| `auto_tower_high` | Number of shots to the high goal during auto | `number` |
| `auto_tower_points` | Points awarded for the shots to the high, med, and low goals in autonomous | `number` |
| `auto_power_shot_left` | If the robot knocked down the left power shot in autonomous | `boolean` |
| `auto_power_shot_center` | If the robot knocked down the center power shot in autonomous | `boolean` |
| `auto_power_shot_right` | If the robot knocked down the right power shot in autonomous | `boolean` |
| `auto_power_shot_points` | Points awarded for the power shots in autonomous | `number` |
| `auto_wobble_points` | Points awarded for the wobble delivery during autonomous | `number` |
| `tele_tower_low` | Number of shots to the low tower during teleop | `number` |
| `tele_tower_mid` | Number of shots to the mid tower during teleop | `number` |
| `tele_tower_high` | Number of shots to the high tower during teleop | `number` |
| `end_wobble_rings_1` | Number of rings sitting on the wobble for endgame | `number` |
| `end_wobble_rings_2` | Number of rings sitting on the other wobble for endgame | `number` |
| `end_wobble_1` | **TODO** | `number` |
| `end_wobble_2` | **TODO** | `number` |
| `end_wobble_points` | Number of points awarded for wobble delivery in endgame | `number` |
| `end_wobble_ring_points` | Number of points awarded for rings on a delivered wobble in endgame | `number` |
| `end_power_shot_left` | If the robot knocked down the left power shot in endgame | `boolean` |
| `end_power_shot_center` | If the robot knocked down the center power shot in endgame | `boolean` |
| `end_power_shot_right` | If the robot knocked down the right power shot in endgame | `boolean` |
| `end_power_shot_points` | Points awarded for power shots during endgame | `number` |
| `end_nav_points` | Points awarded for navigating in endgame | `number` |

## Participants

| Key | Explanation | Data Type |
| --- | --- | --- |
| `match_participant_key` | Unique TOA ID for the team's involvement in a particular match | `string` |
| `match_key` | The TOA ID for the match | `string` |
| `team_key` | The team number | `string` |
| `station` | Team's position [station definitions](/reference/api-models.html#match-stations) | `number` |
| `station_status` | Team's position status [station status definitions](/reference/api-models.html#match-station-status) | `number` |
| `ref_status` | Referee actions [referee action definitions](/reference/api-models.html#ref-actions) | `number` |
| `team` | Information about the team. Adheres to the [team](#team) model. | `object` |

## Team

| Key | Explanation | Data Type |
| --- | --- | --- |
| `team_key` | Team number | `string` |
| `region_key` | Region. [How to list regions](/reference/api-methods.html#regions) | `string` |
| `league_key` | Region. [How to list leagues](/reference/api-methods.html#leagues) | `string` |
| `team_number` | Team number. Difference between this and `team_key` is the data type | `number` |
| `team_name_short` | Short team name | `string` |
| `team_name_long` | Long team name | `string` |
| `robot_name` | Name of the robot | `string` |
| `last_active` | Last [season](/reference/api-methods.html#seasons) the team participated in | `string` |
| `city` | Location of the team | `string` |
| `state_prov` | Location of the team | `string` |
| `zip_code` | Location of the team | `string` |
| `country` | Location of the team | `string` |
| `rookie_year` | Team's first year competing. *This is not a season, it is a year. For example, 2016 would be valid.* | `string` |
| `website` | Team's website | `string` |