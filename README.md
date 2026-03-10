# NL_Railguard_Predictive_Railway_Maintenance_System

# Railway Disruption Predictor

Predictive maintenance system for Dutch railway infrastructure using machine learning to anticipate failures before they happen — shifting NS/ProRail from reactive crisis management to proactive risk prevention.

---

## Problem

The Dutch rail network has recorded **over 60,000 disruptions since 2011**, with ~44% rooted in technical failures (track/signaling). The current maintenance model is either schedule-based or run-to-failure, guaranteeing high-cost emergency interventions. NS has reported a fifth consecutive annual loss, with **€23M in replacement transport costs** alone. With ProRail's renewal budget at €1.8B/year and 400+ infrastructure projects backlogged in 2024, a smarter approach is critical.

---

## Solution

This project applies supervised machine learning to historical disruption logs to:
- **Classify** the root cause category (e.g. Signal Defect, Track Failure)
- **Regress** the estimated delay duration in minutes

---

## Technical Stack

| Component | Choice | Reason |
|---|---|---|
| **Core Model** | LightGBM (Gradient Boosting) | Fast, accurate on large structured/tabular datasets like railway logs |
| **Tasks** | Classification + Regression | Predict cause category & delay duration simultaneously |
| **Evaluation** | F1-Score (0.39) · MAE (189.2 min) | F1 catches rare high-impact events; MAE gives interpretable delay error |
| **Deployment** | Docker Containerization | Stable, isolated — runs on any cloud or internal NS infrastructure |

---

## Metrics

- **F1-Score: 0.39** — correctly surfaces rare, high-impact events (e.g. accidents) that standard accuracy would miss
- **MAE: 189.2 minutes** — average deviation in delay duration estimates

---
## Design Philosophy

**React → Anticipate → Design → Transform**

The project follows a four-stage framework: understanding how disruptions currently unfold reactively, identifying predictable failure patterns in the data, designing a predictive model, and transforming the operational mindset from "fix it when it breaks" to proactive intervention.
