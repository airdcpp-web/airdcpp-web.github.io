---
layout: documentation
title: How it works
description: Information about Direct Connect network
category: General
order: 1.1
---

# How it works

AirDC++ Web Client is built to work on [Advanced Direct Connect](https://en.wikipedia.org/wiki/Advanced_Direct_Connect) file sharing network. The legacy [Direct Connect](https://en.wikipedia.org/wiki/Direct_Connect_(protocol)) protocol is supported as well, but the functionality is much more limited in such hubs.

## Direct Connect network

The Direct Connect (DC) network is a decentralized network, made up of individual servers (hubs) that users join to share files. Users can search for files and download them from other users connected to the same hub. A hub only helps to find files and connect users; it does not store any files. File transfers are done directly between clients, in peer-to-peer fashion.

Every hub also acts as an instant messaging server. Users can chat with other users of the same hub using the main chat (visible to every user on the hub) or, alternatively, start a private conversation with a particular user. Some hubs also have special chat rooms for groups of people, such as having a chat only for operators.

It is required to be connected to at least one hub in order to be able transfer files. AirDC++ Web Client doesn't include a listing of public hubs so in case you are joining to an existing hub server, you need to know the address to connect to. If you are going to set up a new hub server, it's going to require some effort as there is no inbuilt hub server in the client (see [Setting up an own hub](/docs/general/running-a-hub.html) for more information).