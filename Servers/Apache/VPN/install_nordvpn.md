## Installation NordVPN on Debian
> [Tutorial oficial](https://support.nordvpn.com/Connectivity/Linux/1325531132/Installing-and-using-NordVPN-on-Debian-Ubuntu-Raspberry-Pi-Elementary-OS-and-Linux-Mint.htm)

1. Download the `nordvpn-release_1.0.0_all.deb` [file](https://repo.nordvpn.com/deb/nordvpn/debian/pool/main/nordvpn-release_1.0.0_all.deb?_ga=2.179660580.1226708524.1613982547-1839197232.1599206390&_gac=1.16833227.1613134932.CjwKCAiA65iBBhB-EiwAW253W4YxEC5W8Xy3WfhpoFuKHIrFhBJg2WcHpvNhnMZKwk3_3BCwQY71xhoCEN0QAvD_BwE).

2. Install the package using one of the following commands:
  ```
  sudo apt-get install {/path/to/}nordvpn-release_1.0.0_all.deb

  ou

  sudo dpkg -i {/path/to/}nordvpn-release_1.0.0_all.deb
  ```

3. Update the apt-get list:
  ```
  sudo apt-get update
  ```

4. Finally install the nordvpn:
```
sudo apt-get install nordvpn
``` 
