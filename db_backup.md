# mongodb backup with crontab

```bash
# execute everyday 4 oclock
# db backup
# you can omit --db options to backup all dbs
0 4 * * * mongodump --db [dbname] --out /home/devuser/mongobackups/backup_$(date +\%Y\%m\%d\%H\%M\%S)
# delete files older than 7 days
0 4 * * * find /home/devuser/mongobackups/ -mtime +7 -exec rm -rf {} \;
```


# mongodb restore

```bash
# execute everyday 4 oclock
# db backup
# you can omit --db options to backup all dbs
sudo mongorestore --db [dbname] --drop /home/devuser/mongobackups/backup/[dbname]/
```


