# Linux common commands

1. Connect to server(ip address) by ssh and create full database dump
  
  ```
  ssh user@255.255.255.255 -p SSH_PORT
  pg_dump --verbose -F c -Z 1 -b --dbname=db_production > ~/db_production.dump   ##First method - full dump
  pg_dump --verbose -F c -Z 0 -t products --dbname=db_production > ~/db_production_products.dump  ##Second method - table products dump
  ```

2. Copy file to local PC or another remote host
  
  ```
  scp -P SSH_PORT user@255.255.255.255:/home/user/db_production.dump ~/db_production.dump
  ```
  
3. Drop old db, create new DB with password and restore dump.
  
  ```
  psql -l  ##list of DataBases, Q for quit
  dropdb db_production
  createdb -E UTF8 -T template0 -U user --lc-collate=ru_RU.UTF-8 --lc-ctype=ru_RU.UTF-8 db_production -W   ##There could be use en_US.UTF-8
  pg_restore --verbose -U user -d db_production ~/db_production.dump  ##First restore method
  pg_restore --verbose --no-acl --no-owner -U user -d db_production ~/db_production.dump  ##Second restore method without owner  
  ```

4. To backup DB from Heroku server read this [https://devcenter.heroku.com/articles/heroku-postgres-import-export](https://devcenter.heroku.com/articles/heroku-postgres-import-export)
