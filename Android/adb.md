# :robot: ADB (Android Debug Bridge)

ADB is a command line tool that allow the communication with an Android device to install and debbugging apps. `adb` is a client-server program and have the following components.

- `client`: It runs in development machine and sends commands.
- `daemon (adbd)`: which run the comands on a device. It runs as a backgroud process in each device.
- `server`: It runs as a backgroud process in development machine. It manages communication between the client and the daemon.

ADB is included in Android SDK Platform-Tools package.

## Connecting Genymotion and Kali VirtualBox Machine

- In Virtualbox interface, configure `Genymotion` VM to have 2 network adapters: 
  - one of type `NAT` for internet access.
  - one of type `Host private network`.
- In Vitualbox interface, configure your `Kali VM` to have a network adapter of type `Host private network`.
- Start Genymotion, and get its ip address on the Host private network using `adb devices` command.
![image](https://user-images.githubusercontent.com/34520860/148214617-717bed22-ad8a-484c-a92c-020b09602a9a.png)

- Start your kali VM, and in console execute `adb connect [ip-of-genymotion]:[port]`
- Then in the Kali console check that adb devices show device connected typing `adb devices`

Now your emulator should be connected to your Kali VM through adb.

## Troubleshooting

### :warning: Versão do adb
```
➜  ~  adb devices
List of devices attached
adb server version (41) doesn't match this client (39); killing...
ADB server didn't ACK
adb server killed by remote request

* failed to start daemon
error: cannot connect to daemon
```
This erro occurs by the differece between the Genymotion version and the `adb` version. Mostly emulator have they own `adb` version in `tools/` directory.
Then, it's necessary change the `adb` client version.

```
$ sudo cp ~/Android/Sdk/platform-tools/adb /usr/bin/adb 
$ sudo chmod + /usr/bin/adb
```
Include in `/etc/environment` file the following line:
```
source ~/.bashrc
```




