<p align="center">
  <img src="https://raw.githubusercontent.com/traefik/traefik/v3.0/docs/content/assets/img/traefik.logo.png" alt="Traefik" width="450">
</p>

# Traefik

Traefik (pronounced _traffic_) is a modern HTTP reverse proxy and load balancer that makes deploying microservices easy.
Traefik integrates with your existing infrastructure components (Docker, Swarm mode, Kubernetes, Consul, Etcd, Amazon ECS, ...) and configures itself automatically and dynamically.

## Quick Start

Run Traefik using Docker:

```bash
docker run -d -p 8080:8080 -p 80:80 \
  -v /var/run/docker.sock:/var/run/docker.sock:ro \
  traefik:v3.0 --api.insecure=true --providers.docker
```

> **Note:** Mounting `/var/run/docker.sock` in read-only mode (`:ro`) is recommended for enhanced security.

Open `http://localhost:8080` in your browser to access the Traefik dashboard.

## Documentation

The complete documentation is available at [docs.traefik.io](https://docs.traefik.io).

## Contributing

Please refer to [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on contributing to Traefik.

## License

Traefik is released under the MIT License. See [LICENSE](LICENSE) for details.