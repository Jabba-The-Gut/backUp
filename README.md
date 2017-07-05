# backup.sh

Simple shell-script that makes incremental or full backup's of the user's /home directory. 
Supports a manual-mode with user interaction or an automated-mode for automation
with cron-Daemon on linux.

To automate the script, configure a cron-job to your needs and call the script
in mode = "auto"

# Head of scipt:
Programm: ./backup.sh
Call: ./backup.sh [mode] [scope] [path]
[mode]  "auto" --> mode used for automated backups with cron-Daemon
        "man" --> mode used for manual backups
[scope] "full" --> full backup
        "incremental" --> incremental backup
[path]  directory where the backup is stored

Descritpion: backup-script, that supports full/incremental backups of /home in two  
modes:
If the mode is manual, the user can manually backup /home. The auto mode is for 
automated backups with the cron-Daemon. It can be chosen between full and
incremental backup. All logs are stored in /BackUpLog in [path], fatal errors are logged
in "$HOME"/Desktop/backupscript_error_log.txt
 
