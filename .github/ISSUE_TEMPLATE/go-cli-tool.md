---
name: Go CLI Tool Implementation Proposal
about: Propose a new Go CLI tool implementation
title: "Implement Go CLI Tool: "
labels: ""
assignees: ""
---

Let's implement a simple CLI tool in Go that will:
* Be written in the latest version of Go
  * Do not use vendoring
* Be configurable via configuration file. Provide an example, but gitignore the real file.  Don't store sensitive information in this file.
* Have a `.env` file to store sensitive information (ie REDIS_PASSWORD).  Provide an example but gitignore the real file.
* Update the README appropriately
* Include a Makefile and a ci.yaml file, and have a CI badge in the README
* Use Cobra framework