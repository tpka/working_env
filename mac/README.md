
# Building Mac by Ansible+Homebrew

This documentation describes step by step Mac automated provisioning process. It's based on SpringerNature pre-build Mac.

- Written by: Tomohiro Takatsuka
- As of Oct/2020

## Environment

- macOS Catalina(ver.10.15)
	- built by SpringerNature Casper image

## Pre-Requirement

**install from App Store or Self-service.app**

- Xcode
	- require apple id

**install Homebrew**

- https://brew.sh/
- Run command on website.
	- check once installed $ brew --version
	- install cask $brew tap homebrew/cask

## Prepare ansible and run the playbook
**install ansible**

```
$ brew search ansible
$ brew info ansible
$ brew install ansible
$ ansible --version
```

**prepare for ansible**

```
$ mkdir mac-provisioning-ansible
$ echo 'localhost' > hosts
$ vim xxxx.yml
$ ansible-playbook -i hosts -vv xxx.yml
```
- check status of ansible
	- failed installing app.... etc

## Post-Ansible setup

**apps: install additional applications from SpringerNature self-service app**

- Cisco AnyConnect
- Cisco Jabber
- FileZilla
- Firefox
- Google Chrome
- Google Drive File Stream
- Kofa Power PDF for Mac
- MS Remote Desktop
- Slack
- SpringerNature WiFi
- VLC
- VMware Remote Console for Mac

**apps: install manually**

#- Flash player
#	- Safari & Firefox
#	- Chromium

**Mac setup**

This is my personal preference :)

- System Preference:
	- General:
	- Dock:
		- change position
		- enable automatic hide
	- Mission Control
	- Siri
		- disable
	- Wallet & Apple Pay
		- disable
	- Printer:
		- install from self-service.app
	- Keyboard:
		- add Japanese(Hiragana Google)
		- Shortcut/Input Sources: check on "Selct the previous input source" and "Seletct next source in input menu"
	- Trackpad
		- Tap to click
		- Track Speed: Fastest
	- Displays:
		- change resolution
		- NightShift:on
		- hide mirroring option
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

**Application setup**

- google Drive:
- google Japanese input: setup
	- change keyboard setting
- browser bookmarks: restore
	- Safari
		- ~/Library/Safari
	- Chrome
	- Firefox
- Outlook(or mail.app): setup
	- self-service.app for automatic setup
	- setup signature
- slack:
- remote desktop setting: restore setting
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
- bash alias
	- .bash_profile etc
- git: setup
	- git init
	- git clone
	- .gitignore
- .ssh directory
	- fix permission
- Symbolic link for git directory
	- $ ln -s ln -s /Volumes/GoogleDrive/My\ Drive/git ~/git    ~
- Screenshot saved location
	- https://fukatsu.tech/mac-screenshot-path

```
    # chmod 700 .ssh/
    # chmod 644 config
    # chmod 400 gts-tokyo.pem
    # chmod 600 id_rsa
    # chmod 600 id_rsa_filezilla
    # chmod 644 id_rsa.pub
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


## Reference

### Ref-ansible

- http://qiita.com/kkitta/items/27f8aca89e55b719cb6f
- http://blog.serverworks.co.jp/tech/2017/05/22/ansible-for-mac/

### Ref-Mac setup

- http://qiita.com/decobisu/items/661eb3fb1faa14a2a76d
