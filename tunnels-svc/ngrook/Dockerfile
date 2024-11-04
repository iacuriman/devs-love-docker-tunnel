FROM ubuntu:latest

# Install dependencies
RUN apt-get update && \
    apt-get install -y curl gpg sudo


RUN curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.asc | \
    gpg --dearmor -o /etc/apt/keyrings/ngrok.gpg && \
    echo "deb [signed-by=/etc/apt/keyrings/ngrok.gpg] https://ngrok-agent.s3.amazonaws.com buster main" | \
    tee /etc/apt/sources.list.d/ngrok.list && \
    apt-get update && \
    apt-get install -y ngrok

WORKDIR /app
COPY ngrok.yml /app/ngrok.yml
EXPOSE 4040

CMD ["ngrok", "http", "host.docker.internal:8080", "--config", "/app/ngrok.yml"]