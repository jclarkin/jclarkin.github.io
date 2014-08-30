---
layout: post
title: Week 2 - APIs With Context
date: 2014-01-30
categories:
- Testing
tags: []
status: publish
type: post
published: true
meta:
  _publicize_pending: '1'
author: 
---
This week was spent gaining context on APIs. Questions such as:

*   Who are the consumers of the APIs
*   What is the minimum viable check we want in place for a single API
*   What checks are currently being created by developers
*   What aspects of the [API Checklist](http://www.testinggeek.com/testing-restful-webservices-or-api-testing-remember-papas-be-sfo-deed-help-gc-and-dvla-pc) are of value to a specific group
*   What ways can we black box test an API
*   What ways do we want to white box check the API

We created a diagram of the parts of the white box API framework

+ which layers are being checked via JUnit
+ who are the authors of each layer of checks

This gave me a better understanding of the direction of functionally verifying our API. So the majority of my week was experimentation. My goal was to make it easier for developers to author JUnit checks. My petri dishes are being reviewed, and the results are in the mail :)

There are still a lot of unexplored territory, especially around API consumability. Next week we're going to mindmap what we think we know, and what we think we need to know. That should help give focus to our efforts.

I suspect that communicating our gathered information might be a key next step.