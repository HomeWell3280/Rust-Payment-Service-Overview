## Rust Payment Service Overview

A performant Rust service handling split-payouts via Stripe Treasury, built on Actix Web with:
- **Rust 1.78**
- **Tokio** runtime for async concurrency
- **SQLx** + **PostgreSQL** for persistence
- **Stripe-Rust** SDK for payment rails
- **Tracing** + **Prometheus** metrics
- **Dotenv** for config

### Requirements
- Rust ≥1.78 (with `cargo`)
- PostgreSQL (≥12)
- Docker (optional)
- `.env` file in `services/payment_service`:
  ```dotenv
  DATABASE_URL=postgres://user:pass@localhost/payments
  STRIPE_API_KEY=sk_test_XXX
  SERVICE_NAME=payment_service
  BIND_ADDR=0.0.0.0:8082

  # HomeWell Microservices

This repo delivers Post-LOS operational microservices:
- **common**: shared config & types (Rust and Python interop)
- **user_service** & **booking_service**: Python/FastAPI
- **payment_service**: Rust/Tokio/Actix for high-throughput, memory-safety & low latency payments
