
# Building Mac by Ansible+Homebrew

This documentation describes step by step Mac automated provisioning process.

## Environment
- Playbooks has tested in Aug/2023 with
	- macOS Ventura(ver.13.5)
	- MacBook Pro(13-inch, 2022)
	- ansible [core 2.15.2]
	- python version = 3.11.4
	- Homebrew 4.1.4

## Pre-Requirement

**install Xcode App Store**
- Xcode
	- require your Apple ID

**install Homebrew**

- https://brew.sh/
- Run command on website.
	- check once installed $ brew --version
	- install cask $brew install cask

## Prepare ansible and run the playbook
**install ansible**

```
$ brew search ansible
$ brew info ansible
$ brew install ansible
$ ansible --version
```

**prepare ansible playbooks**

```
$ mkdir ansible-mac
$ echo 'localhost' > hosts
$ vim xxx.yml
$ ansible-playbook -i hosts -vv xxx.yml
```
- check status of ansible
	- for cask installation, you may be asked your password.

## Additional Mac setup

- The reference for additional mac setup is available here. This is totally my personal preference. :) 
  	- https://github.com/tpka/working_env/blob/master/mac/additional-setup.md


# Reference:
- https://brew.sh/
- https://formulae.brew.sh/cask/
- https://docs.ansible.com/ansible/latest/collections/community/general/homebrew_module.html
- https://docs.ansible.com/ansible/latest/collections/community/general/homebrew_cask_module.html
