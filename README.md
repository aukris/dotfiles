# Anshul's Dotfiles

## New Machine Setup
READ THE INSTRUCTIONS SPECIFIC TO YOUR MACHINE TYPE IN RESPECTIVE FOLDER

### Step By Step
0. Go to `macos/install` or similar and run the scripts as needed. You will need to run this only once per machine.
0. Go to `macos/configure` or similar and run the scripts as needed. `macos.sh` might be the first one if you are running for macOS. Per user.
0. In the repo root, use gnu stow to make config available to your home directory. Per user.
  * `stow bash -t ~/` will configure bash for you etc. It might error out if the file it is trying to symlink already exists, cleanup is up to you.
  * `stow others -t ~/` will configure lot of other smaller dotfiles at your home directory.
  * `stow vim -t ~/` will configure vim

## ToDo
* Most of the Ubuntu options as they haven't been tested yet
* Get a better bash prompt
* For brew install, check for packages with flags or with alternate names isn't done properly
* Have richer config for `others`
* Have a better bash_history config as in what should go in, duplicates, sharing in tabs etc.
* Have better config for git especially when it comes to mergetool, difftool, and aliases, attributes, ignores etc.
* Detailed configuration for vim
* Detailed configuration for tmux
* Detailed configuration for fish

## Interesting Strategies
* [Using Stow](https://spin.atomicobject.com/2014/12/26/manage-dotfiles-gnu-stow/)
* [Best Shell Setup](https://bitbucket.org/flowblok/shell-startup/src)