# Change configuration file basics:  
<details>
    
### Configure file location  
  <details>
  
  >su postgres    
  >vim /home/*data*/*postgresql.conf*    
    
In case of error (service not started and need to access pg_ctl start), you can change file location in the **FILE LOCATIONS** section:
  >data_directory='/home/*actual_directory*'  
  >hba_file='/home/*data*/*pg_hba.conf*'  
  >ident_file='/home/*data*/*pg_indent.conf*'
  
   </details>
  
  ### Configure connection from host of another network  
  <details>

  >su postgres  
  >vim /home/*data*/*postgresql.conf  
    
Go to **CONNECTIONS AND AUTHENTICATION** section (2):  
  >listen_addresses='*'
    
Go to pg_hba.conf
    >vim /home/*data*/*pg_hba.conf*  
    
Check which users will have access locally (recommended to have one superuser with trusted to automatically connect to postgresql for backup)  
    
    >Type   Database  User            Address       Method  
    >local  all       *superuser*                   trust  
    >local  all       postgres                      md5  
    
Add which users will be able to access remotely (recommended md5 to allow remote connections through Dbeaver, could do other authentication methods but not necessary): 
Create a superuser to be able to access the postgresql server remotely: 
    
    >Type   Database  User            Address       Method  
    >local  all       *superuser*       *address*   md5
    
   </details>
  
  ### Define log locations
   <details>

  >su postgres  
  >vim /home/*data*/*postgresql.conf  
    
    
   </details>
  
  </details>
