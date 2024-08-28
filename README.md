# dataFactory local deployment

This repository intend to manage files used to quickly deploy a development environment on a local computer.

## Requirements

- Docker >= 23.0.6
- Docker compose >= 2.17.3

For more information on how to install and configure docker & docker compose, please refer to the [official documentation](https://docs.docker.com/engine/install/).

## Usage

Clone this repository, then execute the following commands in the created folder :

```bash
docker login quay.io # NOTE: use credentials provided by dFakto support
docker compose up -d
```