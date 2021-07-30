---
layout: default
title: Documentation Decisions
parent: Getting Started
nav_order: 2
---

# Documentation decisions
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

While writing this documentation set, I have chosen to abide by several standards, and several semi-trivial concepts that are frankly up to personal preference.

## Parameters

This is how TOA and I have chosen to embed dynamic information in commands. See the below example:

**Problem**: I wish to retrieve all teams participating at a particular event.

**Given Information**: The event key is `2021-OH-OFSR1-T18`.

**How we will describe the solution in these documents**
```
GET https://theorangealliance.org/api/event/:event_key/teams
```

| Param | Description | Type |
| --- | ----------- | --- |
| `:event_key` | The TOA ID of the event in question | A valid, specific TOA event key |

**How you would interpret this solution for the given problem**
```
GET https://theorangealliance.org/api/event/2021-OH-OFSR1-T18/teams
```

| Param | Description | Type |
| --- | ----------- | --- |
| `:event_key` | The TOA ID of the event in question | A valid, specific TOA event key |

Notice how we replaced `:event_key` with the key of the event, just plopped right in the URL. No colons, commas, or squiggly braces (or whatever these `{}` are called)

## Examples

Examples will **always** be provided in cURL and JavaScript (node.js Axios library) and occasionally in Python. 

If you need any other languages, you can usually find a cURL-based translator online. A few of note are here:

| Language | Translator URL |
| --- | --- |
| Dart | [https://curl.trillworks.com/#dart](https://curl.trillworks.com/#dart) |
| Go | [https://curl.trillworks.com/#go](https://curl.trillworks.com/#go) |
| Java | [https://curl.trillworks.com/#java](https://curl.trillworks.com/#java) |
| PHP | [https://curl.trillworks.com/#php](https://curl.trillworks.com/#php) |
| Python | [https://curl.trillworks.com/#python](https://curl.trillworks.com/#python) |
