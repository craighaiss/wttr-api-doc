---
title: Supported formats
tags: [formats]
keywords: formats
last_updated: Sep 20, 2021
summary: "A list of the formats supported by the wttr.in API."
sidebar: mydoc_sidebar
permalink: supported-formats.html
---

# Supported formats

The wttr.in API can return data in the following formats.

- ANSI sequences (for console HTTP clients, including curl, httpie, and wget)
- Plain text
- HTML
- PNG
- JSON
- [Prometheus metrics](https://prometheus.io/)

Choose the format that best matches your purpose. For example, if you are developing a console-based application, you will want to choose either ANSI or Plain text format. For websites, choose HTML to render the results directly in the browser, or JSON if you wish to parse the results prior to rendering the forecast data. If you are using this API to monitor forecast data through a monitoring tool such as Prometheus, choose the Prometheus metrics format.

