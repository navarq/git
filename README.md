# git
Instructions to set up git for the first time

Do not forget to change the part between <> to your github username

``` {sh }
export USER_AT_HOST="<ur-usernom-goes-ere>@github.com"
export PUBKEYPATH="$HOME/.ssh/known_hosts"
ssh-copy-id "$PUBKEYPATH" "$USER_AT_HOST"
```

``` {sh }
ssh-keygen -t rsa -b 4096 -f ~/.ssh/id_rsa
```

``` {sh }
eval $(ssh-agent)
```

``` {sh }
ssh-add
```
