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
recommended to use the latest stable version if possible.

* Download or clone the repository to some directory (e.g. `~/github/porn/gitconfig/`).
```
cd
mkdir -p github/porn
cd github/porn
git clone https://github.com/porn/gitconfig.git
```

* Symlink the gitconfig to your home:
```
ln -s ~/github/porn/gitconfig/gitconfig ~/.gitconfig.porn
```

* Include the gitconfig file in your `~/.gitconfig`:
```
[user]
	name = Your Name
	email = email@example.xxx
...
[include]
	path = ~/github/porn/gitconfig/gitconfig
```
This way your local changes won't overwrite the file when you use:
```
git config --global user.name "James Bond"
```

* Include the git prompt config in your `~/.bashrc`:
```
$ echo "source ~/github/porn/gitconfig/bashrc.gitprompt" >> ~/.bashrc
```
On next login your bash prompt will show nice symbols that represent the state
of your current working tree. If you want to enable git prompt without logging
out and in, just source the file:
```
$ source ~/github/porn/gitconfig/bashrc.gitprompt
```
