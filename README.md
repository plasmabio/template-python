# materials-example

Example repository to create an environment with course materials.

## Structure of the repo

This repository follows the [binder-examples/conda](https://github.com/binder-examples/conda) example very closely.

[`repo2docker`](https://repo2docker.readthedocs.io) is the underlying tool that is used to build an environment from a repository.

`repo2docker` can be configured with several types of files. In the case of this repo:

- `environment.yml`: specify the dependency that will be installed using `conda`
- `postBuild`: specify extra dependencies such as JupyterLab extensions

Once created, the environment can be reused without building it again.

For more information, see the [extensive rep2docker documentation](https://repo2docker.readthedocs.io).

## Materials

Materials can be added anywhere to this repository, either at the top level or in subdirectory.

When building the environment, the materials (and any other file) will be copied to the Docker image.

In this example, there is already a test notebook available under `materials/example.ipynb`.