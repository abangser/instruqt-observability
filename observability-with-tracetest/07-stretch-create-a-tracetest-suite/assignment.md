---
slug: stretch-create-a-tracetest-suite
id: azcz01qbcyxs
type: challenge
title: 'Stretch: Create a TraceTest suite'
teaser: A short description of the challenge.
notes:
- type: text
  contents: |
    # Creating a test suite

    So far you have focused on writing test cases. But sometimes these tests need to be built up from a larger workflow. TraceTest can do that too!
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
timelimit: 2100
---

🦪 The world is your oyster
===========================

At this stage you can do anything you fancy. If you want to try making a suite, feel free to review the documents below. But this will be self paced.

Feel free to work together and/or ask questions to the room as you go!

🚰 Creating flow
================

So far you have created individual test cases, but you may be wondering, what happens when a use case requires multiple steps. For example, a user needs to login before authorising to another endpoint? Or in the case of Pokeshop, you want to create a Pokemon before looking it up again in the list.

The way to do this in TraceTest is to create a suite where the triggers run in order.

🧑🏽‍🎓 First you can study the existing suite
=========================================

The TraceTest server actually already has an example of this visible.

Navigate to the `Test Suite` tab from the home page to see a test suite called `Running all test`.

If you open this up you will see a number of tests run in order. Explore around here a bit to see how it all works.

For example, can you add one of your new tests to this suite? Choose the right location for it to work right!

👷‍♀️ Ok now go to work
====================

Try to make a test suite where there are two tests that need to run in order. But make it so that the second test depends on a specific (and dynamic) value from the result of the first test.

> 💡 This may require variable sets and/or outputs which can both be found in the TraceTest documentation!
