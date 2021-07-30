---
layout: default
title: API Design
parent: Getting Started
nav_order: 2
---

# API design and structure
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Introduction

TOA's API is designed to follow the REST API specification and design.

They have segmented their API into four categories, organized by HTTP methods (`GET`, `POST`, `PUT`, and `DELETE`) with each accomplishing a different purpose:

`GET` - Getting cached/saved information about teams and events

`POST` - Creating or adding data to TOA's database

`PUT` - Updating information in TOA's database

`DELETE` - Deletes information from TOA's database

## Paths

TOA sorts API endpoints with the URIs used to access them. For example, getting information about a particular event uses the API endpoint URI `/api/event/:event_key`, but if you want to know all the teams participating is at `/api/events/:event_key/teams`.