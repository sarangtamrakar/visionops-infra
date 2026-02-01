Clients
  ↓
FastAPI Gateway (CPU, stateless)
  ↓
Kafka Topics
  ├── inference-requests
  ├── retraining-requests
  ├── metrics-events
  ↓
LangGraph Orchestrator Service (CONTROL PLANE)
  ├── GPU Scheduler Agent
  ├── CV Task Router Agent
  ├── Retraining Decision Agent
  ├── Drift Monitoring Agent
  ↓
Postgres (Locks, GPU state, quotas)
  ↓
Kubernetes / OpenShift API
  ├── spawn GPU inference pods
  ├── spawn retraining jobs
  ├── scale CPU workers
  ↓
Execution Pods (DATA PLANE)
  ↓
MinIO / MLflow / Metrics
