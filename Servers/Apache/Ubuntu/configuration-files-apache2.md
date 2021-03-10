# Configuration Files in Apache2

## :open_file_folder: File's Structure 

Apache2 is configured by directives in configuration files. The default directory structure is below:

```
etc
 |__apache2
      |__apache2.conf
      |__conf-available
      |    |__...
      |__conf-enabled
      |    |__*.conf
      |__envvars
      |__magic
      |__mods-available
      |    |__...
      |__mods-enabled
      |    |__*.load
      |    |__*.conf
      |__ports.conf
      |__sites-available
      |    |__...
      |__sites-enabled
           |__*.conf
```
- **apache2.conf**: main configuration file. It contains the configuration directives that give the server its instructions. Changes to the main configuration files are only recognized when it is started or restarted.
- **conf-available**: it contains available configuration files.
- **conf-enabled**: holds symlinks to the files in `conf-available`. When a configuration file is _symlinked_, it will be enabled the next time apache2 is restarted.
- **envvars**: where environment variables are set.
- **mods-available**: it contains configuration files to load modules and configure them.
- **mods-enabled**: holds symlinks to the files in `mods-available`.
- **ports.conf**: houses the directives that determine which ports Apache2 is listening on.
- **sites-available**: has configuration files for Virtual Hosts. `Virtual Hosts` allow Apache2 to be configured for multiple sites that have separate configurations.
- **sites-enabled**: itcontains symlinks to the `sites-available`.
- **magic**: instructions for determining MIME type based on the first few bytes of a file.
