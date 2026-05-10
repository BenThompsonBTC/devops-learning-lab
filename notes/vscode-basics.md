# VS Code Basics

VS Code is a code editor that keeps files, terminal commands, Git changes, and extensions in one place.

## Open Ben's Workspace

From PowerShell:

```powershell
code "C:\Users\Ben Thompson\Documents\Projects\Projects.code-workspace"
```

This opens the main project folders together: DevOps lab, Python automation lab, PowerShell sanitization, GitHub profile, and portfolio lab.

## Main Areas

- Explorer: files and folders on the left.
- Search: find text across projects.
- Source Control: Git changes, commits, sync/push.
- Terminal: run commands without leaving VS Code.
- Extensions: add tools like Python, PowerShell, Docker, and GitHub Actions support.

If VS Code opens to GitLens, Release Notes, or another welcome page, click the Explorer icon at the top-left activity bar. That is the normal file view.

## Terminal

Open a terminal with:

```text
Terminal > New Terminal
```

Use it for commands like:

```powershell
git status
python scripts/system_health_summary.py
```

## Tasks

VS Code tasks are saved commands you can run from the Command Palette.

Open the Command Palette:

```text
Ctrl+Shift+P
```

Then search:

```text
Tasks: Run Task
```

Useful starter tasks have been added:

- `Run system health summary`
- `Run Python tests`
- `Run hello DevOps script`
- `Git status`

## Source Control

The Source Control tab shows changed files.

Always check status before and after changes:

```powershell
git status
```

Basic Git flow:

```powershell
git status
git add .
git commit -m "Describe the change"
git push
```

For portfolio repos, Codex can usually commit and push safe completed work. For private/sanitization work, review first.

## Run Python Scripts

In `python-automation-lab`:

```powershell
python scripts/system_health_summary.py
```

Run tests:

```powershell
$env:PYTHONPATH="src"
python -m pytest
```

## Run PowerShell Scripts

In a PowerShell terminal:

```powershell
.\scripts\hello-devops.ps1
```

If a script came from work, keep it in `powershell-script-sanitization\_raw-private` until sanitized.

## Use Codex Safely

- Start Codex work from inside the repo you want to change.
- Ask Codex to inspect first when unsure.
- Keep raw work data out of public repos.
- Let Codex update README files when a project changes.

## What Not to Commit

Do not commit:

- Passwords, API keys, tokens, certificates, or `.env` files
- Work exports, logs, screenshots, or production data
- Real usernames, emails, domains, tenant IDs, hostnames, IPs, ticket numbers, or internal paths
- Anything from `powershell-script-sanitization\_raw-private`

If unsure, ask Codex to inspect before adding files to Git.
