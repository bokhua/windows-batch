# Commonly used Windows batch commands

### Directory info
```
set current_drive=%~d0
set current_dir=%~dp0
```

### Script to run MS SQL scripts using sqlcmd
```
for %%var in (*.sql) do (
	sqlcmd /S 127.0.0.1,1433 /d mydb -U dbadmin -P dbpassword -i "%%var"
)
```
