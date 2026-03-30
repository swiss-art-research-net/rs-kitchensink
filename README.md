# ResearchSpace Kitchen Sink

This is a sample ResearchSpace app for testing and development purposes.

## Usage

Clone the repository and start the services with Docker Compose:

```bash
dcker compose up -d
```

## Customisation

The Docker Compose configuration contains defaults for the ResearchSpace image as well as for the port mapping. In order to change them, add a `.env` file to the project. The following variables are supported:

- `PLATFORM_IMAGE`: The Docker image to use for the ResearchSpace platform. Default is `swissartresearx/researchspace:e891b3ca8358ff85c6a5e6e8cfbb870155a7d804`.
- `PORT_PLATFORM`: The port on the host to map to the ResearchSpace platform. Default is `8081`.
- `PORT_BLAZEGRAPH`: The port on the host to map to the Blazegraph SPARQL endpoint. Default is `8082`.

Alternatively, specify the variables before the `docker compose` command:

```bash
PLATFORM_IMAGE=researchspace/platform-ci:latest docker compose up -d
```