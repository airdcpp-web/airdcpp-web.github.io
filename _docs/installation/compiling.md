---
layout: documentation
title: Compiling from source
description: Common installation instructions for all platforms
category: Installation
order: 2.5
---

## Table of contents

 * [Installation](#installation)
 * [Updating](#updating)
 * [Installing a development version](#installing-a-development-version)
 * [Uninstalling](#uninstalling)

## Compiling from source

### System requirements

Each compiler thread requires about 1 GB of free RAM. If the system you are compiling on has 1 GB of RAM or less, the compiler will most likely crash. 

You can try the following to solutions to avoid compile-time RAM requirements:

* Add [swap space](https://www.linux.com/news/all-about-linux-swap-space)
* Use [Docker](https://www.docker.com)

### Installing dependencies

You must first install the required tools and packages that are required for compiling.

* [Installing dependencies for Ubuntu](/docs/installation/dependencies-ubuntu.html)

* [Installing dependencies for other distributions](/docs/installation/dependencies.html)


### Download the client

```
$ git clone https://github.com/airdcpp-web/airdcpp-webclient.git
$ cd airdcpp-webclient
```

### Compile

```
$ cmake .
$ make -j2
```
`-j2` after the `make` command means that the client is compiled by using 2 threads. It's a good idea to replace the value with the number of available CPU cores.

With more advanced build scenarios, you might find the [Compiling options](/docs/advanced/compiling-options.html) page useful.

**"Internal compiler error" during compilation**

The compiler ran out of memory. Try freeing up some memory or use a smaller number of threads for compiling.

### Install

```
$ sudo make install
```

### Configure and run

When starting the client for the first time, you need to run the initial configuration script. This will set up the server ports and administrative user account for accessing web user interface.

```
$ airdcppd --configure
```

You may now start the client normally

```
$ airdcppd
```

Access the user interface with your web browser and log in with the user account that was created. If you accepted the default ports and the client is running on the same computer, the following address can be used:

[http://localhost:5600](http://localhost:5600)

#### Note for FreeBSD users

AirDC++ Web Client uses IPv6 natively by default. Since FreeBSD has [IPv4-mapped IPv6 addresses](https://en.wikipedia.org/wiki/IPv6#IPv4-mapped_IPv6_addresses) disabled by default, you can access the client only via an IPv6 address. If you need IPv4 connectivity, you may enable support IPv4-mapped IPv6 addresses (future client versions will also add a configurable bind address).


## Updating

Fetch the latest files

```
$ git pull
```

Remove the old installation. Note that you won't be able to access the Web UI after this command. If you want to keep using the client while the new version is being compiled, You may also choose to perform this step just before running the 'make install' command in the installation section. 

```
$ sudo make uninstall
```

Follow the instructions in the [Compile and install](#compile-and-install) section to install the new version.

**IMPORTANT**: if you had the Web UI open in browser during the upgrade, you should force the latest UI files to be fetched by the browser by reloading the page. Otherwise the UI won't function properly.

Note that if you check the version numbers from the About page (Settings -> About), the last numbers in UI and client versions may differ because minor updates can be released separately for both projects. However, the major version numbers (0.**xx**.x) should always match. The latest available Web UI version can be checked from [the NPM package page](https://www.npmjs.com/package/airdcpp-webui).


## Installing a development version

Development versions can be unstable. Usually you want to run a stable version unless you want to help with finding bugs from upcoming versions or testing recently made bug fixes for your issues.

```
$ git checkout develop
```

Follow the instructions in the [Updating](#updating) section to get the latest changes and to compile and install the new version.


If you want to switch back to a stable release, run

```
$ git checkout master
```

## Uninstalling

```
$ sudo make uninstall
```

You may also remove the source and settings directories as well if you are not going to need them later.
