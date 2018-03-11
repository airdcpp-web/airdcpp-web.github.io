---
layout: documentation
title: Dependencies for compiling
description: Common information about required dependencies
category: Installation
order: 2.6
---

# Dependencies for compiling

## Supported compilers

**clang** (tested with recent versions)

**gcc** (version 4.9 or newer is required)

## Required tools

**cmake**

**pkg-config**

**npm** (required for UI installation)

The npm app (Node package manager) is often shipped as part of the `node`/`nodejs` package. If that's not the case on your platform, you may visit their [home page](https://nodejs.org) for installation instructions.

**python** (for additional installation scripts)


## Required libraries

#### boost

Version 1.54 or newer is required

#### boost-regex

#### boost-thread

#### boost-system

#### bzip2

#### maxminddb

#### leveldb

#### miniupnpc

Version 1.8 or newer is required

#### openssl

Version 1.0.0 or newer is required

#### stdc++

#### websocketpp

Version 0.7.0 or newer is heavily recommended due to stability issues in older versions. If your package manager doesn't provide the library, see [manual installation instructions](/docs/installation/websocketpp.html).

#### zlib

## Optional libraries 

#### natpmp 

Provides [NAT-PMP](https://en.wikipedia.org/wiki/NAT_Port_Mapping_Protocol) port mapping capabilities

#### tbb (Intel Thread Building Blocks)

Enhances concurrency, not available for all processor architectures
