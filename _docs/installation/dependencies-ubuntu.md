---
layout: documentation
title: Dependencies for compiling (Ubuntu)
description: Installing required packages on Ubuntu
category: Installation
order: 0
---

## Installing packages on Ubuntu

**IMPORTANT: unless you are going to edit the source code, the recommended way to install the application on Ubuntu is to use the provided [portable binaries](/docs/installation/linux-binaries.html)**

Ubuntu 16.04 or newer is required for compiling the client.

### Install tools

`$ sudo apt-get install gcc g++ git cmake npm python pkg-config`

### Install libraries

`$ sudo apt install pkg-config libbz2-dev zlib1g-dev libssl-dev libstdc++6 libminiupnpc-dev libnatpmp-dev libtbb-dev libgeoip-dev libboost1.58-dev libboost-regex1.58 libboost-thread1.58 libboost-system1.58 libleveldb-dev libwebsocketpp-dev`

The installation command is targeted for Ubuntu 16.04 LTS. For installation on newer distributions, please see the [Notes](#notes) section below.

#### Notes

* `libtbb-dev` is an optional dependency as it's not available for all processor architectures (such as armv6).
* The version number of `libboost-*` packages generally differs in each Ubuntu release. If you get installation errors related to libboost packages, use the command `apt-cache search libboost` to check the latest version available for your system and replace all versions numbers in the installation command accordingly. 