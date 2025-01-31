---
layout: documentation
title: Portable Linux binaries
description: Portable Linux binaries
category: Installation
order: 2.2
---

# Portable Linux binaries

## Download

**Current application version**: 2.13.3 (Web UI 2.13.1)

- **[64-bit](https://web-builds.airdcpp.net/stable/airdcpp_2.13.3_webui-2.13.1_64-bit_portable.tar.gz)**
- **[32-bit](https://web-builds.airdcpp.net/stable/airdcpp_2.13.3_webui-2.13.1_32-bit_portable.tar.gz)**
- **[ARM](https://web-builds.airdcpp.net/stable/airdcpp_2.13.3_webui-2.13.1_armhf_portable.tar.gz)**

Supported CPUs: 

- ARM: ARMv7 or newer
- 64-bit: CPU with an SSE3 support

Older versions can be downloaded from the [build archive](http://web-builds.airdcpp.net/stable/).


## Usage

Unpack the downloaded archive and run the following terminal commands inside the extracted directory:

Initial configuration wizard

`./airdcppd --configure`

Launch normally

`./airdcppd`


## Updating to a new version

The application can be updated in the same way as it was originally installed, just by replacing the old files with the latest ones from the archive. Your existing configuration files will remain intact.

If you still want to back up your existing configuration before the update, please read the [configuration directory docs](/docs/advanced/config-files.html).

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
