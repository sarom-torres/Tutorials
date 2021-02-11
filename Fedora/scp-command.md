# Copy files to and from server using scp

## Useful parameters
* **-P**: specifies the port to connect to on the remote host.

* **-p**: preserves modification times, access times, and modes from the original file.

* **-q**: (quiet mode) disables the progress.

* **-r**: copy entire directories recursively

* **-v**: (verbose mode).  print debugging messages about their progress.

## Without a file .ssh/config

### Single File
Copy **from** local **to** remote 
```
scp <filename> <remote-user>@<remote-server>:<file-path>
```

Copy **from** remote **to** local
```
scp <remote-user>@<remote-server>:<remote-file-path>  <filename>
```

### Multiple Files

Copy **from** local **to** remote 
```
scp <filename> <filename> <remote-user>@<remote-server>:<file-path>
```

Copy all files **from** local **to** remote
```
scp * <remote-user>@<remote-server>:<remote-file-path>
```

## With a file .ssh/config

Copy **from** remote **to** local
```
scp <alias>:<remote-file-path> <filename>
```


