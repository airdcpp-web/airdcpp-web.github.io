---
layout: documentation
title: Command line options
description: Listing of command line options
category: Usage
order: 3.1
---

# Command line options

## Usage 

```$ airdcppd [options]```

## Client options

##### `-h`

Print help

##### `-v`

Print version

##### `-d`

Run as daemon

##### `-p=PATH`

Custom pid file path (default: <CFG_DIR>/.airdcppd.pid)

##### `-c=PATH`

Use the specified config directory for client settings

##### `--no-auto-connect`

Don't connect to any favorite hub on startup

##### `--cdm-hub`

Print all protocol communication with hubs in the console (debug)

##### `--cdm-client`

Print all protocol communication with other clients in the console (debug)

##### `--cdm-web`

Print web API commands and file requests in the console (debug)

## Web server

##### `--configure`

Run initial config wizard or change server ports

##### `--add-user`

Add a new web user with administrative permissions (or change password for existing users)

##### `--remove-user`

Remove web user

##### `--web-resources=PATH`

Use the specified resource directory for web server files