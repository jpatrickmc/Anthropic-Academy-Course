# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## State of the repo

This is a near-empty scratch workspace for an Anthropic course exercise (module 1). It is not a git repository and has no build, lint, or test tooling. It contains only:

- `module1-notebook.ipynb`: a Jupyter notebook. So far it has one cell, `%pip install anthropic python-dotenv`, and one empty cell.
- `.env`: local environment variables, presumably the Anthropic API key. Do not print, commit, or copy its contents.

## Working in the notebook

- Run it in Jupyter or the VS Code notebook UI. There are no scripts or CLI commands.
- Dependencies are installed from inside the notebook with `%pip install`. There is no requirements file or virtualenv config.
- The `python-dotenv` dependency implies the intended pattern: call `load_dotenv()` to read `.env`, then construct `anthropic.Anthropic()`, which picks up `ANTHROPIC_API_KEY` from the environment. Confirm the variable name in `.env` before relying on this.

Update this file as the project grows (for example, once there are multiple notebooks, scripts, or tests).
