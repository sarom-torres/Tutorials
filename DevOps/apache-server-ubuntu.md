# Topics about Apache Server Ubuntu

## Uninstall apache2

### Check if apache2 is installed

Type:
```
dpkg --get-selections | grep apache
```
or
```
apache2 -v
```
### Remove apache2
1. Check if the apache2 is running usign the following command:
```
sudo service apache2 status
```
2. If apache2 is running stop the service
```
sudo service apache2 stop
```

