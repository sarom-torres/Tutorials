# Basic Topics about Apache Server

## Ubuntu

### Check if apache2 is already installed
```
dpkg --get-selections | grep apache
```
or
```
apache2 -v
```

## CentOS

### Check if httpd is already installed
```
rpm -q httpd
```
or
```
rpm -qa | grep -i httpd
```
### Installation
```
# yum install httpd httpd-devel mod_perl php mod_ssl
```
