---
slug: getting-to-know-logs
id: 5yzykftyatdg
type: challenge
title: Welcome to Pokeshop
teaser: Explore our shared webapp and how logs can provide insights
notes:
- type: text
  contents: |
    # Exploring Pokeshop

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
- title: Editor
  type: code
  hostname: docker-vm
  path: /pokeshop
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

🤖 First, where am I?
=====================

This first section is an introduction to your workshop environment here in Instruqt.

Instruqt is a completely browser based environment where you will be able to explore and experiment in a safe way without needing to change your personal computers in any way.





👾 Pokeshop, a way to collect them all!
=======================================

Did you notice the tab with the source code editor, next to
the terminal?

🏁 Finish
=========

To complete the
challenge, press **Check**."
