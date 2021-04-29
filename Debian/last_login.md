# :key: :house: Find the last login

To present the last logins performed on the computer using the following command:
```
$ last
```
or
```
$ last | head -n <number-lines>
```
## To find the last bad login attempts
```
$ lastb
```
 or reading the log file
```
$ tail -f -n 100 /var/log/auth.log | grep -i failed
```

## List User Last Login on Linux

List the last login times for all users:
```
$ lastlog
```
or specify a username
```
$ lastlog -u <user>
```
