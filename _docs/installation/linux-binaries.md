---
layout: documentation
title: Portable Linux binaries
description: Portable Linux binaries
category: Installation
order: 2.2
---

# Portable Linux binaries

## Download

- **[64-bit](http://web-builds.airdcpp.net/stable/airdcpp-2.0.0-64-bit-portable.tar.gz)**
- **[32-bit](http://web-builds.airdcpp.net/stable/airdcpp-2.0.0-32-bit-portable.tar.gz)**
- **[ARM](http://web-builds.airdcpp.net/stable/airdcpp-2.0.0-armhf-portable.tar.gz)**

Note: the ARM binary is compatible with ARMv7 and newer architectures only.


## Usage

Unpack the downloaded archive and run the following terminal commands inside the extracted directory:

Initial configuration wizard

`./airdcppd --configure`

Launch normally

`./airdcppd`


## Nightly builds

Nightly builds can be downloaded from http://web-builds.airdcpp.net/develop/


## Migration from non-portable builds

Portable builds will save all settings under the application directory by default, while non-portable versions generally save settings in user's home directory.

Making the application to use your existing settings directory:

1. Rename `dcppboot.xml` to `dcppboot.xml.user`
2. Open the file and change the `ConfigPath` tag to `<ConfigPath>%[HOME]/.airdc++/</ConfigPath>`

If you want to have the settings inside the application directory instead, you may create a directory named `config` and move your settings there.