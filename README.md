# config-git
####Configuration multiple credentials 
---

Generation keys
`ssh-keygen -o -a 100 -t ed25519 -f ~/.ssh/id_ed25519_diogo_gmail -C 'diogo@gmail.com'`

`ssh-keygen -o -a 100 -t ed25519 -f ~/.ssh/id_ed25519_diogobiz_hotmail -C 'diogobiz@hotmail.com'`

---

> file ~/.ssh/config

```
Host diogo.github.com
    HostName github.com
    User git
    AddKeysToAgent yes
    IdentityFile ~/.ssh/id_ed25519_diogo_gmail

Host diogobiz.github.com
    HostName github.com
    User git
    AddKeysToAgent yes
    IdentityFile ~/.ssh/id_ed25519_diogobiz_hotmail
```

usage: 

`git clone git@diogo.github.com:sanar/new-esanar.git`

`git clone git@diogobiz.github.com:[user]/[repo].git`

