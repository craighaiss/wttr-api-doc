---
title: "wttr.in API reference"
keywords: homepage
tags: [getting_started]
sidebar: mydoc_sidebar
permalink: index.html
summary: These brief instructions will introduce you to the wttr.in weather API.
---

## Introduction

The wttr.in REST API is a weather forecast service primarily targeted to consoles. This API is able to represent weather forecast information in the following formats:

- ANSI sequences for console HTTP clients, including curl, httpie, and wget
- Plain text
- HTML for web browsers
- PNG for graphical viewers
- JSON for scripts and APIs
- Prometheus metrics for scripts and APIs

wttr.in relies on the [wego weather client](https://github.com/schachmat/wego) to display weather information.

### Sources for weather data

The wttr.in API currently relies on data from World Weather Online.

Our developers are currently working to add more resources for weather data, including:
- OpenWeatherMap
- AccuWeather
- Windy.com
- Norwegian Meteorological Institute
- BBC WeatherFeeds
- Australian Government Bureau of Meteorology

### Base URL
http://wttr.in

{% include links.html %}
