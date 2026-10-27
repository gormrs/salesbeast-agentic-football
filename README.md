# SalesBeast — Agentic Football Cup

Our team for the [AWS Agentic Football Cup](https://agenticfootballcup.com/):
five Strands agents on Amazon Bedrock AgentCore, each controlling one player in a
5v5 match.

- **[`salesbeast-team/`](salesbeast-team/)** — our team. Same structure as the AWS
  balanced team, with prompts and models tuned from public write-ups of the cup.
  See its README for the changes and sources.
- `lib/` — shared code every team uses (state summary, parsing, fallback).
- `ai-team-strands-*` — the AWS sample teams, kept for reference and benchmarking.

Based on [aws-samples/sample-ai-possibilities](https://github.com/aws-samples/sample-ai-possibilities)
(`agentic-football-sample-agents`), MIT-0.

## Quick start

```bash
python3 -m venv .venv && source .venv/bin/activate   # Python 3.10+
pip install -r salesbeast-team/ai-gk/requirements.txt
cd salesbeast-team
python3 ai-gk/test_local.py          # local test, no AWS needed
python deploy_all.py                 # deploy (needs AWS credentials, Node, AgentCore CLI, CDK)
```
