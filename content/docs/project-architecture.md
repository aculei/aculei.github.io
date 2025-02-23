---
title: Project architecture
type: docs
prev: /
next: /backend
weight: 1
---

![excali](excali.webp)
Edit or view the graph on Excalidraw using this [link](https://excalidraw.com/#json=GxDjAVUbDxEkcGvkSiGgS,boJAltwlmd8-sxRH5KnO3g).

Aculei project is divided into three components: the [backend](components/backend), the [frontend](components/frontend) and the [image classification](components/ai) module.

## Cloudflare buckets
Cloudflare buckets are used to efficiently store images. The database only stores the URI of a given image. When backend is requested to return a set of images it retrieves metadata from the database and produces images' URI . The frontend can retrieve images from cloudflare buckets using the URI provided by the backend.

## MongoDB
The database is hosted as free-tier MongoDB Atlas instance. This allow room for experiments and a lot of flexibily during development and testing.