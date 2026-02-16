# Probely DAST scan (GitHub Actions)

This repo runs a Probely DAST scan on push/PR and on manual trigger.

## Setup

1. **Settings** → **Secrets and variables** → **Actions**
2. Add **Secret:** `PROBELY_API_KEY` (your [Probely API key](https://help.probely.com/en/articles/8592281-how-to-generate-an-api-key))
3. Add **Variable:** `PROBELY_TARGET_ID` (target ID in Probely for the app you want to scan; [add a target](https://help.probely.com/en/articles/5733114-how-to-add-a-target) if needed)

## Run

- **Automatic:** push to `main`/`master` or open a PR
- **Manual:** **Actions** → **Probely Scan** → **Run workflow**

The workflow installs the Probely CLI, starts a scan on the target, waits for it to finish, and fails the job if there are high or critical findings.
