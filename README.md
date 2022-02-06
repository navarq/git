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

# Need to authenticate?

The following two lines are what need to be done each time you want to add to a source code repo or download one
``` {sh }
eval $(ssh-agent)
```

``` {sh }
ssh-add
```
lookup the generated public key
```
cat ~/.ssh/id_rsa.pub 
```

Next go to settings
```
https://github.com/settings/keys


and copy the PUBLIC (.pub) key into the place listed.

# For remote connection to servers
For a linux server use the following to allow connections

```
sudo iptables -A OUTPUT -p tcp --dport 22 -m conntrack --ctstate NEW,ESTABLISHED -j ACCEPT
sudo iptables -A INPUT -p tcp --sport 22 -m conntrack --ctstate ESTABLISHED -j ACCEPT
```

* remember to allow connections through port 22 on your local router

```
sudo apt-get install openssh-server 

```
Then to open a remote command line connection to the server do the following
```
ssh <username>@<ip-address>
```
