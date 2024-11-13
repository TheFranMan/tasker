# Tasker
This repository hosts the Tasker Ecosystem, designed for easy orchestration and monitoring across systems using Docker Compose. It provides a consistent and streamlined structure, with built-in monitoring via Prometheus and Grafana. For local development, it includes mock services to avoid impacting live systems.


## Setup
To set up the Tasker ecosystem, start by cloning each of the following repositories in the specified directory structure:

plaintext
Copy code
/
 ├── [common](https://github.com/TheFranMan/tasker-common)
 ├── [gateway](https://github.com/TheFranMan/tasker-gateway)
 └── [worker](https://github.com/TheFranMan/tasker-worker)
Steps
Clone Repositories: Clone each repository into the root directory as shown.

Start Services: Once the structure is set up, navigate to the root directory and start all systems, including monitoring, by running:

bash
Copy code
docker compose up
This will launch the core services and monitoring systems.

## Monitoring
Monitoring is provided via Prometheus for metrics collection and Grafana for visualization. You can access the Grafana dashboard at http://localhost:3021/. The default login credentials are admin for both the username and password (consider updating these in production environments).

To set up the dashboard:

Import the pre-configured Grafana dashboard from the file located at ./data/grafana/dashboard.json.
