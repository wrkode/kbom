# KBOM - Kubernetes Bill of Materials

![GitHub release (latest by date)](https://img.shields.io/github/v/release/ksoclabs/kbom)
![Hex.pm](https://img.shields.io/hexpm/l/apa)
[![Go Report Card](https://goreportcard.com/badge/github.com/ksoclabs/kbom)](https://goreportcard.com/report/github.com/ksoclabs/kbom)
[![FOSSA Status](https://app.fossa.com/api/projects/custom%2B37386%2Fgithub.com%2Fksoclabs%2Fkbom.svg?type=shield)](https://app.fossa.com/projects/custom%2B37386%2Fgithub.com%2Fksoclabs%2Fkbom?ref=badge_shield)
[![OpenSSF Best Practices](https://bestpractices.coreinfrastructure.org/projects/7273/badge)](https://bestpractices.coreinfrastructure.org/projects/7273)

The Kubernetes Bill of Materials (KBOM) standard provides insight into container orchestration tools widely used across the industry.

As a first draft, we have created a rough specification which should fall in line with other Bill of Materials (BOM) standards.

The KBOM project provides an initial specification in JSON and has been constructed for extensibilty across various cloud service providers (CSPs) as well as DIY Kubernetes.

## Getting Started

### Installation

```sh
brew install ksoclabs/homebrew-kbom/kbom
```

or

```sh
make build
```

### Usage

`KBOM generate` generates a KBOM file for your Kubernetes cluster

```sh
kbom generate [flags]
```

Optional flags include:

```plain
  -f, --format string     Format (json, yaml) (default "json")
  -h, --help              Help for generate
  -p, --out-path string   Path to write KBOM file to. Works only with --output=file (default ".")
  -o, --output string     Output (stdout, file) (default "stdout")
      --short             Short - only include metadata, nodes, images and resources counters
```

## Schema

The high level object model can be found [here](docs/schema.md).

## Supported Kubernetes Versions

We have tested *kbom* with all versions newer than *v1.19*, and can confirm that it is fully compatible with each of these versions. This means that you can use our tool with confidence, knowing that it has been thoroughly tested with.

## Supported Cloud Providers

We have tested our tool with all of the main cloud providers, including `Azure`, `AWS`, and `Google Cloud`. Of course it's possible to generate `kbom` file for any K8s cluster, but please have in mind that in some cases not all metadata entries will be set.

## Contributing

KBOM is Apache 2.0 licensed and accepts contributions via GitHub pull requests. See the [CONTRIBUTING](CONTRIBUTING.md) file for details.
