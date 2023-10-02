---
slug: using-tracetest-advanced-features
id: ihyd3rjzvevr
type: challenge
title: Using TraceTest advanced features
teaser: A short description of the challenge.
notes:
- type: text
  contents: |
    # Using expressions and selectors for more powerful test cases

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
timelimit: 2100
---

😑 What are expressions?
========================

Expressions aren't just something a person's face shows. They are also a way to write small bits of logic to result in an answer. For example, an `if` statement is an expression that results in `true` or `false` as an answer.

The full documentation on TraceTest expressions can be found here: https://docs.tracetest.io/concepts/expressions/

🧮 Calculating response time
============================

One way to use expressions is to set a more flexible response assertion.

For example, try writing a test that checks for response time but sets a limit of acceptable response time rather than a specific value.

📝 Selecting spans
==================

Selectors are the logic for deciding what parts of a Trace the assertions should run against. You may want something to be true for all spans (e.g. no errors) while wanting something else to be only true for one or a few spans (e.g. a specific value found in only one service).

The full documentation on TraceTest selectors can be found here: https://docs.tracetest.io/concepts/selectors

🕵🏽‍♂️ Selecting spans
==================

Spans can be particularly useful for reducing duplicated test cases.

Try and use the built in helpers to select current and all spans, but also try and work with the expression to select only a few of the spans that you may want to validate against.

👷🏽‍♀️ Putting these to use
=======================

So remember that test you did on a trace that succeeded at importing a Pokemon?

Well what would happen if you selected a trace that did _not_ succeed?

Did the things you expect to fail fail? If not, can you use selectors or expression to write a more powerful (and flexible) test?

🗣 Let's chat
=============

1. Can you think of a use case for tracing and TraceTest in your organisation?
1. How would thinking about testing in this way chance your team's perspective?

🎬 This is the end of the guided tour
===================================================

Like any tool, there is a lot to learn. With the topics we have covered so far you can easily spend the rest of the day or even week honing your understanding and skills.

Thinking about logs, traces, and testing traces are big topics.

Go ahead to the next section where you will be free to explore anything you like and maybe you could even try creating a test suite with data passing between steps ✨
