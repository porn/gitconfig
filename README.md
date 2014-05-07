# gitconfig

My personal git configuration being used on my laptop as well as on servers I
have to deal with.

# Installation

The .gitconfig `[include]` syntax requires Git 1.7.10+. Though I recommend using the latest stable version if possible.

1. Download or clone the repository to some directory (e.g. `~/github/porn/gitconfig/`).
```
cd
mkdir -p github/porn
cd github/porn
git clone https://github.com/porn/gitconfig.git
```
2. Symlink the gitconfig to your home:
```
ln -s ~/github/porn/gitconfig/gitconfig ~/.gitconfig.porn
```
3. Include the file in your `~/.gitconfig`:
```
[user]
	name = Your Name
	email = email@example.xxx
...
[include]
	path = ~/.gitconfig.porn
```
This way your local changes won't overwrite the file when you use:
```
git config --global user.name "James Bond"
```

# TODO
- screenshots;-)
- move installation of gitprompt here
