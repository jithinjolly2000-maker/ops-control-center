<div align="center">

# 🧭 Operations Control Center

### Capacity vs demand · actuals vs plan · automation impact, in one view

[![View Live Demo](https://img.shields.io/badge/▶_View_Live_Demo-0b5c6b?style=for-the-badge&logoColor=white)](https://jithinjolly2000-maker.github.io/ops-control-center/)

![Built with](https://img.shields.io/badge/Built_with-Vanilla_JS-f7df1e?style=flat-square&logo=javascript&logoColor=black)
![No dependencies](https://img.shields.io/badge/Dependencies-none-0a7a52?style=flat-square)
![Hosting](https://img.shields.io/badge/Hosted_on-GitHub_Pages-222?style=flat-square&logo=github)
![Data](https://img.shields.io/badge/Data-synthetic_demo-b5841f?style=flat-square)

</div>

---

> ⚠️ **Portfolio demonstration — synthetic data. Nothing here comes from any employer or real system.** Teams, queues, automation agents and every figure are generated in the browser from a fixed seed, so the numbers are the same on every visit. Money is shown in generic currency units (CU).

## ✨ What it shows

The dashboard answers three questions an operations manager asks every week:

| Question | What you see |
|----------|--------------|
| 👥 **Do we have enough people?** | 26 weeks of workload vs capacity hours. Bars are coloured by gap status (Short / Balanced / Surplus, also written as text). A sortable table breaks it down by team and queue: trained and ramping staff, average demand, workload, capacity, gap % and number of short weeks |
| 📈 **How are we doing vs plan?** | Cumulative actual vs plan line chart for tasks automated, hours saved or OPEX avoided, plus a variance table (plan to date, actual, variance, status, full-range plan) |
| 🤖 **What's our automation impact?** | 7 synthetic automation agents with tasks handled, variance to plan, hours saved, cost avoided and automation rate, with totals. Sortable, with an hours-saved bar chart |

KPI cards sit on top (headcount, weeks short of capacity, tasks automated, hours saved, OPEX avoided, automation rate). Team, queue and week-range filters recalculate every section.

## 💡 How it works

It combines four inputs into one view, so a manager can plan capacity, spot gaps and report impact without juggling separate spreadsheets:

- **Team & training data**: trained and ramping headcount per team and queue. New hires ramp for 6 weeks at 50% capacity.
- **Demand plan**: expected tasks per queue per week, with a mid-period peak.
- **Actuals**: task volumes for weeks 1–18, compared with the plan.
- **Automation results**: tasks each agent handled, converted to hours saved (minutes saved per task) and cost avoided (hours × rate).

```text
workload h  = demand plan × handling time − planned automation hours
capacity h  = (trained + 0.5 × ramping) × 32 productive hours
gap %       = (capacity − workload) / workload   → Short < −5%, Surplus > +10%
```

## 💡 Why I built it

I've run a planning and tracking tool like this for an operations team: one place to see staffing
against expected workload, progress against the yearly plan, and the hours automation takes off
the team. This demo rebuilds the idea from scratch with invented teams, queues and agents, so you
can see the method without any confidential data.

## 🧰 Tech

- **Vanilla HTML / CSS / JavaScript**. No frameworks, no build step, no dependencies
- Seeded random generator (mulberry32) for reproducible synthetic data
- Hand-drawn inline SVG charts, each with a text description; the whole app is a single `index.html`
- Labelled controls, keyboard-sortable tables (`aria-sort`), status shown with text, not colour alone
- Hosted free on **GitHub Pages**

## ▶️ Run locally

```bash
start index.html      # Windows — no build step
```

<div align="center">

---

**Built by Jithin J** · [GitHub](https://github.com/jithinjolly2000-maker) · [LinkedIn](https://www.linkedin.com/in/jithin2k)

</div>
