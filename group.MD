
The following lists all groups currently on the system
```{sh}
cut -d':' -f 1 /etc/group | sort
```

What the above does?
1. cut -d  => get all characters until the colon ":" symbol 
2. -f 1 => get all characters
3. /etc/group => the file which lists all the groups on the current system
4. | => pipe operator
5. sort => sort all group names alphabetically

Following creates a group called docker
```{sh }
sudo groupadd docker
```

To add a user to a group do
```{sh add-user to group}
sudo adduser <username> docker
```

To remove a user from a group do
```
sudo deluser <uisername> docker
```
