# Tasker
This repo acts as the home for the tasker ecosystem. It is opinionated regarding the layout of its parts, but this approach allows every system to be controlled from a single docker compose. Monitoring via Prometheus and Grafana is also provided. Mocks are supplied for use in local setups as to not hit active services.



## Setup
The following systems need to be setup in the following pattern:
```
/
 - [common](https://github.com/TheFranMan/tasker-common)
 - [gateway](https://github.com/TheFranMan/tasker-gateway)
 - [worker](https://github.com/TheFranMan/tasker-worker)
```

To start all the systems (including monitoring), run `docker compose up -p`

## Monitoring
Monitoring is supplied via Prometheus and using a Grafana dashboard at <a href="http://localhost:3021/" target="_blank">http://localhost:3021/</a>. The username and password are both `admin`. The dashboard can be imported using the file `./data/grafana/dashboard.json`.
