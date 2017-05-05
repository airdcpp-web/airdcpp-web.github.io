---
layout: documentation
title: Extensions and Web API
description: Using AirDC++ Web API
category: Advanced
order: 7.4
---

# Scripting API

AirDC++ Web Client includes a JSON-based Web API, which can accessed via WebSockets or HTTP REST calls. The API is documented at [http://apidocs.airdcpp.net](http://apidocs.airdcpp.net).

The most convinient way to use the API is to write an extension that can be installed and managed from within the application itself. The primary extension language is JavaScript ([Node.js](https://nodejs.org)) and they are written and published as (almost) regular [npm](https://www.npmjs.com) packages.

- [Extension starter project for JavaScript](https://github.com/airdcpp-web/airdcpp-create-extension)
- [Example extensions for Javascript (WebSocket)](https://github.com/airdcpp-web/airdcpp-extension-js/tree/master/examples)
- [Example extension for Python 3.x (HTTP REST)](https://github.com/airdcpp-web/airdcpp-example-python-extension)
- [Extension specifications](https://github.com/airdcpp-web/airdcpp-extensions)