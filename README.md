# Osdag Tests — Developing unit tests for Osdag using PyTest

**Project:** Developing unit tests for Osdag using PyTest  
**Author:** Sandipan Bhattacherjee — @sandipanb01

## Overview
This repository contains:
- `osdag_validator_cli/` — CLI, API, GUI wrappers and helpers.
- `tests/` — PyTest test-suite for osdag validator classes.
- `dist/` — packaged/executable builds (if any).
- `README.md`, `LICENSE`, `.gitignore`

## Quickstart (dev)
1. Create & activate virtualenv:
   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```
2. Install dev deps:
   ```powershell
   pip install pytest fastapi uvicorn
   ```
3. Run tests:
   ```powershell
   pytest -q
   ```
4. Run API (local):
   ```powershell
   uvicorn osdag_validator_cli.app:app --reload
   ```

## CLI examples
```powershell
python -m osdag_validator_cli.cli fu 410
python -m osdag_validator_cli.cli fy 250
python -m osdag_validator_cli.cli plate 10 250
```

## Project files of interest
- `osdag_validator_cli/cli.py` — main CLI entrypoints.
- `osdag_validator_cli/app.py` — FastAPI wrapper to expose validator as HTTP API.
- `tests/` — unit tests (PyTest).



## License
This project is available under the MIT license. See `LICENSE`.
