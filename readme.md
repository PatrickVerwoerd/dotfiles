# Patrick's Dotfiles 
Inspired by https://driesvints.com/blog/getting-started-with-dotfiles

## A Fresh macOS Setup

Follow these install instructions to setup a new Mac.

1. Update macOS to the latest version with the App Store
2. Install Xcode from the App Store, open it and accept the license agreement
3. Install macOS Command Line Tools by running `xcode-select --install`
4. Copy public and private SSH keys to `~/.ssh` and make sure they're set to `600`
5. Clone this repo to `~/.dotfiles`
6. Append `/usr/local/bin/zsh` to the end of your `/etc/shells` file
7. Run `install.sh` to start the installation
8. Make sure Dropbox is set up and synced
9. Restore preferences by running `mackup restore`
10. Restart your computer to finalize the process

Your Mac is now ready to use!

## Your Own Dotfiles
## To do
- Check out the [`aliases.zsh`][6] file and add your own aliases. If you need to tweak your `$PATH` check out the [`path.zsh`][7] file.
- One thing you'll need to do manually is add your `~/.zshrc` file. You can't symlink the `.zshrc` file from your dotfiles because Mackup will already symlink your `.zshrc` from your home directory. That's why we'll need to create the file manually. Add the contents below to a `.zshrc` file in your user directory. What it will do is load the `.zshrc` file from your dotfiles. Make sure that the path to your dotfiles is correct.

```zsh
# Load Zsh
source ~/.dotfiles/.zshrc
```

> I've thought about backing up the `.zshrc` file entirely to Mackup and removing it from this repo. But I like it to be versioned with the repo so I can use it for documentation and as an example. I also believe that it makes more sense to keep it in this repo because it's pretty tied into this repo's files and settings.

When installing these dotfiles for the first time you'll need to backup all of your settings with Mackup. Install and backup your settings with the command below. Your settings will be synced to your Dropbox so you can use them to sync between computers and reinstall them when reinstalling your Mac. If you want to save your settings to a different folder or different medium than Dropbox, [checkout the documentation][8].

```zsh
brew install mackup
mackup backup
```

You can tweak the shell theme, the Oh My Zsh settings and much more. Go through the files in this repo and tweak everything to your liking.

[1]:	./.macos
[2]:	https://github.com/mathiasbynens/dotfiles/blob/master/.macos
[3]:	https://github.com/kevinSuttle/MacOS-Defaults
[4]:	./Brewfile
[5]:	https://caskroom.github.io/search
[6]:	./aliases.zsh
[7]:	./path.zsh
[8]:	https://github.com/lra/mackup#supported-storages