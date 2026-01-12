# copilot
Github Copilot &amp; RooCode Configs

## Structure

- [agents/](agents/) — Custom role agents (Markdown)
- [instructions/](instructions/) — Shared base instructions and metric glossary
- [prompts/](prompts/) — Custom prompts
- [skills/](skills/) — Custom skills

## Regenerate agent docs

Agent Markdown files in [agents/](agents/) are kept intentionally slim and reference shared content in [instructions/](instructions/).

- Run: `python3 scripts/refactor_agents.py`
