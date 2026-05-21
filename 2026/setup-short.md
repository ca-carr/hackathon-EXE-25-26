# Quick GitHub Codespaces Setup

This is the short version of the setup.

## What you need
- A GitHub account
- Access to GitHub Codespaces

## 1. Fork the repo
1. Open the repo on GitHub.
2. Click Fork.
3. Create the fork in your own account.

## 2. Create a Codespace
1. Open your fork.
2. Click Code.
3. Open the Codespaces tab.
4. Click Create codespace on main.

Wait a minute or two while it starts.

## 3. Start coding
When it opens, you can edit files straight away in the browser.

That is enough to begin.

## Optional: use VS Code on your laptop
1. Install VS Code.
2. Install the GitHub Codespaces extension.
3. Open Command Palette.
4. Run: Codespaces: Connect to Codespace.
5. Pick your Codespace.

## Optional: Python setup
You only need this if you want to run Python examples.

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

If you are not running Python code, skip this.

## Quick checks
- File editing works in Codespace
- Terminal opens in Codespace
- You can run basic commands like:

```bash
ls
git status
```

## Common problems
- Cannot create a Codespace: check your account plan and quotas.
- Extension connection fails: reconnect from Command Palette.
- Repo access issue: confirm you forked it to your own account.

## Done
You are ready to work in the hackathon repository.
