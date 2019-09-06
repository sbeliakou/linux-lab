# linux-lab

## 19. Cron overview and usage

### 1. Crontab interface
- Using command `crontab -e` create a job (to run every minute) to print `date` command output to /tmp/task1. 
- Create cron job via `crontab -e` which will be executed every 5 minutes and will be erasing /tmp/task1 file.
- Check all cron jobs via `crontab -l`


### 2. Manual way

2.1. Create cron job (in /etc/cron.d/) which will be executed every 3rd minute and will be appending current timestamp to /tmp/task2 file.

2.2 Create cron job (in /etc/cron.d/) which will be executed every 10th minute and will be erasing /tmp/task2 file.
Check task2 file content.



### 3. Hourly, daily, weekly, monthly jobs

3.1. Create cron job "task3_hourly" which will be executed every hour and will be appending current timestamp to file /tmp/task3_hourly.

3.2. Create cron job "task3_daily" which will be executed every day  and will be appending current timestamp to file /tmp/task3_daily.

3.3. Create cron job "task3_weekly" which will be executed every week  and will be appending current timestamp to file /tmp/task3_weekly.

3.4. Create cron job "task3_monthly" which will be executed every month  and will be appending current timestamp to file /tmp/task3_monthly.
Check the content of all resulting files.
