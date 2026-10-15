# Laboratory Activity 9: Mission 9 – The Cloud Automation Engineer

## Mission Overview
This lab removes human error from a repeating operational task. A Bash script is written to automatically compress and back up a client's application data, and the Linux cron scheduler then runs that script every night at 2:00 AM, with no one needing to press a button.

## Objectives
* Learn the basic syntax of a Bash shell script, including variables and simple commands
* Use the nano text editor to write and save a script that can be executed
* Change Linux file permissions using chmod
* Understand task scheduling and how a crontab entry is written
* Document the automation code and cron job setup using Markdown

## Commands Executed
* `mkdir app-data` / `echo "..." > app-data/data.txt` — set up placeholder client data
* `nano backup.sh` — wrote the automated backup script
* `chmod +x backup.sh` — gave the script permission to run
* `./backup.sh` — executed the script and produced a compressed `.tar.gz` backup
* `crontab -e` — added the cron entry `0 2 * * * /root/backup.sh`
* `crontab -l` — checked that the schedule was installed

## Skills Learned
* Writing and running a Bash shell script from the terminal
* Controlling Linux file permissions with chmod
* Scheduling repeating automated tasks with cron
* Documenting automation code and scheduling syntax so other engineers can follow it
