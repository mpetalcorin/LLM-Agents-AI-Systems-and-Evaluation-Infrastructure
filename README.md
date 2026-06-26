# LLM Agents, AI Systems, and Evaluation Infrastructure

This repository contains a notebook that simulates and evaluates LLM-agent research workflows using benchmark-inspired synthetic datasets. It demonstrates Python research engineering, agent evaluation, AI-systems analysis, reproducible experimentation, statistical testing, and visual reporting.
<img width="1536" height="1024" alt="LLM AGENTS AI SYSTEMS" src="https://github.com/user-attachments/assets/315b8e3d-f7fb-4f3b-90c8-7e61351b5fba" />
## What this project demonstrates

- LLM-agent workflow simulation
- Direct LLM, chain-of-thought-style, ReAct-style, tool-router, memory, and self-reflecting agent comparisons
- Benchmark-inspired task families:
  - Retrieval question answering
  - Fact verification
  - Interactive web-style decision tasks
  - Embodied-planning-style sequential tasks
  - Tool/API use
  - Code-patch evaluation
  - Safety/policy evaluation
- Multi-metric evaluation:
  - Success rate
  - pass@1
  - Hallucination rate
  - Invalid tool-call rate
  - Timeout rate
  - Latency
  - Token use
  - Synthetic cost
  - Calibration
  - Robustness
  - Failure-mode decomposition
- Bootstrap confidence intervals
- Fisher exact tests
- Failure-triage logistic regression
- Reproducible CSV outputs and publication-style figures

## Data provenance

All datasets are **synthetic** and generated for portfolio demonstration only. The simulated values are calibrated around qualitative trends and broad ranges from standard public LLM-agent and LLM-evaluation literature, including ReAct, HELM, ToolBench/StableToolBench, and SWE-bench. This repository does **not** reproduce proprietary Meta data or claim exact leaderboard replication.

## Repository structure

```text
.
├── LLM_Agents_AI_Systems_Evaluation_Infrastructure.ipynb
├── data/
│   ├── synthetic_llm_agent_runs.csv
│   ├── task_family_metadata.csv
│   ├── agent_variant_metadata.csv
│   ├── agent_summary_metrics.csv
│   ├── bootstrap_success_ci.csv
│   ├── direct_vs_reflect_fisher_tests.csv
│   └── synthetic_llm_agent_evaluation_report.md
└── figures/
    ├── 01_overall_success_rate.png
    ├── 02_task_agent_heatmap.png
    ├── 03_bootstrap_ci.png
    ├── 04_failure_modes.png
    ├── 05_cost_latency_tradeoff.png
    ├── 06_calibration_curves.png
    ├── 07_robustness_drop_heatmap.png
    ├── 08_ablation_gain_heatmap.png
    ├── 09_failure_triage_coefficients.png
    └── 10_confusion_matrix.png
```

## How to run

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook LLM_Agents_AI_Systems_Evaluation_Infrastructure.ipynb
```

## Key message

This project shows how to turn an AI-research idea into a reproducible engineering workflow: generate tasks, run agent variants, measure performance, diagnose failures, quantify uncertainty, and communicate results clearly.

## References

- Yao et al., ReAct: Synergizing Reasoning and Acting in Language Models.
- Bommasani et al., Holistic Evaluation of Language Models.
- Qin et al., ToolLLM / ToolBench.
- StableToolBench.
- Jimenez et al., SWE-bench.
