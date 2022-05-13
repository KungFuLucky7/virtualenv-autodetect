# virtualenv-autodetect

Makes you forget that you have virtualenv's (if you use cd).
Works in Zsh and Bash.

## Installation

### Basic

Add this line to your .zshenv, .bashrc or .bash-profile:

```source /path/to/virtualenv-autodetect.sh```

### Oh-My-Zsh

```zsh
git clone git@github.com:RobertDeRose/virtualenv-autodetect.git $ZSH_CUSTOM/plugins/virtualenv-autodetect
sed -Ei 's/plugins=\((.*)\)/plugins=\(\1 virtual-autodetect\)/' $HOME/.zshrc
```

## What it does

* This will search for a Virtual Environment (VENV) to activate when you enter a directory or any of its descendants.
* VENV directory is detected automatically by locating a bin/activate inside that contains the strings "source bin/activate"
* An active VENV will be replaced with a deeper one if a descendant contains it's own VENV
* The VENV will be deactivated automatically when changing to a directory that no longer has a parent to a VENV

## Credit

Originally inspired and faintly based on https://gist.github.com/2211471 by https://github.com/egilewski/virtualenv-autodetect
