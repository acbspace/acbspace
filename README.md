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

An enterprise workflow intelligence platform that consolidates activity from
developer and collaboration tools into a prioritized operational dashboard.

- Aggregates tasks and events from distributed enterprise tools
- Identifies pending work, blockers, and ownership gaps
- Generates actionable summaries using AI-assisted workflows
- Designed around event-driven services and observable infrastructure

**Tech:** `Go` `React` `Kafka` `PostgreSQL` `Docker` `Kubernetes` `OpenTelemetry`

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

### 🏆 [Study Helper](https://github.com/acbspace/study-helper-app)

A cross-platform study-tracking application that combines focus tools,
social accountability, and competitive seasonal study leagues.

- Focus timer with subject-level study tracking
- Daily, weekly, and monthly productivity analytics
- Study groups and real-time rankings
- Seasonal leagues, divisions, promotions, and leaderboards

**Tech:** `React Native` `Expo` `TypeScript` `FastAPI` `PostgreSQL` `WebSocket`

---

### 🐾 Pet Friend

A mobile app that tracks a pet's entire life in one place — health and
vaccination records, vet appointments, photos, and a start-to-finish timeline.

- Pet profiles with health, vaccination, and medication history
- Vet appointment calendar with Google Calendar sync
- Photo and document storage for records
- Life-story timeline from adoption onward
- Cross-platform mobile experience

**Tech:** `React Native` `Expo` `TypeScript` `Supabase` `PostgreSQL`
