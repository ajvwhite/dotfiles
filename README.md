DOTFILES
========

This repository contains customisations that I typically use on my mac setups.  Mostly, these focus around configurations for zsh shell, git version control, and vim.

Dependencies
------------

* [Homebrew](https://brew.sh/)
* [Ansible](https://www.ansible.com/)
* [Awesome Terminal Fonts \(Needs manuall install due to system protection\)](https://github.com/gabrielelana/awesome-terminal-fonts)
* [Powerline Fonts \(For iTerm 2 - Set font to "Mesio LG M DZ Regular"\)](https://github.com/powerline/fonts)

You can install ansible via Homebrew

```
$ brew install ansible
```

Installation
------------

Clone the repository:

```
$ git clone https://github.com/ajvwhite/dotfiles.git
$ cd dotfiles
```

**DANGER** This will fully overwrite your current dot files (e.g. ~/.profile ~/.bash_profile ~/.zshrc etc)!

Run Ansible

```
$ ansible-playbook default.yml
```

You can skip package installations and/or network operations (Vim plugins cloning, etc)
with something like:

```
$ ansible-playbook default.yml --skip-tags="java,zsh"
```

You can also run only specified tags with something like:

```
$ ansible-playbook default.yml --tags="zsh,zshplugins,zshthemes"
```

If you want to install/configure only certain parts, replace `default.yml` in the commands
above with of the other playbooks.

Features
--------

Here is a brief overview of some of the features hidden deep in these dotfiles.

### Git version control

1.  Color support in console git client.
2.  Several handy git aliases to make frequent operations faster ("st" instead of "status", "co" instead of "checkout",
    etc).
3.  Several handy git aliases to make long lists of parameters much shorter ("la", "whatchanged", etc).

### Vim text editor

1.  Collection of plugins for web developers (PHP Indent, NERDTree, Syntastic, Tagbar, Gist, etc).
2.  Support for 256 colors in console.


Feedback
--------

You can send in comments and pull requests for the project on GitHub at https://github.com/ajvwhite/dotfiles.

Credits & Thanks
----------------

A huge thanks to [Constantinos Kouloumbris](https://github.com/ckr) as this is hugely based off his 
[dotfiles](https://github.com/ckr/dotfiles) project