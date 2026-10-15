# Steps by Rito Ghosh

A Quarto site for reproducible, step-by-step setup notes. Its design follows [ritoghosh.com](https://ritoghosh.com/) and [ritoghosh.com/thoughts](https://ritoghosh.com/thoughts/).

## Preview locally

Install [Quarto](https://quarto.org/docs/get-started/) and run:

```bash
quarto preview
```

## Add a guide

Create a directory containing an `index.qmd` file under `steps/`:

```text
steps/
└── my-guide/
    ├── index.qmd
    └── image.png
```

At minimum, include this front matter:

```yaml
---
title: "Guide title"
description: "What this guide sets up."
author: "Rito Ghosh"
date: "YYYY-MM-DD"
categories: [setup]
toc: true
---
```

The listing in `index.qmd` discovers guides automatically.

## Publish

Pushing to `master` triggers [`.github/workflows/publish.yml`](.github/workflows/publish.yml), which renders the project and publishes it to the `gh-pages` branch.

For the current `ritog/steps` remote, the expected project-site URL is:

<https://ritog.github.io/steps/>
