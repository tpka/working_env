
# Mac setup

This documentation describes how to setup Mac for work. It's my personal preference :)

## Environment
- Playbooks has tested in Aug/2023 with 
 	- macOS Ventura(ver.13.5)
	- MacBook Pro(13-inch, 2022)

## Mac setup

- System Settings:
	- Apple ID:
		- Link Apple ID
	- Notifications
		- disable for some app
  	- Screen Time
		- Turn off
 	- Siri:
		- disable
 	- Desktop & Dock:
		- change position
		- enable "automatically hide"
  		- Hot Corners
	- Displays:
		- change resolution
		- NightShift:on
  	- Touch ID:
	- Wallet & Apple Pay:
		- disable
	- Keyboard:
		- add Japanese(Hiragana Google)
		- Shortcut/Input Sources: check on "Selct the previous input source" and "Seletct next source in input menu"
	- Trackpad
		- Tap to click: enable
		- Track Speed: Fastest
	- Printer:
	- TimeMachine: setup

- Finder:(Preference)
	- hide disks from desktop
	- tags: hide all tags
	- Sidebar: cleanup
	- Advanced: "Show all filename extensions"
	- customize finder toolbar
		- http://itea40.jp/technic/mac-beginners/finder-tool-bar-customize-app-icon/
		- add app shortcut
	- quicklook for markdown file(did not when setting up in 2023)
		- https://github.com/toland/qlmarkdown, this is not maintained since 2020...
		- $ brew install --cask qlmarkdown
	- quicklook for yaml(did not when setting up in 2023)
		- http://www.evanlovely.com/utilities/quicklook-yaml/, this is also old....

## Application setup

- google Japanese input: setup
	- change keyboard setting
- browser bookmarks: restore
	- Safari
		- sync from iCloud
	- Chrome
	- Firefox
- bash(.zshrc) alias
	- .bash_profile, bashrc
	- .zprofile, .zshrc
- git: setup
	- git init
	- git clone
	- .gitignore
- Symbolic link for working directory
	- $ ln -s /Users/<GDRIVE-PATH>/My\ Drive/600-code ~/code
- Screenshot saved location
	- [Macのスクリーンショットの保存先を変更する3つの方法](https://yama-mac.com/change_the_screenshot_save_location_and_file_format/#change_location)
	- % defaults write com.apple.screencapture location /Users/<GDRIVE-PATH>/My\ Drive/200-ongoing 

- .ssh directory
	- fix permission
```
    # chmod 700 .ssh/
    # chmod 600 ~/.ssh/config
    # chmod 600 ~/.ssh/id_rsa
    # chmod 644 ~/.ssh/id_rsa.pub
```
    - ssh-agentへ登録する (-KオプションはMacのみ使用できる)
		> ssh-add -K ~/.ssh/id_rsa
	- .ssh/config
		- to remember pass phrase
		- https://superuser.com/questions/1127067/macos-keeps-asking-my-ssh-passphrase-since-i-updated-to-sierra
- iterm2: setup
	- enable Sync by suing github account
- Alfred
	- Assign MacOS permissions
		- Accessibility
		- Full Disk Access
    	- Hotkey:
		- "Command double tap"
- Spectacle
	- Assign MacOS permissions
		- Accessibility
	- Enable Launch at login
- Visual Studio Code
	- Added later this section
