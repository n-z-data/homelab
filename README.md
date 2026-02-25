# Homelab MiniOps (Raspberry Pi Swarm + Observability + LLM Ops)

A public-facing write-up of a small production-style homelab built on a Raspberry Pi Swarm, with monitoring, alerting, and LLM-assisted ops reporting.

> Internal IPs, secrets, and exact storage paths are intentionally omitted.

## What’s running here
- **Swarm cluster (4× Raspberry Pi)**: manager + workers
- **Observability**: Prometheus + Grafana + exporters
- **DNS resiliency**: redundant Pi-hole instances
- **Data layer**: PostgreSQL + exporter
- **Media services**: Plex + Transmission + encoding worker
- **Automation (ops-runner)**:
  - Agent Host (internal API to local LLMs)
  - Local LLMs: **Mistral + Llama**
  - Agent Runner: scheduled briefs + alert-triggered incident explainers

## Diagrams
- Architecture: `diagrams/architecture.mmd`
- Alert/automation flow: `diagrams/alert-flow.mmd`

## Alerts (noise-controlled)
- Real-time notifications for all alerts (Discord)
- **Email incident explainers only for `severity=critical|high`**

## Why this exists
This lab is designed to practice realistic ops workflows:
- service monitoring and probing
- alert routing with sensible severity
- incident summaries with context
- reproducible documentation and diagrams
