# Traefik

[![Build Status](https://github.com/traefik/traefik/workflows/Main/badge.svg)](https://github.com/traefik/traefik/actions)
[![Go Report Card](https://goreportcard.com/badge/github.com/traefik/traefik)](https://goreportcard.com/report/github.com/traefik/traefik)
[![Documentation](https://img.shields.io/badge/docs-v3.0-blue.svg)](https://doc.traefik.io/traefik/)

Traefik (pronounced _traffic_) is an open-source HTTP reverse proxy and load balancer designed to deploy microservices with ease. It integrates seamlessly with infrastructure components (Docker, Kubernetes, Swarm, Consul, Etcd, ECS) and configures itself automatically and dynamically.

## Core Features

- Dynamic configuration updates without process restarts
- Multiple load balancing algorithms and circuit breakers
- Automatic HTTPS setup via Let's Encrypt / ACME
- Native observability: Metrics (Prometheus, Datadog, StatsD, InfluxDB) and OpenTelemetry integration
- Access logging and distributed tracing (OpenTelemetry, Jaeger, Zipkin)
- Web UI / Dashboard for real-time routing visibility

## Quick Start

Run Traefik with Docker:

```bash
docker run -d -p 8080:8080 -p 80:80 \
  -v /var/run/docker.sock:/var/run/docker.sock \
  traefik:v3.0 --api.insecure=true --providers.docker=true
```

Open `http://localhost:8080/dashboard/` to view the Traefik dashboard.

## Documentation

Detailed guides and technical references can be found at [doc.traefik.io/traefik](https://doc.traefik.io/traefik/).

## License

Traefik is licensed under the [MIT License](LICENSE).