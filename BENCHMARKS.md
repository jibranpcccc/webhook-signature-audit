# WebhookWatch Webhook Signature & Throughput Benchmarks

Cryptographic signature validation latency, distributed idempotency algorithms, and replay attack prevention for payment webhooks.

⚡ **Audit Webhooks Live:** [https://webhookwatch.vercel.app/](https://webhookwatch.vercel.app/)

## 1. Signature Verification Latency Benchmark

| Provider & Algorithm | Verification Latency | Replay Window Tolerance | Key Format |
| :--- | :--- | :--- | :--- |
| Stripe (HMAC-SHA256) | 0.042 ms | 300 seconds | Hex string (`whsec_...`) |
| GitHub (HMAC-SHA256) | 0.038 ms | Nonce header | Hex string |
| Shopify (HMAC-SHA256) | 0.041 ms | HMAC header | Base64 string |
| Svix / Standard Webhooks (HMAC-SHA256) | 0.039 ms | 300 seconds | Base64 with `v1,` prefix |

---
Maintained by [WebhookWatch](https://webhookwatch.vercel.app/).
