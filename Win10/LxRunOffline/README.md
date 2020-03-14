## List of distro  
```
wsl -l -v
```
Or  
```
LxRunOffline l
```


## Install distribution  

```
$ LxRunOffline.exe i -n ubuntuAlpha -d D:\Runing-WSL\UbuntuAlpha -f D:\ISO\WSL\ubuntu-18.04-server-cloudimg-amd64-root-20191021.tar.xz -s  
```

i                   Install distro  
-n ubuntuAlpha      Name of distro  
-d D:\Runing-WSL\UbuntuAlpha        Save distro location  
-f D:\ISO\WSL\ubuntu-18.04-server-[longname].tar.xz     Where image to install  
-s      create shortcut to desktop  

## Run distribution
$ LxRunOffline l
list of wsl name

$ LxRunOffline r -n ubuntuAlpha

## Uninstall  

## Move  
```
lxrunoffline m -n [distro-name you got from lxrunoffline list] -d [where you want the distro to go]  
```



######  
#### I dont have test yet  
##### Backup instance configs  

export registry at  

* Computer\HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Lxss\<Distro ID>, you could check DistributionName and find out which one is the correct ID.  

* LxRunOffline has export config option, but I haven’t tried importing it back yet:
```
LxRunOffline ec -n Ubunto -f Ubuntu.xml
```
