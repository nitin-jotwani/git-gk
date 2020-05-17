### Setup multiple accounts
- Generate `key-gen` and name it something different like `id_rsa_myPersonalAccount`
- Create config file in `~/.ssh/` with custom `Host` and `IdentityFile` which we created above
```
Host personalrepo.github.com
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/id_rsa_myPersonalAccount`
```
- Copy `id_rsa_myPersonalAccount.pub` into your git ssh settings
- Clonning repo
	- Copy ssh url. example `git@github.com:nitin-jotwani/git-gk.git`
	- Clone it with your custom `Host` which we created in config file as `personalrepo.github.com`
	example: `git clone git@personalrepo.github.com:nitin-jotwani/git-gk.git`

### Git commit username Identity
Every repo contains `.git` folder inside it having config file also. By default config is referred from global.

To set different config for different repo, set it up inside repo without `--global`. This will update only local config inside `repo/.git`

example `git config user.name "Nitin Jotwani"

### Git Plugins/Tools
- [Zsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
- [Git commit](https://github.com/commitizen/cz-cli)
- [Git Town](https://www.git-town.com/)
