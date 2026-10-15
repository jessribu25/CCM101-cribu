# Automation Research

## Bash Script
A Bash script is a text file made up of Linux commands that the shell runs one after another, from the first line to the last, just as if someone were typing them manually. The first line, `#!/bin/bash`, is known as a "shebang." It tells the operating system which interpreter, Bash in this case, should be used to execute the rest of the file.

## Variables
Programmers use variables such as `$BACKUP_DIR` rather than writing out the full folder path each time, since this keeps scripts easier to maintain and reduces mistakes. If the backup location changes, only the one variable assignment at the top needs updating, instead of searching through the whole script to fix every command that mentions the path.

## Cron Job
A cron job is a task scheduled with Linux's built-in `cron` daemon, which automatically runs a given script or command at a chosen time, date, or interval without anyone needing to start it. This matters for cloud operations because essential recurring jobs, like backups, shouldn't rely on someone remembering to run them each day. Cron takes human memory out of the equation.
