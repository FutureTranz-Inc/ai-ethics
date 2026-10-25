# AGENTS Guide for `ai-ethics`

This file gives coding agents a repository-specific operating manual.
Use these rules to make safe, consistent changes that pass local and CI checks.

## Repository Snapshot

- Primary language: Python (standard library only) in `src/ai_ethics_enforcer.py`.
- Supporting automation: Bash scripts under `scripts/` and `scripts/hooks/`.
- Policy/config assets: Markdown and YAML in repo root and `docs/`.
- CI workflows: `.github/workflows/*.yml`.
- No package manifest like `package.json` or `pyproject.toml` is currently present.

## Source of Truth

- Project overview and usage examples: `README.md`.
- Contribution workflow: `CONTRIBUTING.md`.
- Attribution enforcement policy: `AI_ATTRIBUTION_POLICY.md`.
- CI behavior: `.github/workflows/ci.yml` and `.github/workflows/attribution-policy.yml`.

## Build, Lint, and Test Commands

Run from repository root.

### Environment Setup

- Create virtual environment: `python3 -m venv venv`
- Activate environment (macOS/Linux): `source venv/bin/activate`
- Install Python dependencies: `pip install -r requirements.txt`

### Linting

- Markdown lint (same tool family used in CI): `markdownlint '**/*.md' --ignore node_modules`
- YAML lint: `yamllint **/*.yml **/*.yaml --ignore=node_modules`
- Shell syntax check for all scripts: `find scripts -name "*.sh" -exec bash -n {} \;`
- YAML parse check used in CI: `python3 -c "import yaml; [yaml.safe_load(open(f)) for f in ['ethics-checklist.yml']]"`

### Test / Validation Commands

- Run attribution policy commit check: `bash scripts/ci-check-attribution.sh`
- Run enforcer against one file: `python3 src/ai_ethics_enforcer.py --type file path/to/file --format json`
- Check one commit: `python3 src/ai_ethics_enforcer.py --type commit HEAD`
- Check commit message content from stdin:
  `printf 'Subject\n\nBody' | python3 src/ai_ethics_enforcer.py --type content -`

### Single-Test Equivalents (Most Useful)

- Single shell script syntax test:
  `bash -n scripts/install-attribution-policy.sh`
- Single workflow syntax sanity (YAML parse):
  `python3 -c "import yaml; yaml.safe_load(open('.github/workflows/ci.yml'))"`
- Single file ethics enforcement test:
  `python3 src/ai_ethics_enforcer.py --type file src/ai_ethics_enforcer.py`

## CI Expectations to Match Locally

- CI lints Markdown and YAML.
- CI validates shell syntax for files in `scripts/`.
- CI runs attribution policy checks on commit messages.
- CI may enforce PRD ethics section requirements in targeted PRs.
- Before opening PRs, run lint + policy checks locally to avoid churn.

## Code Style Guidelines

Follow existing style in each file you touch.
When conventions conflict, match nearby code and keep diffs minimal.

### Python (`src/`)

- Imports are currently grouped in one block; preserve readability and avoid unused imports.
- Prefer standard library only unless explicitly requested (current project has no external runtime deps).
- Use type hints for function signatures where already present.
- Keep class and function docstrings concise and behavior-oriented.
- Use dataclasses/enums consistently with existing patterns when extending violation models.
- Keep line-level logic simple and explicit; avoid clever one-liners for policy checks.
- Favor pure helper methods for reusable checks (`_is_*` patterns are already used).

### Formatting and Structure

- Use 4 spaces for Python indentation.
- Keep shell indentation consistent with existing script style (4 spaces in many scripts).
- Keep Markdown headings descriptive and hierarchy consistent.
- Keep YAML keys lowercase snake_case (matches `ethics-checklist.yml`).

### Naming Conventions

- Python classes: `PascalCase` (`AIEthicsEnforcer`, `Violation`).
- Python functions/methods/variables: `snake_case`.
- Constants in shell scripts: `UPPER_SNAKE_CASE` (for color vars and counters).
- Script filenames: kebab-case (for installer/check scripts) or established names; do not rename casually.

### Error Handling and Exit Behavior

- Shell scripts should fail fast with `set -e` where already used.
- Return non-zero exits for policy violations; do not silently ignore failures.
- In Python CLI paths, preserve existing `sys.exit(0|1)` contract.
- Catch expected exceptions narrowly (for file IO, subprocess, decode errors) and provide actionable messages.
- Do not suppress validation errors that are part of policy enforcement.

### Logging and Output

- Keep CLI and script output user-actionable (what failed + how to fix).
- Prefer concise status lines with clear pass/fail indicators.
- Avoid adding excessive verbosity in hooks or CI scripts.

## Policy-Specific Rules for This Repository

- Human-only authorship is mandatory; never add AI attribution lines.
- Do not add banned phrases like `Generated with ...` or AI co-author metadata.
- Preserve references to human contributors and existing legal/policy framing.
- If editing policy docs or hooks, maintain alignment with `AI_ATTRIBUTION_POLICY.md`.

## File-Specific Guidance

- `src/ai_ethics_enforcer.py`: core logic; keep behavior deterministic and testable.
- `scripts/hooks/commit-msg`: validates commit messages via Python enforcer.
- `scripts/hooks/pre-commit`: validates staged files.
- `scripts/ci-check-attribution.sh`: CI guardrail for commit history.
- `.github/workflows/*.yml`: treat as enforcement contracts; avoid casual drift.

## Agent Starter Files

Root starters for copying into other projects: `CLAUDE.md`, `GEMINI.md`, `GPT.md`, `COPILOT.md`, `CURSOR.md`, `GROK.md`.
The index is `docs/AGENT_INTEGRATION.md`. Keep those files aligned with `AI_ATTRIBUTION_POLICY.md`.

## Cursor and Copilot Rule Files

- `.cursorrules`: not found.
- `.cursor/rules/`: not found.
- `.github/copilot-instructions.md`: not found.

If these files are added later, update this `AGENTS.md` and treat those rule files as higher-priority agent guidance for editor-specific behavior.

## Safe Change Workflow for Agents

1. Read the target file and nearby related files first.
2. Make minimal, scoped edits that match local conventions.
3. Run the narrowest relevant single-test command first.
4. Run broader lint/policy checks if changes touch shared paths.
5. Keep commit messages human-authored and policy-compliant.

## Common Pitfalls to Avoid

- Do not assume npm-based project tasks exist; this repo is not Node-packaged.
- Do not introduce new dependencies without explicit request.
- Do not weaken hook/CI checks to make failing content pass.
- Do not rewrite large docs/scripts when a focused patch is enough.
- Do not add AI attribution statements to code, docs, PR text, or commits.

## Quick Command Checklist

- `python3 src/ai_ethics_enforcer.py --type file src/ai_ethics_enforcer.py`
- `bash -n scripts/ci-check-attribution.sh`
- `markdownlint '**/*.md' --ignore node_modules`
- `yamllint **/*.yml **/*.yaml --ignore=node_modules`
- `bash scripts/ci-check-attribution.sh`

Keep changes small, verifiable, and aligned with policy enforcement goals.
