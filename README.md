# gitconfig

My personal git configuration being used on my laptop as well as on servers I
have to deal with.

# Features
* colours everywhere
* many aliases to save your fingers!
* using vim for diff and merges
* git-sh-prompt setup

# Installation

* Download or clone the repository to some directory (e.g. `~/github/porn/gitconfig/`).
```
cd
mkdir -p github/porn
cd github/porn
git clone https://github.com/porn/gitconfig.git
```

* Include the gitconfig file in your `~/.gitconfig`:
```
[include]
	path = ~/github/porn/gitconfig/gitconfig
...
```
This way your personal changes won't overwrite the file when you use:
```
git config --global user.name "James Bond"
git config --global user.email "jb@example.com"
```

## Global Ignore
Feel free to use my collection of file patterns I don't want to track:
* Symlink the global gitignore file to your home directory
```
ln -s ~/github/porn/gitignore.global ~/.gitignore
```

## Shell Prompt
To display the git repository status in the bash prompt there are two options.

### Starship
I'd love to recommend [starship](https://github.com/starship/starship) project.
See the "screenshot":
```
…/gitconfig (master) [*%] at 10:25:17 $ git st
## master...origin/master
 M README.md
 M gitconfig
?? .README.md.swp
…/gitconfig (master) [*%] at 10:25:19 $
```

...on the prompt you can see:
- we're on the `master` branch
- `*` stands for `Changes not staged for commit`
- `%` stands for `Untracked files`
- and the time :)

### Bash Prompt Configuration
Kinda similar (but way poorer, bash-only) effect can be achieved using the
`bashrc.gitprompt` in this repo:

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
