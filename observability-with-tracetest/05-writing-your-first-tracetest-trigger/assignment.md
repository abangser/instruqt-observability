---
slug: writing-your-first-tracetest-trigger
id: 84re6uvnd0rr
type: challenge
title: Writing your first TraceTest trigger
teaser: A short description of the challenge.
notes:
- type: text
  contents: |
    # Writing triggers to prepare scenarios for validation

    While TraceTest is unique to other testing tools because it can work with pre-existing data, that does not stop it from doing a more tradition trigger of a scenario and then validating the outcome.

    This section will focus on how you trigger a scenario and then you can continue to exercise the validations you practised in the last section.
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

🫵 Time to trigger (poke) the app using TraceTest
=================================================

It is time to create another test. This time using a different trigger type, specifically the `HTTP Request` type.

Once you select this type and click `Next` you can fill in a name and description of your choosing.

The next page will require a HTTP verb (e.g. `GET` or `POST`), a URL and (if applicable) a Request body.

You should use `api:8082` as the start of your URL, but will then need to add the specific path.

Depending how comfortable you are with APIs, you may want to play with different URLs and types. But the simplest option is to keep the verb as `GET` and make the path `/pokemon`. This is the list Pokemon API endpoint and does not require an request bodies making it a fairly simple one to get started with.

Once you are happy with your initial trigger, go ahead and click `Create and Run`. This will immediate close the modal and run the test.

🧐 Check if the request worked
==============================

You should quickly be able to see the success of your API request with the `Status` listed on the top right side of the screen.

If this is a green 200 type response then you are made it work first try! 🙌

If not, you are able to edit the URL and other parameters on the left hand side until you get the response code you are hoping to see.


📊 Next validate the trace is successful
========================================

Once you know the request worked, it is time to review the resulting trace and then add some validations.

Head over to the `Test` tab where the trace should be loading up (this takes a few seconds!). Once loaded, you can explore this trace just like you would any other and start to add test validations to the execution.

⏸ Pause here and have a think
==============================

Where would you choose to use this type of testing? Where would you _not_ choose to use it? What are your hopes (and concerns) over Trace based testing?

What other tools does TraceTest remind you of? Can you imagine using such a tool without major learning curves?

🚂 Let's keep this train
========================

The next two sections start to introduce some of the advanced features of TraceTest which can hopefully help unlock some opportunities for you.
