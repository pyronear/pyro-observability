# pyro-observability
Observability platform for edge devices

## Setup

### Prerequisites

- [Docker](https://docs.docker.com/engine/install/)
- [Docker compose](https://docs.docker.com/compose/)

The project was designed so that everything runs with Docker orchestration (standalone virtual environment), so you won't need to install any additional libraries.

### Configuration

In order to run the project, you will need to specific some information, which can be done using a `.env` file.
This file will have to hold the following information:
- `GRAFANA_SECURITY_ADMIN_USER`: the name of the grafana admin
- `GRAFANA_SECURITY_ADMIN_PWD`: the password of the grafana admin

So your `.env` file should look like something similar to:
```
GRAFANA_SECURITY_ADMIN_USER = admin
GRAFANA_SECURITY_ADMIN_PWD = admin 
```

The file should be placed at the root folder of your local copy of the project.

Additionally, you'll need to provide the list of prometheus scrape targets in `prometheus/prometheus.yml`
### Running the service

You can run the service using the following command:

```shell
docker-compose up -d --build
```

## License

Distributed under the Apache 2 License. See [`LICENSE`](LICENSE) for more information.
