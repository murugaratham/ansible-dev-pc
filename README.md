# Mac Developer Machine Setup

This repository contains useful scripts to set up a mac development machine. They have been tested with the following OSes:

| OS                                    | SKU     | Version(s) |
| ------------------------------------- | ------- | ---------- |
| [macOS](https://www.apple.com/macos/) | Desktop | 11.6       |

## Pre-Requisites

### macOS

1. Install [Homebrew](https://docs.brew.sh/)
1. Install [Ansible] `brew install ansible`

## Running

Before running the scripts, please review `_all.yaml` and `_all_no_customization.yaml`, and comment out software you don't want installed. In particular, most folders contain `customization.yaml` files which tend to contain my personal opinions on customizations; feel free to comment out sections of those files, or ignore them entirely.

To run the setup:

```bash
ansible-playbook -K _all.yaml
```

To see what has changed since the last run:

```bash
ansible-playbook -K _all.yaml --check --diff
```

You will be prompted for your password, so that administrative-level software can be installed. _**You must be a sudoer to run these scripts, otherwise the installation process will fail.**_ You can also run individual files if you'd prefer to take more control over what's executed.

Since core OS packages are upgraded, it is safest to reboot the PC/VM after running these scripts. At a bare minimum, many UI shell customizations done here will require you to log out and log back in.

Feel free to fork and make your own preferences

- [x] Making iterm ANSI colors similar VS Code
- [x] Using Fira Code as default font in ITerm

Installed Apps:

- AppCleaner
- Docker
- Dotnet
- Chrome
- ITerm2
- NodeJS
- Oh My Zsh
- Rectangle
- Slack
- Terraform
- Vs code
