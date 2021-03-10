# Topics about Apache Server Ubuntu

## Uninstall apache2

### Checking if apache2 is installed

Type:
```
dpkg --get-selections | grep apache
```
or
```
apache2 -v
```
### Removig apache2
1. Check if the apache2 is running usign the following command:
```
sudo service apache2 status
```
2. If apache2 is running stop the service:
```
sudo service apache2 stop
```
3. After that remove and cleanu the apache2 packages:
```
sudo apt-get purge apache2 apache2-utils apache2.2-bin
```
4. Run the following command to cleanup the remains packages:
```
sudo apt-get autoremove
```

### Checking if apache2 has been removed

Type the following commands:

 Commando         | Success Output  | Unsuccess Output
------------------|-----------------|--------------------------
`which apache2`     | Blank line      | Path where is the apache2
`sudo service apache2 start` | `apache2: unrecognized service` | Status of the service

