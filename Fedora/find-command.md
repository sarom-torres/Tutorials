# Find Command

- To install the `find` command in Fedora::

```
sudo dnf install findutils
```

- Searching a file by name:

```
find -name file-name.sh
```

- Searching a file by size. The command below will search hte fils larger than 1GB.

```
find -size +1G 
```

- Searching a specific directory. The command bellow will search all occurences of "word" in My-directory:
```
find My-directory -name "*word*"
```
