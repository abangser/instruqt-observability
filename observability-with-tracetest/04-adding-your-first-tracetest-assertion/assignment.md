---
slug: adding-your-first-tracetest-assertion
id: 01onreatn99d
type: challenge
title: Adding your first TraceTest assertion
teaser: A short description of the challenge.
notes:
- type: text
  contents: |
    # Creating a test to validate (and maintain) your trace data

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
timelimit: 2100
---


👀 Another new tab
==================

In this section you again have a new tab added to the right hand side. It is called `🔗 Testing`.

This tab is a running [TraceTest](https://tracetest.io/) instance. TraceTest is an OSS tool that allows you to write validations against trace data.

TraceTest can act independently as a test runner (i.e. actually executing the user flow test case) and a validator (i.e. making assertions against the data collected).

While TraceTest can validate against externally created traces, today we will use TraceTest to write our user flow _and_ do the validation of the resulting trace data.

🗺 First a tour
===============

This instance of TraceTest actually already has some data in it which can give you a sense of how it works.

There are three core pages:
`Tests`: This is the "home" page and lists all current tests. We will be here for most of today
`Test Suites`: This is where you can group together tests into a suite. This is powerful to create a CI suite, but also to create dependent flows like you might do in another API testing tool such as Postman.
`Variable Sets`: This is where you can create different environments / setups for your tests. For example, you can create a set of variables that are valid for dev and a different set for production so the same tests can be run in both.

If you want to run a test that already exists, you can just click the run button on the right (go ahead, hit that button! 🫵).

This opens the second most important view for us today. The detailed test view.

This view also has a number of tabs, but also offers to show you around, so start there and follow that tour.

🆕 Writing your first test
===========================

On the introductory slide it was mentioned that TraceTest can be a runner and a validator, but can also separate and only do validation on previously created data.

Since the two concepts can be separated in TraceTest we are going to focus first on how to write `tests` by creating a test from an existing trace.

🕵🏽‍♂️ Find a trace to test
=======================

To test a specific trace, you will need to first go get a `traceID` from Jaeger on the `🔗 Traces` tab.

Go ahead an search for a trace where you successfully imported a Pokemon.

Once you find your trace, click on it to view the details.

The default view is called the `Trace Timeline` view. You can change the view from the rop right corner where there is a drop down button. Select this button and click on `Trace JSON`. This will open a new tab but give you access to the complete `traceID`.

Copy this `traceID` field and return to the Instruqt tab in your browser and then navigate to the `🔗 Testing` tab.

🧪 Create a TraceTest
=====================

Return to the "home" page by clicking on the `TraceTest` logo in the top right.

Once on the home page, you can select `Create`. This will present you with a number of options including `TraceID`. Select this option.

Provide a name and description of your choosing and then hit `Next`.

Name your variable name the same as what was in the JSON so `traceID` and

> 🐛 Watch out! Small bug here here you need to actually `x` out of the front test modal to get to the variable modal!

In the variable modal, paste the TraceID from the the previous step.

Then hit `Run`.

This should bring up the runner page. If you navigate to the `Trace` tab you should be able to compare this to the trace you had selected in Jaeger!

But this hasn't validated anything yet...


🦾 First, try a template test
=============================

Navigate over to the `Test` tab and you should continue to see the trace on your left, but now a blank work area to the right. At the top of this work area you can click the down arrow (🔽) next to `Add Test Spec` and select one of the snippets.

This will automatically populate a test and immediately run it for you. This is great, but it is not tailored to your request nor is it enough validation. Time to add a second (this time custom) validation.

☑ Now add a custom test
======================

There are two ways to add custom validations and you should try both!

1️⃣ First:

You can use the `Add Test Spec` button to create one from an empty form. TraceTest will automatically select the root span for you, but why don't you try and select a different span, and then add an assertion to it.

> 💡 Tip: If you aren't sure what to assert on, you may want to use the attributes panel on the left to explore options. You can open this with the double chevron (⏩).

2️⃣ Second:

Once within the attributes tab you can actually select the three dots next to an attribute and have an option to `Create a test spec`.

Try making a few assertions and seeing what attributes you would want to assert on.

> 💡 If you want to learn more, you can check out the TraceTest docs at: https://docs.tracetest.io/

🗣 Let's chat
=============

1. When might you use testing against pre-existing traces?
1. What do you think about the template tests, do you agree these are commonly valuable assertions?
1. Are there any other assertions you are thinking of that you aren't sure how to complete in this UI?
