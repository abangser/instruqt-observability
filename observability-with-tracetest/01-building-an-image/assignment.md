---
slug: building-an-image
id: 5yzykftyatdg
type: challenge
title: Building a container image
teaser: Learn how to build an image using a Dockerfile
notes:
- type: text
  contents: |
    # Learn about Docker

    Docker is an open platform for developing, shipping, and running applications.
    Docker enables you to separate your applications from your infrastructure so
    you can deliver software quickly. Containers run anywhere!

    In this first challenge, you'll create a container image. Please wait while we
    boot a virtual machine for you.
tabs:
- title: DockerCompose
  type: terminal
  hostname: docker-vm
- title: Terminal
  type: terminal
  hostname: docker-vm
- title: Editor
  type: code
  hostname: docker-vm
  path: /pokeshop
- title: TraceTest
  type: service
  hostname: docker-vm
  path: /
  port: 11633
- title: Jaeger
  type: service
  hostname: docker-vm
  path: /search
  port: 16686
- title: Pokeshop
  type: service
  hostname: docker-vm
  path: /
  port: 8081
difficulty: basic
timelimit: 600
---

🧪 Build a Docker image
=======================

Use this command to build a Docker image using the Dockerfile in
this directory:

```
docker build -t my-service .
```

💡 Source editor
================

Did you notice the tab with the source code editor, next to
the terminal?

🏁 Finish
=========

To complete the
challenge, press **Check**."
