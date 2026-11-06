# cronmiss canary: GitHub Actions

A scheduled workflow that runs every hour at :17 and pings [cronmiss](https://cronmiss.com).

From Nov 4 to 6, 2026 it was scheduled every 5 minutes, GitHub's shortest schedule, and GitHub started it only every 4 to 8 hours. That measured throttling, so it now runs hourly: each hourly run that never arrives within 45 minutes is a run GitHub dropped.

It measures how reliably GitHub Actions actually fires scheduled workflows: how often runs are delayed, and how often they are dropped. The results feed the public platform-health page on cronmiss.com.

The ping URL is a repository secret. A monthly empty commit keeps GitHub from disabling the schedule after 60 days without activity.
