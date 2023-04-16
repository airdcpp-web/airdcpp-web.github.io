---
layout: documentation
title: Portable Linux binaries
description: Portable Linux binaries
category: Installation
order: 2.2
---

# Portable Linux binaries

## Download

**Current application version**: 2.11.4 (Web UI 2.11.5)

- **[64-bit](https://web-builds.airdcpp.net/stable/airdcpp_2.11.4_webui-2.11.5_64-bit_portable.tar.gz)**
- **[32-bit](https://web-builds.airdcpp.net/stable/airdcpp_2.11.4_webui-2.11.5_32-bit_portable.tar.gz)**
- **[ARM](https://web-builds.airdcpp.net/stable/airdcpp_2.11.4_webui-2.11.5_armhf_portable.tar.gz)**

Note: the ARM binary is compatible with ARMv7 and newer architectures only.

Older versions can be downloaded from the [build archive](http://web-builds.airdcpp.net/stable/).


## Usage

Unpack the downloaded archive and run the following terminal commands inside the extracted directory:

Initial configuration wizard

`./airdcppd --configure`

Launch normally

`./airdcppd`


## Beta builds

[Beta build archive](https://web-builds.airdcpp.net/develop/)


## Cross-compiling for other architectures

If you want to cross-compile your own portable binaries for a custom architecture, see the [compiling instructions for Buildroot](https://github.com/airdcpp-web/airdcpp-webclient/tree/master/buildroot).


## Migration from non-portable builds

Portable builds will save all settings under the application directory by default, while non-portable versions generally save settings in the user's home directory.

To make the application use your existing settings directory:

1. Rename `dcppboot.xml` to `dcppboot.xml.user`
2. Open the file and change the `ConfigPath` tag to `<ConfigPath>%[HOME]/.airdc++/</ConfigPath>`

If you want to have the settings inside the application directory instead, you may create a directory named `config` and move your settings there.
