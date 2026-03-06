---
name: Go Service Implementation Proposal
about: Propose a new Go microservice implementation
title: "Implement Go Service: "
labels: ""
assignees: ""
---

Let's implement a simple service in Go that will:
* Be written in the latest version of Go
  * Do not use vendoring
* Have a Dockerfile and Docker Compose file
  * Use the `scratch` image as the runtime
  * The Docker image in the Docker Compose file will be read-only
  * The Redis server will be hosted externally, so no need to include it in the Docker Compose file
* Be configurable via configuration file. Provide an example, but gitignore the real file.  Don't store sensitive information in this file.
* Have a `.env` file to store sensitive information (ie REDIS_PASSWORD).  Provide an example but gitignore the real file.

