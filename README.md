# Scrape

Scrape is an automated data collection workflow powered by GitHub Actions.  
It periodically executes a shell script (`scrape.sh`) to scrape or fetch data from a Spotify's real-time updated listening data analytics and commits the results back to the repository automatically.

---

## Overview

This project uses a GitHub Actions workflow to:

1. Check out the repository.
2. Ensure `scrape.sh` exists, creating it if missing.
3. Run the scraping command to collect data from the target API.
4. Commit and push any changes automatically to the repository.

The default scraping command targets:

---

## Automation Schedule

The workflow runs on the following schedule (in UTC):

Cron expression:
```yaml
- cron: '2,30,52 * * * *'
