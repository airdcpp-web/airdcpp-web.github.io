---
layout: documentation
title: Proxying with nginx
description: Example configuration for proxying with nginx
category: Advanced
order: 7.1
---

# Proxying with nginx

Proxying the request can make sense if you have multiple web applications (or an existing web site) and you want them to be accessible from internet from a single, standard port (access to less commonly used port numbers can be blocked in some public networks). Using a proxy server will also simplify certificate management if you want all your web applications to be accessible via HTTPS with a trusted certificate.

See [the nginx documentation](http://nginx.org/en/docs/beginners_guide.html#proxy) for more information about setting up a proxy server.


## Example configuration

```
	#	
	# AirDC++ Web Client
	#
	# You may change the location path but it must always start with "airdcpp".
	# This is because the UI uses URLs for routing so it must be able to determine
	# the base directory from the URL.
	#
	location /airdcpp/ {
	        # Client URL (no need for HTTPS when using localhost)
	        proxy_pass  http://localhost:5600/;

	        # Gzipping javascript will reduce the transferred data significantly
	        # This has no effect if gzip compression is disabled from nginx
	        gzip_types      text/plain application/javascript;

	        # Proxy websockets
	        proxy_http_version 1.1;
	        proxy_set_header Upgrade $http_upgrade;
	        proxy_set_header Connection "upgrade";
	}
```