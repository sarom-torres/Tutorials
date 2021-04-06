# :headphones: How to install a Spotify

It's possible to install **spotify** in Fedora using CLI with **snap**.

First, you need install the **snapd** package using the following command:
 ```
$ sudo dnf install snapd
```
Then, create a simbolic link to snapd directory:
```
$ sudo ln -s /var/lib/snapd/snap /snap
```
Finally, you can install Spotify using the following command:
```
$ sudo snap install spotify
```
