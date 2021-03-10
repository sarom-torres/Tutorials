# &#129718; Topics about Apache Server Ubuntu &#129718;

## :floppy_disk: Install apache2

1. Update the packages using the following command:
```
sudo apt-get update
```
2. After that install apache2 with:
```
sudo apt-get install apache2
``` 
3. Check if apache2 is running
```
sudo service apache2 status
```
4. If the service is not runnig type the following command:
```
sudo service apache2 start
```

## :heavy_check_mark: Checking if apache2 is installed

Type:
```
dpkg --get-selections | grep apache
```
or
```
apache2 -v
```
