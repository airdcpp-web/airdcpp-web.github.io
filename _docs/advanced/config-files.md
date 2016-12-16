---
layout: documentation
title: Configuration file location
description: Configuration file location 
category: Advanced
order: 7.2
---

# Configuration file location

The application uses user-specific configuration files by default.

Default configuration path:

`/home/<username>/.airdc++/`

## Using custom location

**Version 1.4.1 or newer is required for customizing the configuration file location**

Put the file *dcppboot.xml* inside the directory *CMAKE_INSTALL_FULL_SYSCONFDIR/airdcpp/* (*/usr/local/etc/airdcpp/* by default).

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