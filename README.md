# Cloud Telemetry Service (Python 3.11)

FastAPI-powered asynchronous microservice that ingests telemetry streams from core engines and routes batches to AWS SQS and S3 data lakes.

## Features
- **Async High-Throughput Ingestion**: Validates batches using Pydantic v2 schemas.
- **Adaptive SQS Dispatcher**: Automatic backoff when queues encounter throttling.
- **Docker Multi-Stage Build**: Secure distroless image deployment.

## Running Locally
```bash
poetry install
poetry run uvicorn app.main:app --reload --port 8000
```
