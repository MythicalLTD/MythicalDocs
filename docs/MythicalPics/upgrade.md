---
sidebar_position: 6
---
# Update MythicalPics

This documentation covers the process for updating within the 1.x series of releases. This means updating from — for example — 1.0.0 to 1.1.0

## Download the Update
The first step in the update process is to download the new client files from GitHub. The command below will download the release archive for the most recent version of MythicalPics.
```bash
cd /var/www/MythicalPics
mariadb-dump -p mythicalpics > mythicalpics_backup.sql
cd /var/www
zip -r mythicalpicsbackup.zip MythicalPics/
cd /var/www/MythicalPics
git fetch --all
git reset --hard origin/main