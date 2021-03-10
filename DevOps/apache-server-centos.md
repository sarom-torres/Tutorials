# Topics about CentOS Apache Server 

## Installation

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
