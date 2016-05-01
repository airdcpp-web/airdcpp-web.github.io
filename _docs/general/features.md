---
layout: documentation
title: Features
description: Summary of file sharing features supported by the client
category: General
order: 1.2
---

# Features

Summary of file sharing features supported by the client.


## Transfers


### Chunked downloads

Files are downloaded in segments and a single file can be downloaded simultaneously from multiple users.


### Multiple per-user connections

Support for establishing multiple transfer connections with a single user will provide better speeds for users with fast connections or when the per-connection speed between the users is slow (possibly because of long distance).


### Sharing of partially downloaded content.

Clients are able to exchange information about downloaded file chunks and directory (bundle) content. This will speed up spreading of recent content that are being downloaded by many users simultaneously. Partially downloaded content won't show up in search or filelists to ensure that people won't accidentally end up queuing them.


### Encryption

File transfers between clients are encrypted by default. Hubs may also use encryption when communicating with the clients. Additionally, you may establish direct encrypted private messaging channels with other clients to prevent hubs from spying on private conversations.


## Sharing


### Share profiles

You may share different content in different hubs.


### Share refresh on per-directory basis

You may refresh the content of individual roots or subdirectories to speed up refreshes with large shares.


### Instant sharing

Content being downloaded in to a shared folder will appear in share instantly when the file/directory finishes downloading.


## Searching

AirDC++ Web Client sorts the most relevant matches for you search first by default, which makes it possible to use very short/common search terms. It will also choose the fastest sources automatically when queuing new content from search or when searching for alternates for queued content.


## Filelists

AirDC++ Web Client uses exclusively partial filelists for browsing users' shares, meaning that content of each directory will be downloaded on demand. This will greatly speed up opening of new filelists and reduce resource usage compared to traditional approach of downloading full filelists (which can be hundreds of megabytes in size). Partial filelists contain the same information as full filelists and you can continue to browse them even when there are file downloads running from the same user.


## Performance

The client has been tested to handle heavy real-life workloads, such as in the following scenarios: 

* Hundreds of terabytes of shared content or more than 10 million share files
* Thousands of queued files/directories

The resource usage mainly depends on your transfer speeds (especially when encrypted transfers are enabled) and the number of files shared.