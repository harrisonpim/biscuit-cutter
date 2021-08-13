# :cookie: Biscuit cutter

This is the rough structure that I've been using for data science projects recently.

The project structure takes some inspiration from [cookie cutter data science](http://drivendata.github.io/cookiecutter-data-science/), but is really based on my own experience of running research projects over the last few years.

With those needs in mind, the structure emphasises reproducibility, collaboration, and code-review. The project is built and orchestrated with docker.

Most of my research begins as a set of jupyter notebooks. This template provides that minimal starting point, using the[jupyter/scipy-notebook](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#jupyter-scipy-notebook) image as a base.

Beyond that stage, I've included some instructions for [scaling research out horizontally or vertically](docs/secondary-containers.md), and making [common config changes](docs/common-config-changes.md).

## Requirements

- docker

## Developing

To build and start the core jupyter service, run

```shell
docker compose up --build project
```
