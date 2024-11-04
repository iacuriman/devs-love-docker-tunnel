# Dockerized Tunnel Services Monitor

A lightweight, futuristic monitoring dashboard for tunnel services, currently supporting ngrok. This project provides a containerized solution with a modern UI to help you manage and monitor your tunnel connections.

## Currently Supported Services
- ngrok (reference implementation)

## Looking for Contributors! 🚀

We're actively seeking contributors to help expand support for other tunnel services, such as:

- Cloudflare Tunnel
- LocalTunnel
- Pagekite
- Telebit
- Serveo
- Localtunnel.me
- Expose

Each new tunnel service implementation should:
1. Follow the existing UI pattern (reference tunnels-svc/ngrook/test-svc/public/index.html)
2. Provide a Dockerfile for containerization
3. Include clear documentation
4. Support basic monitoring features

## Prerequisites

- Docker installed on your machine
- Account with your preferred tunnel service

## Getting Started

1. Clone this repository
2. Configure your tunnel service (see service-specific README in each directory)
3. Build and run with Docker Compose: