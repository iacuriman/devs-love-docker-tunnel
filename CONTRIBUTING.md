## Contributing

Thank you for considering contributing to the Dockerized Tunnel Services Monitor! Follow these steps to contribute:

1. **Fork the Repository**

   Fork the repository to your GitHub account.

2. **Create a New Directory for Your Tunnel Service**

   Create a new directory under `tunnels-svc/` named after your service, e.g., `tunnels-svc/cloudflare-tunnel`.

3. **Implement the Basic Monitoring Interface**

   - Follow the UI pattern in `tunnels-svc/ngrook/test-svc/public/index.html`.
   - Ensure consistency in design and functionality.

4. **Provide a Dockerfile**

   - Create a `Dockerfile` within your service's directory.
   - Ensure the service runs efficiently within a Docker container.

5. **Submit a Pull Request**

   Once your service is implemented and tested, submit a pull request for review.

See our [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.