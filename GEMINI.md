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
