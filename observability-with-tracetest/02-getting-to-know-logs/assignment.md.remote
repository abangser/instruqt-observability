---
slug: getting-to-know-logs
id: 5yzykftyatdg
type: challenge
title: Exploring Pokeshop
teaser: Explore our shared webapp and how logs can provide insights
notes:
- type: text
  contents: |
    # Exploring Pokeshop through logs

    Pokeshop is a web app and API that allows you to collect your favourite
    Pokemon. You can do this with either importing existing Pokemon or creating
    new ones.

    This section will introduce you to the application, allow you to explore its
    features, and also understand how logs work with the multi-service application.
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
difficulty: basic
timelimit: 600
---

👾 Pokeshop, a way to collect them all!
=======================================

The website is pretty simple in that it only has a handful of actions users may do:

1. View all Pokemon on the homepage
1. Add a new Pokemon
1. Import an existing Pokemon
1. Remove a Pokemon

Have a look around so that you can get to know the user experience of this website.

Once you are content with the features from the UI, it is time to investigate the architecture.


🏛 Pokeshop architecture
========================

What seems simple at first can often have a lot of complexity behind the scenes. With the user experience you may expect to see a UI, API, and Database. But did you know it also has a queuing system to manage streaming requests?

You can see the full architecture [here](https://docs.tracetest.io/live-examples/pokeshop/overview/#system-architecture).


🪵 Viewing application logs
===========================

If you needed to investigate what is happening in this application you may need to use the logs in one or more services.

To view logs you can go to the new tab called `🔗 Logs` which is a [Dozzle](https://dozzle.dev/) service that gives access to logs of all running Docker containers.

Once in the Logs tab, go ahead and explore to try and find your own actions in the web app displayed in logs.

> 💡 Hint! You can roll over the small coloured dots (🔴🔵) in the top right corner to open a search box for any one stream.

For example, can you import a Pokemon and see how it flows through the architecture?

Spend a few minutes on this before finishing up this section.

🏁 We may never be done, but let's move on
==========================================

You could likely spend a whole half day working on just understanding the logs. That is partly because they are interesting, but also partly because logs make it hard to answer the question "how did this request get answered by my system?".

With that in mind, click `Next` and you will get a chance to look at how tracing can help with these types of questions.
