# Virtual Hosts in Apache2

Virtual Host is the pratice of running more than one website on a single machine. There are two types:

- **IP-based**: there is a different IP address for every website.
- **Name-based**: there is multiple names running on each website.


## Name-based

![Name-based Virtual Host](/images/virtual-hosts.jpg)


The configuration files are in `/etc/apache2/sites-available` with the extension `.conf`.

First Site: `example1.conf` 
```
<VirtualHost *:80>
    ServerName www.example.com
    DocumentRoot "/var/www/html/example_html"
    ServerAlias example.com *.example.com
    ServerAdmin root@example.com
    ErrorLog "/var/log/httpd/error_log_example"
    CustomLog "/var/log/httpd/access_log_example" combined
</VirtualHost>
```
Second Site: `example2.conf` 
```
<VirtualHost *:80>
    ServerName www.example2.com
    DocumentRoot "/var/www/html/example2_html"
    ServerAlias example2.com *.example2.com
    ServerAdmin root@example2.com
    ErrorLog "/var/log/httpd/error_log_example2"
    CustomLog "/var/log/httpd/access_log_example2" combined
</VirtualHost>
```
With:

- `<VirtualHost *:80>`: this tag indicates that the configuration will apply to any IP address on port 80. It's possible to change the `*` to an specific IP address. Specific IP addresses or ports have precedence over their wildcard equivalents.

- `ServerName`: defines the unique name of the site.

- `DocumentRoot`: is the directory where the content exists that Apache should serve when we visit the domain name.

- `ServerAlias`: defines alternative names can be used when matching a request.

- `ErrorLog`: file where error logs are stored that are related to this virtual host.

- `CustomLog`: file where access logs are stored. When a client views a web page the access requests will be logged here.

### Useful Commands

To check the Virtual host **sintax**.
```
apachectl configtest
```
To show the VirtualHost **configuration**.
```
apachectl -S
```
To **enable** a specific site configured previously.
```
a2ensite <filename>
```
To **reload** apache2 and **activate** the new configuration.
```
systemctl reload apache2
```
To **disable** a specific site.
```
a2dissite <filename>
```
To check wich **sites** are enabled and by who:
```
a2query -s
``` 

## IP-based

![IP-based Virtual Host](/images/ip-based.png)

```
<VirtualHost 191.168.1.21:80>
    ServerName www1.example.com
    ServerAdmin webmaster@www1.example.com
    DocumentRoot "/www/vhosts/www1"
    ErrorLog "/www/logs/www1/error_log"
    CustomLog "/www/logs/www1/access_log" combined
</VirtualHost>

<VirtualHost 192.68.1.22:80>
    ServerAdmin webmaster@www2.example.org
    ServerName www2.example.org
    DocumentRoot "/www/vhosts/www2"
    ErrorLog "/www/logs/www2/error_log"
    CustomLog "/www/logs/www2/access_log" combined
</VirtualHost>
```
