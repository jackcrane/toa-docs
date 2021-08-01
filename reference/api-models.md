---
layout: default
title: API Models
parent: API Reference
nav_order: 2
---


# API Models
{: .no_toc}

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Type definitions

### Event types

| Key | Type |
| --- | --- |
| `LGCMP` | League Championship |
| `LGMEET` | League Meet |
| `OFFSSN` | Offseason |
| `QUAL` | Qualifier |
| `RCMP` | Region Championship |
| `SCRIMMAGE` | Scrimmage |
| `SPRING` | Spring Event |
| `SPRQUAL` | Super Qualifier |
| `SPRREGNL` | Super Regional |
| `WORLDCMP` | World Championship |
| `OTHER` | Other |

### Data sources

| Key | Source |
| --- | --- |
| `0` | Unknown |
| `1` | DataSync |
| `2` | Event Archive |
| `3` | FIRST Official |
| `4` | Unofficial |
| `5` | Other |

### Match stations

| Key | Position |
| --- | --- |
| `11` | Red 1 |
| `12` | Red 2 |
| `13` | Red 3 |
| `21` | Blue 1 |
| `22` | Blue 2 |
| `23` | Blue 3 |

### Match station status

| Key | Status |
| --- | --- |
| `0` | Surrogate |
| `1` | Normal |
| `2` | Sit Out during Match (elims only) |

### Ref Actions 

| Key | Status |
| --- | --- |
| `0` | No Action |
| `1` | No Show |
| `2` | Yellow Card |
| `3` | Red Card |