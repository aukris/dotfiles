# Dotfiles
WIP

## New Machine Setup
READ THE INSTRUCTIONS SPECIFIC TO YOUR MACHINE TYPE IN RESPECTIVE FOLDER

### Step By Step
0. Download the zip of this repo so that you can run few scripts.
0. Go to `macos/install` or similar and run the scripts as needed. You will need to run this only once per machine.
0. Go to `macos/configure` or similar and run the scripts as needed. `macos.sh` might be the first one if you are running for macOS. Per user.
0. Setup the .ssh so that you can clone this repo and use that for symlinking.
0. Clone this repo and also setup the appropriate git config (user.name etc. specifically for this repo)
0. In the repo root, use gnu stow to make config available to your home directory. Per user.
```
stow bash -t ~/ -v --ignore=.DS_Store      # will configure bash for you etc. It might error out if the file it is trying to symlink already exists, cleanup is up to you.
stow others -t ~/ -v --ignore=.DS_Store    # will configure lot of other smaller dotfiles at your home directory.
stow vim -t ~/ -v --ignore=.DS_Store       # will configure vim. Run `vim/install.sh` before that.
stow git -t ~/ -v --ignore=.DS_Store
mkdir -p ~/.config/
stow fish -t ~/.config/ -v --ignore=.DS_Store
```
0. Delete `"~/Library/Application Support/OpenEmu/Bindings/Default.oebindings"` if the USB game controllers are not working in OpenEmu

## Exclusions
* Atom settings are synced using the `sync-settings` package which depends on github's gists.
* `sync-settings` package for Atom may not sync language specific settings like gfm soft wrap.

## ToDo
* Most of the Ubuntu options as they haven't been tested yet
* For brew install, check for packages with flags or with alternate names isn't done properly
* Have richer config for `others`
* Have a better bash_history config as in what should go in, duplicates, sharing in tabs etc.
* Have better config for git especially when it comes to mergetool, difftool, and aliases, attributes, ignores etc.
* Detailed configuration for vim
* Detailed configuration for tmux
* Detailed configuration for fish
* Explore alternatives to Terminal on macOS (iTerm 2?)

## Resources
* [Using Stow](https://spin.atomicobject.com/2014/12/26/manage-dotfiles-gnu-stow/)
* [Best Shell Setup](https://bitbucket.org/flowblok/shell-startup/src)
