# Permit Inspector MVP (Driveway / ROW Utility – Hollywood, FL)

**Advisory tool only — not legal advice or an official approval.**
This MVP pre-screens a submission against a small set of rules with clear explanations and citations. 
Update the rules and citations for your jurisdiction in `data/rules/hollywood_row_v1.json`.

## What this does
- Accepts a JSON describing a project (driveway/sidewalk/trench/FDOT flags, slopes, attachments).
- Runs a deterministic rules engine (pass/fail + why + citation).
- Optional PDF text scan for keywords (“NORTH”, “SCALE”, “ADA”) to catch missing annotations.
- Returns a structured report your UI (or Jotform) can render.

## Run locally
```bash
python -m venv .venv
# mac/linux:
source .venv/bin/activate
# windows:
.\.venv\Scripts\activate

pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
