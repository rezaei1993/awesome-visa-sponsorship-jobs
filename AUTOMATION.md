# Daily job automation

This repo refreshes [`DAILY_JOBS.md`](DAILY_JOBS.md) (and the matching README section) from Jaabz once a day.

## Repository secrets (required)

In **Settings → Secrets and variables → Actions**, set:

| Secret | Purpose |
| --- | --- |
| `JAABZ_CATALOG_URL` | Private catalog endpoint URL (from Jaabz) |
| `JAABZ_CATALOG_KEY` | Access token for that endpoint |

Do not commit these values. The fetch script reads them only from the environment.

## Run

**Actions → Daily Jaabz jobs → Run workflow**

Schedule: every day **07:00 UTC**.

## Local dry-run

```bash
export JAABZ_CATALOG_URL='…'
export JAABZ_CATALOG_KEY='…'
export JOB_TYPE=visa
python3 scripts/fetch_jaabz_jobs.py
```
