# :watch: Check and changing the date

### Check the current date
```
$ date
```

### Changing the date using CLI
Edit the file `timezone` in `/etc` directory.
```
$ sudo echo 'America/Sao_Paulo' > /etc/timezone
``` 
Then reconfigure the date using the following command:
```
$ sudo dpkg-reconfigure -f noninteractive tzdata
```
### Changing the date using a dialog box
Execute the following command:

```
$ sudo dpkg-reconfigure tzdata
``` 

