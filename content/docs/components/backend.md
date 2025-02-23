---
title: Backend
type: docs
prev: /project-architecture
next: /frontend
weight: 20
---

Backend is written in Go. It offers APIs to access images metadata, retrieving them from the database. Its APIs are described using Swagger to guarantee transparency to the frontend.

If you have Go installed you can run it either building from source or using Docker:

{{< tabs items="Source,Docker" defaultIndex="1" >}}

  {{< tab >}}
  Clone the repository
  ```console
  git clone https://github.com/aculei/aculei-be.git
  ```
  
  Ensure to export the necessary environment variables: `GIN_MODE` and `MONGO_URI`.

  Run it
  ```console
  go run main.go
  ```
  {{< /tab >}}

  {{< tab >}}
  Pull the image from the registry
  ```console
  docker pull ghcr.io/aculei/aculei-be:main
  ```

  Run it
  ```console
  docker run --rm -e GIN_MODE=debug -e MONGO_URI=<MONGO_URI> -p 127.0.0.1:<my awesome port here>:8888 aculei-be
  ```
  {{< /tab >}}

{{< /tabs >}}