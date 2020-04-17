# Bunkr Helm Charts Repository

A Helm chart repository is a location where packaged charts can be stored and
shared.

## Usage

You can start using this Helm chart repository by adding the repository with
the following command:

```sh
$ helm repo add bunkr-charts https://bunkr-io.github.io/bunkr-helm-charts/
```

## How It Works

This repository is served by GitHub Pages.
GitHub allows us to serve static web pages by configuring a project to serve
the contents of its `/docs` directory.

The Helm chart `index.yaml` file is located under the `/docs` directly. It
contains some metadata about the package, including the contnents of a chart's
`Chart.yaml` file. The index file contains information about each chart in the
chart repository.

Individual charts are located at the root of the repository under their own
directories.

### Contributions

1. [Install](https://helm.sh/docs/intro/install/) `helm` CLI
2. Create a new chart with [`helm create`](https://helm.sh/docs/helm/helm_create/):

```sh
$ helm create mychart
```

3. Package a chart with [`helm package`](https://helm.sh/docs/helm/helm_package/):

```sh
$ helm package mychart
```

4. Add a chart to the repository index with [`helm repo add`](https://helm.sh/docs/helm/helm_repo_add/):

```sh
$ helm repo add mychart https://bunkr-io.github.io/bunkr-helm-charts/
```
