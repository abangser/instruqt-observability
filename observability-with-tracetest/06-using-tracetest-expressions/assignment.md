---
slug: using-tracetest-expressions
id: ihyd3rjzvevr
type: challenge
title: Using TraceTest Expressions
teaser: A short description of the challenge.
notes:
- type: text
  contents: |
    # Using expressions for more powerful test cases

    One of the concerns with the tests so far is how tied to the single test trigger they are. This tight coupling can create fragile tests that we don't need any more of.

    In this section we will look at how to write more matcher based selectors and assertions to make your tests more flexible.
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

Can't be blank!
=====================
