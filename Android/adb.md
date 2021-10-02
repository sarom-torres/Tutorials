# :robot: ADB (Android Debug Bridge)

ADB is a command line tool that allow the communication with an Android device to install and debbugging apps. `adb` is a client-server program and have the following components.

- `client`: It runs in development machine and sends commands.
- `daemon (adbd)`: which run the comands on a device. It runs as a backgroud process in each device.
- `server`: It runs as a backgroud process in development machine. It manages communication between the client and the daemon.

ADB is included in Android SDK Platform-Tools package.

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




