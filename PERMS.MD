

permissions are in bit format 
7 = 111 full control
6 = 110
5 = 101
4 =     read permission
3
2 =     write permission
1 =     execute permission


give permissions for user-owner, group, execute 
``` 
sudo chmod 775 <file>.php
```

give recursive persmissions for current user and groups. And execute permissions for website users
```
sudo chmod 775 <folder> -R
```


Allow the docker group to do things in the dub dub dub folder
```
sudo chgrp -R docker /var/www/
```
