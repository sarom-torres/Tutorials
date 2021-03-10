# &#129718; Topics about Apache Server Ubuntu &#129718;

Apache is the most used web server platform in the world. In this tutorial we will learn some basic topics about Apache Server in Ubuntu enviroment.

-------------------------------------------------------------
## :wastebasket: Uninstall apache2

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
3. After that remove and cleanup the apache2 packages:
```
sudo apt-get purge apache2 apache2-utils apache2-bin apache2-data
```
4. Run the following command to cleanup the remaining packages:
```
sudo apt-get autoremove
```
5. Then type `whereis apache2` if the output is `apache2: /etc/apache2` remove the remaining directory with:
```
sudo rm -rf /etc/apache2
```

### Checking if apache2 has been removed

Type the following commands:

 Commando         | Success Output  | Unsuccess Output
------------------|-----------------|--------------------------
`which apache2`     | Blank line      | Path where is the apache2
`sudo service apache2 start` | `Failed to start apache2.service: Unit apache2.service not found` | Status of the service

------------------------------------------------------------------------------------------------------------------------------
## Installing apache2



