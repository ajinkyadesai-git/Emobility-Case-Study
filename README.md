# Mobility Analytics: PRD + Experiment Readout + Model Card

A compact, recruiter-friendly portfolio artifact showing how I take a product problem from **Problem → KPIs → Scope → Solution → Outcome**, plus an **Experiment Readout** and a **Model Card** for a pilot ML use case.

> **Highlights**
> - Delivery uptime increased by **~18%** after instrumenting activation/uptime funnels and aligning cross-functional KPIs.
> - Reporting latency reduced via automated SQL/dbt pipelines and exec-ready dashboards.
> - Pilot ML model (“Delivery Delay Risk”) documented with task, data, metrics, evaluation, and governance notes.

---

## What’s inside

1) **Mini PRD → Launch: Delivery Uptime Analytics (Mobility Project)**  
   - **Problem:** No single source of truth and inconsistent definitions created slow, reactive ops.  
   - **Goal & KPIs:** Improve delivery uptime by 15–20%; guardrails include rider hours, on-time rate, cancellations, and support tickets.  
   - **Scope:** Ship SQL models and Looker dashboards (cohorts, drilldowns), a KPI dictionary, automated refresh, and an exec readout; pilot → iterate → roll out.  
   - **Outcome:** Approx. **+18%** delivery uptime with faster RCA and reduced reporting latency.
   
2) **Experiment / Analytics Readout: Uptime Funnel Instrumentation**  
   - **Hypothesis:** Reliable funnels + daily exception views will speed issue remediation and increase uptime.  
   - **Method:** Baseline vs. post-rollout comparison; daily ops standups; SQL + Looker; KPI dictionary and guardrails.  
   - **Result:** **~+18%** improvement with stable guardrails (no adverse impact on key operations metrics).  
   - **Decision:** Roll out network-wide; add alerting; schedule an A/B test for dispatch rules; evaluate a predictive delay-risk model.
   
3) **Model Card & Evaluation: Delivery Delay Risk (Pilot)**  
   - **Task:** Binary classification to flag high-risk deliveries pre-dispatch for prioritized ops intervention.  
   - **Data & Features:** Trip logs, rider/device telemetry, route/time windows, weather, hour-of-day, and zone features; time-based split.  
   - **Model:** Gradient-boosted trees baseline; threshold tuned for Recall@k on the top-risk decile.  
   - **Metrics (hold-out):** AUC 0.84; F1 0.61; Recall@10% 0.72; Precision@10% 0.58; latency <150 ms.  
   - **Governance:** No PII in training; role-based access; audit logs; monthly drift/fairness checks; batch scoring in GCP.

---

## How to use this repo

- **For recruiters/hiring managers:** Skim the PRD to see how I structure a problem and KPIs; check the Readout to view experiment rigor and decision-making; use the Model Card to assess ML literacy, evaluation discipline, and governance awareness.  
- **For PM/Analyst peers:** Borrow the KPI dictionary/guardrail approach, the experiment readout template, and the model card sections for your projects.

---

## structure 

```
.
├─ README.md
├─ prd/
│  └─ prd_delivery_uptime_onepager.pdf
├─ readout/
│  └─ uptime_experiment_readout.pdf
└─ model-card/
   └─ delivery_delay_risk_model_card.pdf
```


---

## Roadmap / Next steps

- Add alerting thresholds for exception views and SLA drift.  
- A/B test dispatch rules to quantify incremental impact.  
- Explore a predictive delay-risk model feeding exception queues (with cost/run notes and on-call guardrails).

---

## Data & Privacy

This portfolio uses **representative** operational patterns. No PII is included. For production work, I follow role-based access, audit logging, and periodic drift/fairness checks.

---

## Contact

- Portfolio: https://ajinkyadesai-git.github.io  
- LinkedIn: https://www.linkedin.com/in/ajinkyadesai77/  
- GitHub: https://github.com/ajinkyadesai-git
