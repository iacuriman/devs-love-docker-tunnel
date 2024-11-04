# Dockerized Tunnel Services Monitor

A lightweight, futuristic monitoring dashboard for tunnel services, currently supporting Ngrok. This project provides a containerized solution with a modern UI to help you manage and monitor your tunnel connections.

## Currently Supported Services

- **Ngrok** (reference implementation)

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

1. **Follow the Existing UI Pattern**: Refer to `tunnels-svc/ngrook/test-svc/public/index.html` for UI consistency.
2. **Provide a Dockerfile**: Ensure the service is containerized efficiently.
3. **Include Clear Documentation**: Detail setup, configuration, and usage instructions.
4. **Support Basic Monitoring Features**: Implement features like tunnel status, port information, active connections, and tunnel URLs.

## Prerequisites

- **Docker**: Installed on your machine.
- **Ngrok Account**: Sign up at [ngrok.com](https://ngrok.com) to obtain your authtoken.

## Getting Started

### 1. Clone the Repository

```bash
git clone $REPO_URL
```

### 2. Configure Your Tunnel Service

Navigate to the Ngrok configuration directory and set up `ngrok.yml`:

```yaml
version: "2"
authtoken: YOUR_NGROK_AUTHTOKEN
web_addr: 0.0.0.0:4040
```

*Replace `YOUR_NGROK_AUTHTOKEN` with your actual Ngrok authtoken.*

### 3. Build and Run with Docker Compose

From the root directory, run the following command to build and start the services:

```bash
docker-compose up --build
```

This command will:

- Build the `test-svc` Docker image.
- Build and run the Ngrok container.
- Expose the dashboard on `http://localhost:8080`.
- Expose the Ngrok web interface on `http://localhost:4040`.

## Accessing the Dashboard

Once the containers are up and running:

- **Monitoring Dashboard**: Visit `http://localhost:8080` to view the monitoring dashboard.
- **Ngrok Web Interface**: Visit `http://localhost:4040` to access the Ngrok web interface, which displays the forwarding URLs and connection details.

## Stopping the Services

To stop the Docker containers, press `CTRL+C` in the terminal where Docker Compose is running, or run:

```bash
docker-compose down
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Ngrok](https://ngrok.com) for providing a robust tunneling solution.
- All contributors and future tunnel service implementations.
- [Alpine Linux](https://alpinelinux.org) for the lightweight Docker base image.