## Prerequizites
1. Make sure you have `cronie` package installed on the system
2. Make sure crond service is enabled and running

## Tasks for Self-checking

### 1. Creating Cron Jobs with crontab tool
- Using command `crontab -e` create a job (to run every minute) to print `date` command output to /tmp/task1.
- Using command `crontab -e` create a job (to run every 5 minute) to erase /tmp/task1.
- Using command `crontab -l` check created cron jobs.

### 2. Creating Cron Jobs with definitions in files
- create a job (to run every 3 minute) to print `date` command output to /tmp/task2.
- create a job (to run every 10 minute) to erase /tmp/task2.
- check /tmp/task2 file content.

Example:
```bash
echo '*/5 * * * * root date > /var/log/cron_job.log' > /etc/cron.d/5-min-log
tail -f /var/log/cron_job.log
```

### 3. Hourly, daily, weekly, monthly jobs
- create a job (to run every hour) to print `date` command output to /tmp/task3_hourly.
- create a job (to run every day) to print `date` command output to /tmp/task3_daily.
- create a job (to run every week) to print `date` command output to /tmp/task3_weekly.
- create a job (to run every month) to print `date` command output to /tmp/task3_monthly.
- check the content of all resulting files

Example:
```bash
cat << 'EOF' > /etc/cron.hourly/every-hour-log
#!/bin/bash
echo $(date) >> /tmp/hourly-test
EOF
chmod +x /etc/cron.hourly/every-hour-log
# after an hour
cat /tmp/hourly-test
```
