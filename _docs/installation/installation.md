---
layout: documentation
title: Installation
description: Installation main page
category: Installation
order: 2.1
---

# Installation

## Windows

Web functionality is included in the regular [AirDC++ desktop application](http://www.airdcpp.net/) from version 3.10 onwards.

**[Download AirDC++ for Windows](http://www.airdcpp.net/download)**

After you have downloaded the client, you may enable web functionality from `File` -> `Settings` -> `Web server`.

## OS X

There is no installation package available at the moment but developers are able to compile the client from source. See [this issue](https://github.com/airdcpp-web/airdcpp-webclient/issues/37) for more information about the OS X package status.

## Linux/UNIX

More installation packages are wanted for different operating systems. If you want to help with making an installation package available for your favorite operating system, please see this [this Github issue](https://github.com/airdcpp-web/airdcpp-webclient/issues/38).

[Compiling the client on other platforms](/docs/installation/compiling.html)

### Notes for FreeBSD users

AirDC++ Web Client uses IPv6 natively by default. Since FreeBSD has [IPv4-mapped IPv6 addresses](https://en.wikipedia.org/wiki/IPv6#IPv4-mapped_IPv6_addresses) disabled by default, you can access the client only via an IPv6 address. If you need IPv4 connectivity, you may enable support IPv4-mapped IPv6 addresses (future client versions will also add a configurable bind address).

