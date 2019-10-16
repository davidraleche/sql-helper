### SQL Client

  TablePlus(Mac)

  DBeaver

  Workbench



	

### Export all Databases

NOT A ROOT USER

    mysqldump –all-databases> database.sql

    mysqldump –all-databases -uuser -ppassword> database.sql

    mysqldump –all-databases –skip-lock-tables -u user-ppassword  > Sept2018database.sql

### Long Queries
	Explain 

### SQL TABLE SIZE
	select table_schema, sum((data_length+index_length)/1024/1024) AS MB from information_schema.tables group by 1;
