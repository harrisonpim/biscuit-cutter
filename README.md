# :cookie: Biscuit cutter

This is the rough structure that I've been using for starting data science projects recently.

The project structure takes some inspiration from [cookiecutter data science](http://drivendata.github.io/cookiecutter-data-science/), but is really based on my own experience of running research projects over the last few years. With those needs in mind, the structure emphasises reproducibility, collaboration, and code-review.

Most of my research begins as a set of jupyter notebooks. This template provides that minimal starting point, orchestrated with docker, and using the [jupyter/scipy-notebook](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#jupyter-scipy-notebook) image as a base.

Beyond that point, I've included:

- instructions for [scaling research out horizontally or vertically](docs/secondary-containers.md)
- instructions for making [common config changes](docs/common-config-changes.md)
- a couple of [non-essential recommendations](docs/recommendations.md)

I'll try to keep this repo up to date as my own workflow develops.

## Requirements

- docker

## Getting started

[See the instructions](/docs/getting-started.md)
