# :headphones: How to install a Spotify

## Installing using a repo

Adding the public key
```
curl -sS https://download.spotify.com/debian/pubkey_0D811D58.gpg | sudo apt-key add
```
Set the Spotify repository in the source.list:
```
echo "deb http://repository.spotify.com stable non-free" | sudo tee /etc/apt/sources.list.d/spotify.list
```
Install the Spotify client:
```
Then you can install the Spotify client:
```

## Installing using snapd

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
$ sudo snap remove spotify
```
If you check the list using `snap list` you will see that the spotify is still there and `disabled`. To remove completely run the following comand.
```
$ sudo snap remove spotify --revision=[rev-number-column]
```
