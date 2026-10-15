Backup Script Guide
The Script (backup.sh)
bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR

# Compress the source directory into a tarball (.tar.gz)
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"
What chmod +x backup.sh Did

By default, Linux treats a new text file as data, not as a program, even if it contains valid shell commands. This prevents the system from accidentally executing random text files. chmod +x backup.sh grants the file execute permission, explicitly telling Linux that it is allowed to run as a program.

My finding: After creating the script with nano backup.sh, my first attempt to run ./backup.sh failed with bash: ./backup.sh: Permission denied. After running chmod +x backup.sh, the same command ran successfully and printed “Initiating automated backup...” followed by “Backup completed successfully at 20261015_034434!”

Verifying the Backup

Running ls -l backups/ confirmed the backup was created:

-rw-r--r-- 1 root root 177 Oct 15 03:44 backup_20261015_034434.tar.gz

This shows the following:

The file name contains the timestamp from the run (2026-10-15 at 03:44:34), which matches the success message.
It is owned by root and is readable by everyone but writable only by its owner.
It is 177 bytes, which is small, so the app-data folder contains very little data.
Cron Expression Breakdown: 0 2 * * * /root/backup.sh
Field	Value	Meaning
Minute	0	At minute 0
Hour	2	At 2 AM (02:00, 24-hour time)
Day of Month	*	Every day of the month
Month	*	Every month
Day of Week	*	Every day of the week

Put together, this schedules /root/backup.sh to run automatically every night at exactly 2:00 AM, with no human intervention required.

My finding: I registered the job with crontab -e and confirmed it with crontab -l. The listing showed the default explanatory comments from cron, with my entry 0 2 * * * /root/backup.sh on the last line, so the schedule is active.
