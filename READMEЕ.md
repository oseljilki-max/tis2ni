graph TD
    User((Пайдаланушы)) --> Frontend[Frontend: Next.js]
    
    subgraph "Cloud Infrastructure (K8s)"
        Frontend --> API[Backend API: Go]
        API --> DB[(Database)]
        API --> Vault[HashiCorp Vault: Secrets]
    end

    subgraph "Monitoring"
        API -.-> Sentry[Sentry: Error Tracking]
        API -.-> Grafana[Grafana: Metrics]
    end
