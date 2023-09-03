# WSL Cheat sheet

### To list installed distributions

```powerhsell
wsl -l
wsl --list
```

### To list installed distributions along with its running status and wsl config being 1 or 2

```powerhsell
wsl -l --verbose
wsl -l -v
```

### To run a specific distro

```powerhsell
wsl -d distro_name
wsl --distribution distro_name
```

### To terminate/shutdown a specific distro

```powerhsell
wsl -t distro_name_to_shutdown
wsl --terminate distro_name_to_shutdown
```


### To shutdown all disstros
```powerhsell
wsl --shutdown
```

### Set specific distro as default

```powerhsell
wsl -s my_default_distro
wsl --set-default my_default_distro
```

### To EXPORT a running distro as image

```powerhsell
wsl --export distro_name_to_export windows_path\tar_file_name.tar
```

### To IMPORT an image as distro

```powerhsell
wsl --import new_distro_name install_location_windows_path tar_file_name.tar --version wsl-version-1-or-2
wsl --import Ubuntu-20 D:\VMs\WSL\Ubuntu-20\ Ubuntu-20.04.tar --version 2 # Setting my secondary HDD as storate loc for new distro
```

### To UNREGISTER (also removes the its file storage) a distro

```powerhsell
wsl --unregister distro_name_that_delete
```

# To run a WSL distro as the specified user.

```powerhsell
wsl -u username -d distroname
wsl -u root -d Ubuntu-20.04
```

## To change the default user for a distribution

```powerhsell
distributionName config --default-user Username
ubuntu config --default-user my_default_username
ubuntu2004.exe config --default-user johndoe # When you have Ubuntu 20.04 version installed from the Microsoft Store
```
