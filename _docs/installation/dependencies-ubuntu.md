---
layout: documentation
title: Dependencies for compiling (Ubuntu)
description: Installing required packages on Ubuntu
category: Installation
order: 0
---

## Installing packages on Ubuntu

Ubuntu 14.04 or newer is required for installing the client.

### Install tools

`$ sudo apt-get install gcc g++ git cmake npm python pkg-config`

### Install libraries

Note that `libtbb-dev` is an optional dependency as it's not available for all processor architectures (such as armv6).

#### Ubuntu 14.04 LTS

`$ sudo apt-get install libbz2-dev zlib1g-dev libssl-dev libstdc++6 libminiupnpc-dev libnatpmp-dev libtbb-dev libgeoip-dev libboost1.55-dev libboost-regex1.55 libboost-thread1.55 libboost-system1.55 libleveldb-dev`


##### Websocket++

Older versions of Ubuntu don't provide a package for Websocket++, which is required for compiling.

Please follow [manual installation instructions](/docs/installation/websocketpp.html) for installing the package.


#### Ubuntu 15.10 or newer

`$ sudo apt-get install pkg-config libbz2-dev zlib1g-dev libssl-dev libstdc++6 libminiupnpc-dev libnatpmp-dev libtbb-dev libgeoip-dev libboost1.5*-dev libboost-regex1.5* libboost-thread1.5* libboost-system1.5* libleveldb-dev libwebsocketpp-dev`