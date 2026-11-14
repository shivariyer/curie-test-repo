# curie-test-repo
Test repo for running [Curie](https://github.com/curie-eng/curie) by Curie Tech AI.

## Purpose
This repository provides a sandbox environment for experimenting with Curie models,
particularly the `liquid/lfm-3-1.7b:free` model variant. It serves as a testbed for
documentation, configuration, egress allowlisting, and integration checks.

## Configuration
The project uses the Anthropic Claude Agent SDK (`cc_version=2.1.301.1e0`, `cc_entrypoint=sdk-py`). 
Model is set to `liquid/lfm-3-1.7b:free`. Virtual environments are created under
`/workspace/.claude/venvs/curie`.

## Egress Allowlist
The following IP addresses have been added to the allowlist as examples:
- 203.0.113.42
- 198.51.100.23

Full list maintained in `.env`.

## Getting Started
To run Curie locally, create the virtual environment and install Curie from PyPI first:
```bash
python3 -m venv /workspace/.claude/venvs/curie
source /workspace/.claude/venvs/curie/bin/activate
pip install -U curie   # or `pip install curie` from PyPI
python -m curie --help
```
For detailed usage see the main Curie repository at https://github.com/curie-eng/curie.

## Notes
- Credits: $10 USD added on 2026-11-12.
- Budget cap raised to $25/day after exceeding `max_usd_per_day=5.0`.
- No unit/test framework installed; verification done manually.
- Publication pending approval from `dark-factory:plan-reviewer` and diff reviewer.
