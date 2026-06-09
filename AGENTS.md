# AGENTS.md

Guidance for AI agents working in this repository.

## Project status

**inference-math** is currently a scaffold repository. The only committed project file is `README.md` (title: `# inference-math`). There is no application source code, dependency manifest, tests, lint configuration, or service definitions yet.

## Cursor Cloud specific instructions

### Services

There are no runnable services in this repository. No dev servers, databases, or Docker Compose stacks are defined.

### Dependencies

No package manager lockfile or manifest exists (`package.json`, `pyproject.toml`, etc.). The VM update script is a no-op until dependencies are added to the repo.

### Lint / test / build / run

| Task   | Command | Notes |
|--------|---------|-------|
| Lint   | —       | No linter configured |
| Test   | —       | No test suite |
| Build  | —       | No build system |
| Run    | —       | No application entry point |

When code is added, update this section with the actual commands (and update the VM update script in `.cursor` / cloud agent config to install dependencies).

### Git

Standard git workflow applies. Create feature branches with the `arafatkatze/<name>-dbf3` naming pattern when making changes.

### VM toolchain (available without repo setup)

The cloud VM includes Git, Node.js (via nvm), pnpm, yarn, npm, and Python 3.12. No repo-specific installation is required until manifests are committed.
