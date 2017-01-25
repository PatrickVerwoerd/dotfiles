# Patrick's Dotfiles
Inspired by https://driesvints.com/blog/getting-started-with-dotfiles

## A Fresh macOS Setup

Follow these install instructions to setup a new Mac.

1. Update to the latest OS version with the App Store
2. Install Xcode from the App Store, open it en accept teh license
3. Install OS command line tools: `$xcode-select --install`
4. Copy SSH keys to `~/.ssh/`
5. Clone this repo to `~/.dotfiles`
6. Append `/usr/local/bin/zsh/` to the end of `/etc/shells` file:  
	`$ ~ echo "/usr/local/bin/zsh" >> /etc/shells`
7. Run `install.sh` to start the installation  
	`$ ~/.dotfiles/ sh install.sh`
8. Setup Dropbox en syncs files 
9. Restore preferences by running `mackup restore` from Dropbox
10. Run `source ~/.dotfiles/.zshrc`
11. Restart computer
12. In iterm: source \~/.dotfiles/.zshrc

🎉 Ready to play!