---
published: true
layout: post
title: Why HTTP dictates that responses must arrive in the order they were requested?
---
This post is still in progress. Not Ready for reading.

# Introduction
HTTP is an asymmetric request-response client-server application protocol.
HTTP version 1.1 make bandwidth improvement by utilizing HTTP pipeline technique,
which multiple HTTP requests are sent over a single TCP connection without
waiting for the corresponding responses.

# Requests Arrived at Server
If you are looking at sending HTTP Requests over a single TCP connection,
the TCP connection will ensure HTTP Requests that arrive out of order are
put back into the order they left the client(such as Web browser).

Therefore, from HTTP server's perspective, HTTP Requests are always arrived
according to the order of leaving HTTP clients.

# Responses Sent from Server
The status line of HTTP Responses only consist of three parts, HTTP version,
status code and reason phase. There is no information that refers to the
corresponding request.


# HTTP/2 Asynchronous Operation

# Questions
* Why don't HTTP Responses retain the reference to the specific requests
that triggered it?

# Summary

# Reference
https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol
https://en.wikipedia.org/wiki/HTTP_pipelining
