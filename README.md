# Year-End Performance Review

A Codex skill that turns Markdown evidence into a positive, evidence-based year-end self-review. It uses ASD-STE100-informed wording and separates **What** you achieved from **How** you worked.

## What it does

- Asks for your current role, level, responsibilities, and manager expectations.
- Reads Markdown files containing Git history, Jira tickets, appreciation emails, and work notes.
- Connects your contributions to supported results and relevant expectations.
- Distinguishes your contribution from team results and avoids invented metrics.
- Produces plain-text What and How sections with concise bullets.

## Install

Clone this repository into your personal Codex skills directory:

```sh
git clone https://github.com/swaraj89/year-end-performance-review.git "${CODEX_HOME:-$HOME/.codex}/skills/year-end-performance-review"
```

If that folder already exists, use the existing installation or back it up before installing this copy.

## Use

Invoke the skill and provide the paths to your Markdown evidence:

```text
Use $year-end-performance-review to write my year-end review.
Read evidence/commits.md, evidence/tickets.md, and evidence/appreciation.md.
Ask me for my current role and expectations before drafting.
```

You can also supply the review period, company values, performance criteria, and a word limit. Keep personal performance evidence outside this public repository.

The final review follows this structure:

```text
What
- [Your contribution and its supported result.]

How
- [A specific action and its supported benefit.]
```

## Files

- [SKILL.md](SKILL.md): workflow and writing instructions.
- [agents/openai.yaml](agents/openai.yaml): skill display metadata.
- [references/research-notes.md](references/research-notes.md): research sources and rationale.

## Writing approach

The skill adapts clarity principles from ASD-STE100 for performance reviews. It does not include the controlled dictionary or certify full compliance. It is not affiliated with or endorsed by ASD. See the research notes for the official sources.
