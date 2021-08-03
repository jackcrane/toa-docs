---
layout: default
title: Authentication
parent: Getting Started
nav_order: 2
---

# Authentication
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## API Access

The API only ever responds with JSON data. To correctly request JSON from the API, set the `Content-Type` header of your request to be `application/json`.

Two custom request headers must be sent with every request you make: `X-TOA-Key` and `X-Application-Origin`. `X-TOA-Key` should be the value of your API key, and `X-Application-Origin` should be the name of your application. Without either of these headers, your request will be denied by the API.

## Getting an API Key

Visit your TOA account page ([https://theorangealliance.org/account](https://theorangealliance.org/account)). On the right side of the page, there is a button that says `Generate a key`. Click that button and after several seconds, you will have an API access key. If you do not see a button there but you see a long string of random alphanumeric characters, that is your API key.

In our request, we will need to set the `X-TOA-Key` header to that key we just generated.

## Dealing with application origins

TOA requires this header to be present, but it can be whatever you want. The point of this header is so they can see who is using their services for analytical purposes. It would be respectful for you to fill this out in a meaningful way.

In our request, we will set the `X-Application-Origin` header to whatever we are calling our application.

## Setting our content-type header

We will need to set a `content-type` header on our request, and it must be set to `application/json`