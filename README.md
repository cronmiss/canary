# cronmiss canary: GitHub Actions

A scheduled workflow that runs every 5 minutes (GitHub's shortest schedule) and pings [cronmiss](https://cronmiss.com).

It measures how reliably GitHub Actions actually fires scheduled workflows: how often runs are delayed, and how often they are dropped. The results feed the public platform-health page on cronmiss.com.

The ping URL is a repository secret. A monthly empty commit keeps GitHub from disabling the schedule after 60 days without activity.
