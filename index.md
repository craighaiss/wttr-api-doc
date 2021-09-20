---
title: "wttr.in API reference"
keywords: homepage
tags: [getting_started]
sidebar: mydoc_sidebar
permalink: index.html
summary: These brief instructions will introduce you to the wttr.in weather API.
toc: false
---

## Introduction

The wttr.in REST API returns weather forecast information that you can use in your applications or websites. While the service is primarily targeted toward consoles, the API is able to represent weather forecast information in [multiple formats](supported-formats.html), including HTML, PNG, JSON, and more.

The wttr.in API does not require authentication, so no key is necessary. You can use standard HTTP verbs in your requests, and the API will return standard response codes.

The wttr.in API relies on the [wego weather client](https://github.com/schachmat/wego) to display weather information.

### Sources for weather data

The wttr.in API currently retrieves data from World Weather Online.

Our developers are currently working to add more resources for weather data, including:
- OpenWeatherMap
- AccuWeather
- Windy.com
- Norwegian Meteorological Institute
- BBC WeatherFeeds
- Australian Government Bureau of Meteorology

### Base URL
The base URL for requests to the wttr.in API is as follows:
```html
http://wttr.in
```

{% include links.html %}
