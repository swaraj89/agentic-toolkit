# Agentic Toolkit

My frequently used skills, plugins, and scripts for working with AI agents.

## Catalog

| Resource | Type | Purpose |
| --- | --- | --- |
| [Year-End Performance Review](skills/year-end-performance-review/SKILL.md) | Codex skill | Turn Markdown evidence into positive, evidence-based What and How bullets with ASD-STE100-informed wording. |

## Structure

- `skills/<skill-name>/`: Self-contained skills, including their references, assets, and skill-specific scripts.
- `plugins/<plugin-name>/`: Authored or customized plugins, each using its required manifest and package layout.
- `scripts/`: Standalone utilities and helpers shared across resources.
- [AGENTS.md](AGENTS.md): Conventions for maintaining this repository.

The plugin and script directories contain `.gitkeep` files so Git tracks them before resources are added. Remove each placeholder when adding content. Keep helpers used by only one skill inside that skill.

## Install a skill

Clone this repository into a location you use for source repositories:

```sh
git clone https://github.com/swaraj89/agentic-toolkit.git
cd agentic-toolkit
```

Copy the desired skill into your personal Codex skills directory. Run these commands from the repository root:

```sh
skill_target="${CODEX_HOME:-$HOME/.codex}/skills"
mkdir -p "$skill_target"
if [ -e "$skill_target/year-end-performance-review" ]; then
  echo 'Skill already exists. Review or back up the existing folder before replacing it.'
else
  cp -R skills/year-end-performance-review "$skill_target/"
fi
```

The installed copy is independent of this checkout. After pulling updates, review the changes and replace the installed copy when ready.

## Year-End Performance Review

The skill asks one question at a time, adapting to your answers and skipping information already supplied. It covers your role, expectations, review purpose, manager priorities, role changes, review dates, and Markdown evidence. After reading the files, it asks targeted questions about missing impact and offers a revision round after the first draft. It accepts Git history, Jira tickets, appreciation emails, and work notes. It distinguishes individual contributions from team results and avoids invented metrics.

```text
Use $year-end-performance-review to write my year-end review.
Read evidence/commits.md, evidence/tickets.md, and evidence/appreciation.md.
Ask me for my current role and expectations before drafting.
```

The final output is plain text with separate What and How bullet lists. You can supply company values, performance criteria, and a word limit.

Its writing style adapts ASD-STE100 clarity principles; it does not include the controlled dictionary or certify full compliance. It is not affiliated with or endorsed by ASD. See the [research notes](skills/year-end-performance-review/references/research-notes.md) for sources.

## Repository scope

Store reusable instructions and tools here. Keep personal performance evidence, credentials, generated output, and installed dependencies outside this public repository.
