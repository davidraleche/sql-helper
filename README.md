### SQL Client

  TablePlus(Mac)

  DBeaver

  Workbench



	

### Export all Databases

NOT A ROOT USER

    sudo mysqldump --all-databases -udxxxx -p > oct-16-2019-database.sql

    mysqldump –all-databases> database.sql

    mysqldump -all-databases -uuser -ppassword> database.sql

    mysqldump –all-databases –skip-lock-tables -u user-ppassword  > Sept2018database.sql

### Long Queries
	Explain 

### SQL TABLE SIZE
	select table_schema, sum((data_length+index_length)/1024/1024) AS MB from information_schema.tables group by 1;

### CRON NACKUP DATABSECron Backup Database


	mysqldump -uroot -p MyDatabase >/home/users/backup_MyDB/$(date +%F)_full_myDB.sql
