# Everything I did with my jupyterhub , jupyter, and instance things
Various things I have done to tweak or break things
2019-08-04:
- Added /opt/miniconda/bin/ to the path with `PATH=/opt/miniconda/bin:$PATH` so that in future it will be on the search path
- Found the location of jupyterhub.sqlite file at /srv/jupyterhub/jupyterhub.sqlite
- The location of the jupyterhub_config.py is at /etc/jupyterhub
- jupyter lab is broken it does not open in the browser window as it should
- I must backup the sqlite database and then do `jupyterhub db-upgrade` everytime I update a new package in jupyter notebook
- Jupyterhub db-upgrade can break so I must backup the database
- Backing up the database can be done with any of the following commands:
[See more here](https://www.quackit.com/sqlite/tutorial/backup_a_database_to_file.cfm)
- If you want to find out where is jupyterhub_config.py, type: whereis jupyterhub and then cd into /etc/jupyterhub

1. `.backup mybackup.db` where .backup is the command, 
2. Type sqlite3 to enter sqlite > prompt
3. Ctrl-D to get out of sqlite (.exit or .quit did not work in Mac)

- A sample jupyterhub_config.py
https://gist.github.com/edsu/27a7057c9bd35884c117
