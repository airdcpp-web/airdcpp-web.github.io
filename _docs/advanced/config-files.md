---
layout: documentation
title: Configuration directory location (Web Client)
description: Configuration directory location 
category: Advanced
order: 7.2
---

# Configuration directory location

The configuration directory location is customizable.

## Default configuration location
### Portable builds

As the installation is meant to be portable, also the config files are stored inside the application directory by default. The name of the configuration directory is `config`.

### Standard installation

`/home/<username>/.airdc++/`

## Using custom location

### Portable builds

Rename the file *dcppboot.xml* that is located next to the application binary to *dcppboot.xml.user* so that it won't be overwritten with the defaults when the application is being updated. You can then edit the file as needed.

### Standard installation

Put the file *dcppboot.xml* inside the directory *CMAKE_INSTALL_FULL_SYSCONFDIR/airdcpp/* (*/usr/local/etc/airdcpp/* by default for self-compiled builds).

Example content of *dcppboot.xml*:

```
<Boot>
    <!--
    ConfigPath specifies where settings, queue and other runtime data should be saved.
    You may use the following variables, which are interpreted on a per-user basis:

    %[HOME] - User's home directory, typically /home/<username>/

    All % variables from strftime with the current time:
    http://www.cplusplus.com/reference/ctime/strftime/

    -->
    <ConfigPath>%[HOME]/airdcpp_mycustomconfig/</ConfigPath>
</Boot>
```