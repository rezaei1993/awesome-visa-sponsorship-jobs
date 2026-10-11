# Daily job automation

This repo can auto-refresh [`DAILY_JOBS.md`](DAILY_JOBS.md) from Jaabz every day.

## Enable GitHub Actions (one-time)

The workflow file is ready at `.github/workflows/daily-jaabz-jobs.yml` but pushing workflow files needs the `workflow` OAuth scope.

Run locally:

```bash
gh auth refresh -h github.com -s repo,workflow
cd /path/to/awesome-visa-sponsorship-jobs
git add .github/workflows/daily-jaabz-jobs.yml
git commit -m "Add daily Jaabz jobs workflow"
git push
```

Or paste the YAML into GitHub → Actions → New workflow.

Then: **Actions → Daily Jaabz jobs → Run workflow**.

Schedule: every day 07:00 UTC.
