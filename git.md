# Powerfull Git
## Install git with Homebrew
```
brew install git
```

## Config git
Create `~/.gifconfig`:

```
# This is Git's per-user configuration file.
[user]
# Please adapt and uncomment the following lines: <----------- Add your info here
#	name = xxx
#	email = xxx@xxx.local

[filter "lfs"]
	clean = git-lfs clean %f
	smudge = git-lfs smudge %f
	required = true

[alias]
	ci	=	commit
	cia	=	commit --amend
	di	=	diff
	st	=	status
	co	=	checkout
	br	=	branch
	pr	=	pull --rebase
	sb	=	submodule
	lg  =   log --topo-order --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%ci) %C(bold blue)<%aN>%Creset' --abbrev-commit --date=relative
	sr  =   sb init; git sb sync; git sb update
[color]
	ui = auto
```

Highly recommand `git lg`.
