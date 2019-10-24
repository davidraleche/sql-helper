### RDS AUTHENTICATION
	mysql -h xxxxxxxxxta.us-east-1.rds.amazonaws.com  -u admin -p 
	
	SELECT User,Host FROM mysql.user;
	SHOW GRANTS FOR 'drupal'@'%';


### SQL Client Recommendation

  	TablePlus(Mac)

  	DBeaver

	Mysql Workbench

	SequelPro

	
### Import database

```
mysql h xxxxx.com -u username -p dbname < dbexport.sql
```

### Export all Databases

```
    sudo mysqldump --all-databases -udxxxx -p > oct-16-2019-database.sql
```

### Export Specific Database

```
mysqldump --databases xxxxxx-name -udxxxx -p > oct-16-2019-database-david-raleche.sql
```

NOT A ROOT USER


    mysqldump –all-databases> database.sql

    mysqldump -all-databases -uuser -ppassword> database.sql

    mysqldump –all-databases –skip-lock-tables -u user-ppassword  > Sept2018database.sql

### Long Queries
	Explain 

### SQL TABLE SIZE
	select table_schema, sum((data_length+index_length)/1024/1024) AS MB from information_schema.tables group by 1;

### CRON NACKUP DATABSECron Backup Database


	mysqldump -uroot -p MyDatabase >/home/users/backup_MyDB/$(date +%F)_full_myDB.sql
