---
layout: documentation
title: Portable Linux binaries
description: Portable Linux binaries
category: Installation
order: 2.2
---

# Portable Linux binaries

## Download

**Current application version**: 2.10.0 (Web UI 2.10.0)

- **[64-bit](https://web-builds.airdcpp.net/stable/airdcpp_2.10.0_webui-2.10.0_64-bit_portable.tar.gz)**
- **[32-bit](https://web-builds.airdcpp.net/stable/airdcpp_2.10.0_webui-2.10.0_32-bit_portable.tar.gz)**
- **[ARM](https://web-builds.airdcpp.net/stable/airdcpp_2.10.0_webui-2.10.0_armhf_portable.tar.gz)**

Note: the ARM binary is compatible with ARMv7 and newer architectures only.

If you want to cross-compile your own portable binaries for a custom architecture, see the [compiling instructions for Buildroot](https://github.com/airdcpp-web/airdcpp-webclient/tree/master/buildroot).


## Usage

Unpack the downloaded archive and run the following terminal commands inside the extracted directory:

Initial configuration wizard

`./airdcppd --configure`

Launch normally

`./airdcppd`


## Nightly builds

[Nightly build archive](https://web-builds.airdcpp.net/develop/)


## Migration from non-portable builds

Portable builds will save all settings under the application directory by default, while non-portable versions generally save settings in user's home directory.

Making the application to use your existing settings directory:

1. Rename `dcppboot.xml` to `dcppboot.xml.user`
2. Open the file and change the `ConfigPath` tag to `<ConfigPath>%[HOME]/.airdc++/</ConfigPath>`

If you want to have the settings inside the application directory instead, you may create a directory named `config` and move your settings there.