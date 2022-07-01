### Install Postgresql
<details>
 
Check web page https://www.postgresql.org/download/ in case of different OS (Rocky Linux 8, Postgresql 10)  
>sudo dnf update  
>sudo dnf install postgresql-server  
</details>  

### Initialize cluster  
<details>

Make sure that SELinux is inactive
>vim /etc/selinux/config  
>SELINUX=disabled

Create new directories:
>mkdir */home/data*  

Change ownership and permits
>sudo chown postgres */home/data*  
>sudo chmod 700  

Need to start new cluster with user postgres (without postgres, the owner of the files are going to be of the user you actually are using).  
>su postgres -c 'initdb -D */home/data*' 
 
Need to modify configure file for service
>sudo vim /usr/lib/systemd/system/postgresql.service  

Change setings in Environment (line 30 aprox)
>Environment=PGDATA=*/home/parent/data*  

Save and reload service
>systemctl daemon-reload
  
Start postgres  
 >systenctl start postgresql
</details>

