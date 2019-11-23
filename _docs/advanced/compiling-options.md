---
layout: documentation
title: Build options
description: Advanced options for CMake 
category: Advanced
order: 7.1
---

# Compiling options

This page lists various options that can be used with CMake. Customizing the options is useful especially for package maintainers or when cross-compiling the application.

**Usage example**

`cmake -DINSTALL_WEB_UI=ON/OFF .`


**External guides**

* [Cross compiling](http://www.vtk.org/Wiki/CMake_Cross_Compiling)
* [Useful generic variables](https://gitlab.kitware.com/cmake/community/wikis/doc/cmake/Useful-Variables)


## Option help

### -DCMAKE_BUILD_TYPE=TYPE

**Default**: RelWithDebugInfo

**Available types**:

* Release: release build without debug symbols (saves disk space but makes solving of crashes and freezes difficult)
* RelWithDebugInfo: release build with debug symbols included
* Debug: full debug build that adds additional runtime validations and console debug messages


### -DINSTALL_WEB_UI=ON/OFF

**Default**: ON

Don't download and install the [Web UI](https://github.com/airdcpp-web/airdcpp-webui/) when compiling the client, allowing the Web UI to be packaged separately. This also drops the `npm` dependency. [Semantic versioning](http://semver.org/) is followed in regards of UI/daemon compatibility.

### -DBUILD_SHARED_LIBS

**Default**: ON

If disabled, a static binary will be built.
