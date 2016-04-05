---
layout: documentation
title: Features
description: Information about client features
category: General
order: 1.1
---

# Getting started


There must be a common hub server for the people to connect to. A single hub server may handle thousands of users.

If you are joining an existing server, you'll simply just enter ther address of the server you've been given to.

If you are going to set up a new server, it's going to require some effort as there is no inbuilt hub server in the client at the moment. Please see the page [Setting up an own hub](/docs/general/running-a-hub.html) for information.


# Features


## Communication

### Protocol support

The application is built to work on [Advanced Direct Connect](https://en.wikipedia.org/wiki/Advanced_Direct_Connect) network. Legacy [Direct Connect](https://en.wikipedia.org/wiki/Direct_Connect_(protocol)) protocol is supported as well, but the functionality is much more limited in such hubs.

### Encryption

File transfers between clients are encrypted by default. Hubs may also support encrypting data transfers between its users. In addition to that, the client also supports direct encrypted private messaging channels that also prevent hubs from spying on your private conversations.


## Downloads

### Chunked downloads from multiple simultaneous users

Files are downloaded in segments and multiple segments running simultaneously, possibly from different users.

### Support for establishing multiple transfer connections with a single user

This will provide better speeds for users with fast connections or when the per-connection speed between the users is slow (possibly because of long distance).

### Sharing of partially downloaded content.

Clients are able to exchange information about downloaded file chuncks and directory (bundle) content. This will speed up spreading of recent content that are being downloaded by many users simultaneously. Partially downloaded content won't show up in search or filelists to ensure that people won't accidentally end up queueing them.


## Sharing

### Share profiles

You may share different content in different hubs

### Per-directory refreshes

### Instant sharing

Content that is downloaded to a shared folder is shown in share instantly when the file/directory finishes downloading

## Searching

The client sorts the most relevant matches for you search first by default, which makes it possible to use very short/common search terms.

## Partial filelists

Use of partial filelists will greatly speed up opening of new filelists compared to traditional approach of downloading the full filelists, which can be hundreds of megabytes. Partial filelists contain the same information as full filelists and you can continue to browse them even when there are file downloads running from the same user.


## Performance

The client has been tested to work also in extreme real-life use: 

* Thousands of queued files/directories
* Hundreds of terabytes of shared content or more than 10 million share files

The resource usage mainly depends on your transfer speeds (especially when encrypted transfers are enabled) and the number of files shared.