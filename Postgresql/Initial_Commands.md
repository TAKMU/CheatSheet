### Enter to a database   
<details>   
 
 **enter from command line**
 > su postgres;  
  psql *database_name* **username**
  
  **Connect to another database from postgres**
  >\\c *another_database*  
  
  
</details>

### Enter postgresql and create databases  
<details>   
 
 **Create database**  
 >su postgres  
 >psql *database_name* username  (can use postgres as *database_name*)  
</details>


### Create user and alter user   
<details>   
 
 **Create username with superuser**
 > \# create user *user_name* *superuser*;  
  
  **Create password for user**
  >\# \\password *user_name*  
  
  **Check all users**  
  >\\du 
  
  
</details>

