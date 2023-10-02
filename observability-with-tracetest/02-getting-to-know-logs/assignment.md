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
timelimit: 2100
---

👾 Pokeshop, a way to collect them all!
=======================================

The website is pretty simple in that it only has a handful of actions users may do:

1. View all Pokemon on the homepage
1. Add a new Pokemon
1. Import an existing Pokemon
1. Remove a Pokemon

We are going to import an existing Pokemon and create a new Pokemon to exercise the system a bit.


📥 Importing an existing Pokemon
================================

To start, we will do the most simple case. Try to import a correct Pokemon.

To do this, click the blue import button and put in a valid Pokemon ID number. Then press OK and wait about 2 or 3 seconds for the new Pokemon to be added to the UI.

> 💡 Hint! As we go through this we will need to import some new Pokemon. There are 1,010 different Pokemon so you can pick a random number within that range, or you can use the Pokedex to look up a specific one!
>
> https://www.pokemon.com/us/pokedex


👹 Next, create a new Pokemon
=============================

Next let's go one step further an see how to create a new one.

Select the blue `Add Pokemon` button and fill in all the fields with valid data. After pressing `OK` you will again see the new pokemon land on the home page after a few seconds 🎉

🧪 OK testers, go be testers!
=============================

If you were kind enough not to immediate try for an edge case, I appreciate you. But now you are set free. Have fun, explore, get to know the behaviours.

✨**_But_**✨ as you do, please continue on to look at the architecture and logs outputs so that your exploring can be in reference to learning more about the inner workings of the application too!

🏛 Pokeshop architecture
========================

What seems simple at first can often have a lot of complexity behind the scenes.

With the user experience you may expect to see a UI, API, and Database. But did you know it also has a queuing system to manage streaming requests?

You can see the full architecture [here](https://docs.tracetest.io/live-examples/pokeshop/overview/#system-architecture).


🪵 Viewing application logs
===========================

If you needed to investigate what is happening in this application you may need to use the logs in one or more services.

To view logs you can go to the new tab called `🔗 Logs` which is a [Dozzle](https://dozzle.dev/) service that gives access to logs of all running Docker containers.

Once in the Logs tab, go ahead and explore to try and find your own actions in the web app displayed in logs.

> 💡 Hint! You can roll over the small coloured dots (🔴🔵) in the top right corner to open a search box for any one stream.

For example, can you import a Pokemon and see how it flows through the architecture?

Spend a few minutes on this before finishing up this section.

🗣 Let's chat
==========================================

How would you like to run automated tests against this application?
What was your experience reading logs?
What else do you wish you could learn from the logs?
