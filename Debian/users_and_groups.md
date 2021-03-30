# :two_women_holding_hands: Users and groups in Linux

## Creating a groups

To create a new group use following command:
```
sudo groupadd <group-name>
```

To show all the groups type:
```
cat /etc/group
```
To show just the groups name:
```
cat /etc/group | awk -F: '{print $1}'
```
