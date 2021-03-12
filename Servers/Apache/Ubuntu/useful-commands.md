# :crystal_ball: Useful Commands

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
