---
description: >-
  Install gitignore.io locally for testing, debugging, and submitting new
  application functionality.
---

# Local Server

### Requirements

* Vapor - [macOS](https://docs.vapor.codes/3.0/install/macos/) / [Ubuntu](https://docs.vapor.codes/3.0/install/ubuntu/)

### Local

```bash
$ git clone --recursive git@github.com:toptal/gitignore.io.git
$ cd gitignore.io/
$ vapor build
$ vapor run
```

### Docker

It’s also possible to run the app using [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/). It can be done by running the commands below.

```bash
$ git clone --recursive git@github.com:toptal/gitignore.io.git
$ cd gitignore.io/
$ docker-compose up -d
```



