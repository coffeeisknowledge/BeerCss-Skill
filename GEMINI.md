# Project Context & Rules

## Git Standards (Commitizen)
**MANDATORY:** All commits must follow the Conventional Commits specification.
Do NOT use the interactive `cz` tool. Generate the message string directly using the format below.

**Format:** `type(scope): subject`

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation
- `style`: Formatting (missing semi colons, etc)
- `refactor`: No bug fix, no new feature
- `test`: Adding tests
- `chore`: Maintainance (build, configs, beads)

**Example:**
User: "Ya configuré beads."
Assistant: `git commit -m "chore(beads): initialize project structure and database"`

## Agent Behavior
- Check `beads` state before starting work.
- Always close the relevant `beads` task after a successful commit.

## Project Structure & Scope
- **Development Root:** All skill-related files (SKILL.md, assets/, references/) MUST be developed and maintained within the `beercss/` directory.
- **Referenceability:** This structure ensures the skill can be easily referenced or moved to `.gemini/skills/` in the future.

## Source of Truth & Documentation
- **Mandatory Source:** The `beercss/docs/` directory contains the source of truth for all BeerCSS components, helpers, and patterns.
- **Verification Protocol:** BEFORE implementing or documenting any component in the SuperSkill, you MUST read its corresponding file in `beercss/docs/` (e.g., read `beercss/docs/BUTTON.md` before working on button patterns).
- **Beer Purity Law:** Strictly adhere to the "3 ingredients" philosophy (Settings, Elements, Helpers) as described in `docs/INDEX.md`.
- **No Hallucinations:** If a pattern or class is not documented in `docs/`, do not assume it exists. Use only established BeerCSS conventions found in the documentation.

## Git Standards (Commitizen)
**MANDATORY:** All commits must follow the Conventional Commits specification.
Do NOT use the interactive `cz` tool. Generate the message string directly using the format below.

**Format:** `type(scope): subject`

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation
- `style`: Formatting (missing semi colons, etc)
- `refactor`: No bug fix, no new feature
- `test`: Adding tests
- `chore`: Maintainance (build, configs, beads)

**Example:**
User: "Ya configuré beads."
Assistant: `git commit -m "chore(beads): initialize project structure and database"`

## Agent Behavior
- Check `beads` state before starting work.
- Always close the relevant `beads` task after a successful commit.
