# Helmora Agents installers

Public bootstrap scripts for [Helmora Agents](https://github.com/Helmora-AI/HelmoraAgent).

This repository contains only the two installer entry points, so the desktop app can
fetch them without needing access to the full source checkout.

```text
scripts/install.ps1   Windows (PowerShell 5.1+)
scripts/install.sh    macOS / Linux
```

Both scripts clone `Helmora-AI/HelmoraAgent`, create the Python environment, and run
the staged install. They are copied from the main repository's `scripts/` directory;
update them there first, then sync this repository.

Windows:

```powershell
irm https://raw.githubusercontent.com/Helmora-AI/HelmoraAgents/main/scripts/install.ps1 | iex
```

macOS / Linux:

```bash
curl -fsSL https://raw.githubusercontent.com/Helmora-AI/HelmoraAgents/main/scripts/install.sh | bash
```

The target checkout can be overridden with `HELMORA_REPO_URL` (or `HERMES_REPO_URL`).

MIT licensed; see `LICENSE`.
