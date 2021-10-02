# ADB (Android Debug Bridge)

ADB is a command line tool that allow the communication with an Android device to install and debbugging apps. `adb` is a client-server program and have the following components.

- `client`: It runs in development machine and sends commands.
- `daemon (adbd)`: which run the comands on a device. It runs as a backgroud process in each device.
- `server`: It runs as a backgroud process in development machine. It manages communication between the client and the daemon.

ADB is included in Android SDK Platform-Tools package.
