---
slug: adding-your-first-tracetest
id: 01onreatn99d
type: challenge
title: Adding your first TraceTest
teaser: A short description of the challenge.
notes:
- type: text
  contents: |
    # Using trace data for good (and maintaining it!)

    Given we think this trace data gives a great view of the entire system, it seems reasonable to want to use this to also _validate_ the entire system!

    In addition, while telemetry data is in code, it has a lot of the same properties as comments. In that it may be close to the code, but the chance to drift or "rot" is high. Using the data as a part of high value test suites can help maintain the quality and freshness of the telemetry data.
tabs:
- title: Pokeshop Webapp
  type: service
  hostname: docker-vm
  path: /
  port: 8081
- title: Terminal
  type: terminal
  hostname: docker-vm
- title: Logs
  type: service
  hostname: docker-vm
  path: /
  port: 9999
- title: Traces
  type: service
  hostname: docker-vm
  path: /search
  port: 16686
- title: Testing
  type: service
  hostname: docker-vm
  path: /
  port: 11633
difficulty: basic
timelimit: 600
---


👀 Another new tab
==================

In this section you again have a new tab added to the right hand side. It is called `🔗 Testing`.

This tab is a running [TraceTest](https://tracetest.io/) instance. TraceTest is an OSS tool that allows you to write validations against trace data.

TraceTest can act independently as a test runner (i.e. actually executing the user flow test case) and a validator (i.e. making assertions against the data collected).

While TraceTest can validate against externally created traces, today we will use TraceTest to write our user flow _and_ do the validation of the resulting trace data.

🗺 First a tour
===============
