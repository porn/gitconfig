# gitconfig

My personal git configuration being used on my laptop as well as on servers I
have to deal with.

# Features
* colours everywhere
* many aliases to save your fingers!
* using vim for diff and merges
* git-sh-prompt setup

# Installation

The .gitconfig `[include]` syntax requires Git 1.7.10+. Though it is
recommended to use the [latest stable version](https://launchpad.net/~git-core/+archive/ubuntu/ppa) if possible.

* Download or clone the repository to some directory (e.g. `~/github/michondr/gitconfig/`).
```
cd
mkdir -p github/michondr
cd github/michondr
git clone https://github.com/michondr/gitconfig.git
```

* Include the gitconfig file in your `~/.gitconfig`:
```
[include]
	path = ~/github/michondr/gitconfig/gitconfig
...
```
This way your local changes won't overwrite the file when you use:
```
git config --global user.name "James Bond"
git config --global user.email "jb@example.com"
```

* Include the git prompt config in your `~/.bashrc`:
```
$ echo "source ~/github/michondr/gitconfig/bashrc.gitprompt" >> ~/.bashrc
```
On next login your bash prompt will show nice symbols that represent the state
of your current working tree. If you want to enable git prompt without logging
out and in, just source the file:
```
$ source ~/github/michondr/gitconfig/bashrc.gitprompt
```

# auto-complete fixes
If shell does not auto-complete, for example branche names after typing `git co om- 'tab' 'tab'` use [this](https://apple.stackexchange.com/questions/55875/git-auto-complete-for-branches-at-the-command-line) help on stack owerflow
