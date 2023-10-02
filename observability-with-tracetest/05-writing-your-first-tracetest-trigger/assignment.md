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

Once you select this type and click `Next` you can select the `Choose Example v` text to select from a few pre-filled templates. You can select import to mimic the last test we did against the existing trace.

💡 All the template does is fill in the text fields. All field values will be provided in these instructions if you prefer to type them yourself.

If you chose to use a template, you can still change any of the fields, so feel free to customise the name or description to your liking. Once satisfied, click `Next`.

This page should look familiar if you have used any other visual UIs for API testing. If not, that is OK because we will walk through it.

There are three key fields you will need to set:
1. **HTTP verb**: This is a drop down list and should be set to `POST` for import or add, or `GET` for list
1. **URL**: The base URL is `http://api:8081/pokemon` but you may need an additional path if you want to test import (`import`) or list (`?take=20&skip=0`). The full API docs can be found [here](https://github.com/kubeshop/pokeshop/blob/master/docs/overview.md).
1. **Request body**: If you are listing you will want to set this to None. But for both import and add you will need to set it to `JSON` and provide the corresponding values. For import the format is `{"id": 123}` and for add it is `{"name": "foo", "type": "normal", "imageUrl": "https://assets.pokemon.com/assets/cms2/img/pokedex/full/052.png", isFeatured: false}`.

Once you are happy with your initial trigger, go ahead and click `Create and Run`. This will immediate close the modal and run the test.

> 💡 Don't stress too much about this. We will be validating it and can edit as needed!

🧐 Check if the request worked
==============================

You should quickly be able to see the success of your API request with the `Status` listed on the top right side of the screen.

If this is a green 200 type response then you are made it work first try! 🙌

If not, you are able to edit the URL and other parameters on the left hand side until you get the response code you are hoping to see.


📊 Next validate the trace is successful
========================================

Once you know the request worked, it is time to review the resulting trace and then add some validations.

Head over to the `Test` tab where the trace should be loading up (this takes a few seconds). Once loaded, you can explore this trace just like you would any other and start to add test validations to the execution.

🔂 Create a different HTTP test
===============================

Now that you have the hang of it, try another!

🗣 Let's chat
=============

1. Where would you choose to use this type of testing? Where would you _not_ choose to use it?
1. What are your hopes (and concerns) over Trace based testing?
1. What other tools does TraceTest remind you of?
1. Can you imagine using such a tool without major learning curves?
