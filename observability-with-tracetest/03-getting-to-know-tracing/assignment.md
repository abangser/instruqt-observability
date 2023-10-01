---
slug: getting-to-know-tracing
id: gmyxiuymytpk
type: challenge
title: Getting to know tracing
teaser: A short description of the challenge.
notes:
- type: text
  contents: |
    # Introducing traces

    After some time to explore logs, you may have a few questions about how to understand the complete architecture using only telemetry data.

    This section will introduce traces as a way to understand how the pieces of the architecture interact with each other.
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
difficulty: basic
timelimit: 600
---

👀 I spy a new tab!
===================

You can see that there is a new tab added to the right hand side called `🔗 Traces`.

This tab is a running [Jaeger](https://www.jaegertracing.io/) instance. Jaeger is an open source distributed tracing application.


👣 Exploring Jaeger traces
==========================

In Jaeger you can look for a specific trace using the search bar at the top, or you can browse traces by adding filters on the left.

Since you do not have a specific trace ID to search for yet, you should start by trying to find a specific action that you take in the UI.

For example, try to add a new Pokemon and find the trace that correlates with that action.


🕸 The web of services involved in a single action
==================================================

If you found your action as a trace, you can likely see that this single action actually required a number of different services and sub actions.

Each green bar (or row) indicates a sub action. In the case of import, there are both database and streaming requests made.


🔙 Let's go back to logs as well
================================

While we have introduced tracing as a way to solve the challenge of viewing requests across time and across services, it is helpful to compare this to our old (and the more common) way of doing this in logs to really feel the difference.

🎉 Congratulations! You have now used logs AND traces
=====================================================

This may be something you do all the time, or it may be your first time. But either way, you have build up some experience with working your way around an application's telemetry.

Next up we will take these new experiences and pair them with your deep testing expertise to write a system test!
