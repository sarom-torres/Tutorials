# :headphones: How to install a Spotify

### Installing snapd

It's possible to install **spotify** in Fedora using CLI with **snap**.

First, you need install the **snapd** package using the following command:
 ```
$ sudo apt install snapd
```
Then, create a simbolic link to snapd directory:
```
$ sudo ln -s /var/lib/snapd/snap /snap
```

### Installing Spotify 

You can install Spotify using the following command:
```
$ sudo snap install spotify
```

### Checking Spotify is installed
To verify if the spotify is installed use the following command:
```
$ sudo snap list
``` 

### Remove Spotify

Use snap to remove spotify
```
$ sudo snap remove
```
