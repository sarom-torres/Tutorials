## Change user password

1. Open the shell and connect to the server as root user.
```
$ mysql -u root -h localhost -p
```
2. Run ALERT mysql command.
```
ALTER USER 'user-name'@'localhost' IDENTIFIED BY 'new-passwd';
```
3. Type SQL command to reload the grant tables in the mysql database.
```
FLUSH PRIVILEGES;
```
