# Install Postgresql

Check web page https://www.postgresql.org/download/ in case of different OS (Rocky Linux 8, Postgresql 10)
>sudo dnf update

>sudo dnf install postgresql-server

Need to start new cluster with user postgres (without postgres, the owner of the files are going to be of the user you actually are using).

>su postgres -c 'initdb -D */home/parent/data*'

Need to modify configure file for service
>sudo vim /usr/lib/systemd/system/postgresql.service

Change setings in Environment (line 30 aprox)
>Environment=PGDATA=*/home/parent/data*
