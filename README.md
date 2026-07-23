# Hi, I'm Andy 👋

I'm a software engineer with a background in finance.

## 🚀 Featured Projects

### 📈 [Algorithmic Trading System](https://github.com/acbspace/algo-trading-system)

A polyglot research-to-execution trading platform: Rust microservices on a NATS
bus handle the order/tick hot path, Python owns research, and a React dashboard
streams live state.

- Guaranteed sim/live parity — the backtest engine and live execution share the same compiled order-sizing kernel; a CI parity harness enforces it
- Built a research funnel with a real gate: OpenBB→TimescaleDB ingest, Rayon-parallel parameter sweeps, walk-forward validation with an overfitting t-test, then Zipline simulation with realistic costs and Alphalens/Pyfolio approval reports
- Implemented an automated risk engine (CVaR / max-drawdown) with a kill-switch the execution engine honors, plus Prometheus/Grafana observability
- Designed 9 Rust crates separating market data, sizing, execution, risk, and the read-only web gateway; Interactive Brokers integration behind a broker trait with a deterministic paper broker for CI

**Tech:** `Rust` `Python` `TypeScript` `NATS` `Protobuf` `TimescaleDB` `PyO3` `VectorBT` `Zipline` `IBKR API` `Docker` `Kubernetes` `Prometheus`

---

### 🛰️ [Sentinel Flow](https://github.com/acbspace/sentinel-flow-project)

An event-driven incident detection and remediation platform that turns raw
service telemetry into detected, correlated, and auto-resolved incidents —
inspired by Datadog and PagerDuty.

- Ingests high-volume service telemetry over HTTP and streams it through Kafka
  with at-least-once delivery and event-level idempotency
- Correlates related signals into deduplicated, prioritized incidents in real time
- Routes alerts through on-call schedules and escalation policies backed by
  durable Temporal workflows
- Executes guarded automated remediation with approval gates and a full audit trail
- Surfaces live incident state and service health in a real-time React dashboard
- Runs on Kubernetes, instrumented end-to-end with OpenTelemetry — distributed
  tracing across HTTP and Kafka, metrics, and structured logs

**Tech:** `Go` `React` `Kafka` `PostgreSQL` `Docker` `Kubernetes` `OpenTelemetry` `Temporal`
<sub>Kafka, Kubernetes for learning purpose</sub>

---

### 📊 [Signal Ledger](https://github.com/acbspace/signal-ledger)

An auditable research-to-backtest platform that turns analyst PDFs into
page-cited claims, and claims into reproducible paper backtests.

- Extracts page-cited, evidence-gated claims from research PDFs (heuristic or LLM)
- Human accept/reject review; strategies must cite accepted claims
- Immutable strategy versions over checksummed market-data snapshots
- Deterministic, point-in-time backtests — identical inputs reproduce identical results

**Tech:** `Go` `Python` `FastAPI` `PostgreSQL` `Docker`

---

### 🏆 [Study League](https://github.com/acbspace/study-helper-app)

A cross-platform study-productivity app that turns focused study into visible,
fair progress — combining focus tools, social accountability, and competitive
seasonal leagues that reward consistency over raw hours.

- Offline-first focus timer with subject-level tracking that survives backgrounding, force-quit, and device restart
- Productivity analytics — daily, weekly, and monthly breakdowns with streaks, goal completion, and verified-vs-manual study time
- Study groups and live presence — see who's studying in real time, with group leaderboards and encouragement
- Seasonal leagues — divisions, cohorts, promotions/relegations, weekly missions, and League Points that reward goal completion and consistency, not burnout

**Tech:** `React Native` `Expo` `TypeScript` `FastAPI` `PostgreSQL` `Redis` `WebSocket`

---

### 🐾 [Pet Friend](https://github.com/acbspace/pet-friend-app)

A mobile app that tracks a pet's entire life in one place — health and
vaccination records, vet appointments, photos, and a start-to-finish timeline.

- Pet profiles with health, vaccination, and medication history
- Vet appointment calendar with Google Calendar sync
- Photo and document storage for records
- Life-story timeline from adoption onward
- Cross-platform mobile experience

**Tech:** `React Native` `Expo` `TypeScript` `Supabase` `PostgreSQL`
