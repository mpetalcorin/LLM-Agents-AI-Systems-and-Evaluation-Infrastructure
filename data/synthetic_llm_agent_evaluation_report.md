# Synthetic LLM Agent Evaluation Report

## Executive summary

- Best overall success rate: **Reflect** at **30.1%**.
- Lowest mean latency: **Direct** at **31.1 seconds**.
- Best calibration by ECE: **ReAct** with **ECE=0.037**.

## Interpretation

Structured agents generally improved success on tool-heavy and long-horizon tasks, but they also increased latency and synthetic cost. This reproduces a common AI-systems engineering trade-off: more scaffolding improves reliability but consumes more compute and orchestration time.

## Recommended next experiments

1. Add caching and tool-result reuse to reduce latency.
2. Add schema-aware retry logic for invalid tool calls.
3. Use automatic failure clustering to identify repeated prompt/tool bugs.
4. Add held-out adversarial tasks to improve robustness evaluation.
5. Add cost-aware routing, so simple tasks use cheap direct prompting and hard tasks use full agent scaffolding.