
# Mac setup

This documentation describes how to setup Mac for work. It's my personal preference :)

## Environment
- Playbooks has tested in Oct/2021 with 
 	- macOS Big Sur(ver.11.6)
	- MacBook Pro(13-inch, 2020)

## Mac setup

- System Preference:
	- Apple ID:
		- Link Apple ID
	- Dock:
		- change position
		- enable automatically hide
	- Siri
		- disable
	- Notifications
		- disable for some app
	- Internet Accounts
		- untick for acconts
	- Wallet & Apple Pay
		- disable
	- Screen Time
		- Turn off
	- Printer:
		- install from self-service.app
	- Keyboard:
		- add Japanese(Hiragana Google)
		- Shortcut/Input Sources: check on "Selct the previous input source" and "Seletct next source in input menu"
	- Trackpad
		- Tap to click: enable
		- Track Speed: Fastest
	- Displays:
		- change resolution
		- NightShift:on
	- TimeMachine: setup

- Finder:(Preference)
	- hide disks from desktop
	- tags: hide all tags
	- Sidebar: cleanup
	- Advanced: "Show all filename extensions"
	- customize finder toolbar
		- http://itea40.jp/technic/mac-beginners/finder-tool-bar-customize-app-icon/
		- add app shortcut
	- quicklook for markdown file
		- https://github.com/toland/qlmarkdown
		- $ brew cask install qlmarkdown
	- quicklook for yaml
		- http://www.evanlovely.com/utilities/quicklook-yaml/


## Application setup

- google Drive:
- google Japanese input: setup
	- change keyboard setting
- browser bookmarks: restore
	- Safari
		- sync from iCloud
	- Chrome
	- Firefox
- Outlook: setup
	- just login with AzureAD
- slack:
- bash alias
	- .bash_profile, bashrc
- git: setup
	- git init
	- git clone
	- .gitignore
- Symbolic link for git directory
	- $ ln -s ln -s /Volumes/GoogleDrive/My\ Drive/git ~/git    ~
- Screenshot saved location
	- https://fukatsu.tech/mac-screenshot-path
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
- sublimetext3: setup(this can be skipped as not much used anymore)
	- install package control
	- Shortcut: command palette "Shift + Command + P"
	- installed plugin
		- all autocomplete: https://packagecontrol.io/packages/All%20Autocomplete
		- Bracket​Highlighter: https://packagecontrol.io/packages/BracketHighlighter
		- Google Search: https://packagecontrol.io/packages/Google%20Search
		- markdown extended: https://packagecontrol.io/packages/Markdown%20Extended
		- Monokai Extended: https://packagecontrol.io/packages/Monokai%20Extended
		- SideBarEnhancements: https://packagecontrol.io/packages/SideBarEnhancements
		- Synced​Side​Bar: https://packagecontrol.io/packages/SyncedSideBarin
		- Terminal: https://packagecontrol.io/packages/Terminal
		- Trailing​Spaces: https://packagecontrol.io/packages/TrailingSpaces
- powercli: setup
	- powershell is required. run command, "pwsh -version" to check.
	- check this site: https://blogs.vmware.com/PowerCLI/2018/03/installing-powercli-10-0-0-macos.html
- Alfred
	- Assign MacOS permissions
		- Accessibility
		- Full Disk Access
- Spectacle
	- Assign MacOS permissions
		- Accessibility
	- Enable Launch at login
- Visual Studio Code
	- Added later this section
- virtual box:
- vagrant: setup
	- test: vagrant up
	- install plug-in
		- $ vagrant plugin install vagrant-hostmanager
		- $ vagrant plugin install vagrant-hosts
		- $ vagrant plugin install vagrant-vbox-snapshot
		- $ vagrant plugin install sahara
- docker: setup
	- initial setup: docker mac client
