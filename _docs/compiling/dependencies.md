---
layout: documentation
title: Dependencies for compiling
description: Common information about required dependencies
category: Compiling (Web Client)
order: 6.2
---

# Dependencies for compiling

## Supported compilers

**clang** (tested with recent versions)

**gcc** (version 8 or newer is required)

## Required tools

**cmake** (version 3.16 or newer is required)

**pkg-config**

**npm** (required for installing the Web UI)

The npm app (Node package manager) is often shipped as part of the `node`/`nodejs` package. If that's not the case on your platform, you may visit their [home page](https://nodejs.org) for installation instructions.

**python** (for additional installation scripts)


## Required libraries

#### boost

Version 1.54 or newer is required with the following libraries:

- boost-regex
- boost-thread
- boost-system

#### bzip2

#### leveldb

#### maxminddb

#### miniupnpc

Version 1.8 or newer is required

#### nlohmann-json

Version 3 or newer

#### openssl

Version 1.1.0 or newer is required

#### stdc++

#### websocketpp

Version 0.8.2 with the c++20 fixes from the develop branch is required (or newer version, if available). If your package manager doesn't provide the library, see [manual installation instructions](/docs/compiling/websocketpp.html).

#### zlib

## Optional libraries 

#### natpmp 

Provides [NAT-PMP](https://en.wikipedia.org/wiki/NAT_Port_Mapping_Protocol) port mapping capabilities

#### tbb (Intel Thread Building Blocks)

Enhances concurrency, not available for all processor architectures
