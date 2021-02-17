---
title: Step List
weight: 1
---

# Steps that Topgrade takes when upgrading:

- **Linux**: Run the system package manager:
  - **Arch based**: Run [yay](https://github.com/Jguer/yay) or fall back to pacman
  - **Redhat based**: Run `yum upgrade` (or `dnf` if present)
  - **Debian based**: Run `apt update && apt dist-upgrade`
  - **Clear Linux**: Run `swupd update`
  - **Gentoo**: Run `layman -s ALL && emerge --sync -q && eix-update && emerge -uDNa world`
  - **openSUSE**: Run `zypper refresh && zypper dist-upgrade`
  - **Void**: Run `xbps-install -Su`
- **Linux**: Run [etc-update](https://dev.gentoo.org/~zmedico/portage/doc/man/etc-update.1.html):
- **DragonFly BSD**: Upgrade and audit packages
- **FreeBSD**: Upgrade and audit packages
- **Unix**: Run `brew update && brew upgrade`. This should handle both Homebrew and Linuxbrew
- **Unix**: Run `nix upgrade-nix && nix --upgrade`.
- **Unix**: Run [Pearl](https://github.com/pearl-core/pearl) `pearl update`.
- **Windows**: Run Topgrade inside WSL.
- **Windows**: Upgrade Powershell modules
- **Windows**: Upgrade all [Chocolatey](https://chocolatey.org/) packages
- **Windows**: Upgrade all [Scoop](https://scoop.sh) packages
- Check if the following paths are tracked by Git. If so, pull them:
  - ~/.emacs.d (Should work whether you use [Spacemacs](http://spacemacs.org/) or a custom configuration)
  - ~/.zshrc
  - ~/.tmux
  - ~/.config/fish
  - ~/.config/nvim
  - ~/.vim
  - ~/.config/openbox
  - ~/.config/bspwm
  - ~/.config/i3
  - ~/.config/sway
  - Powershell Profile
  - [Microsoft Terminal](https://github.com/microsoft/terminal) configuration
  - Custom defined paths
- **Unix**: Run [zr](https://github.com/jedahan/zr) update
- **Unix**: Run [zplug](https://github.com/zplug/zplug) update
- **Unix**: Run [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) update
- **Unix**: Run [antigen](https://github.com/zsh-users/antigen) update
- **Unix**: Run [antibody](https://getantibody.github.io/) update
- **Unix**: Run [fisher](https://github.com/jorgebucaran/fisher)
- **Unix**: Upgrade tmux plugins with [TPM](https://github.com/tmux-plugins/tpm). _Note_: Do not use
  the `-b` flag in your configuration as suggested by the TPM readme.
- Update Rustup by running `rustup update`. This will also attempt to run `rustup self update` when Rustup is installed inside the home directory.
- Run Cargo [install-update](https://github.com/nabijaczleweli/cargo-update)
- Upgrade Emacs packages (You'll get a better output if you have [Paradox](https://github.com/Malabarba/paradox) installed)
- Upgrade [Flutter SDK](https://flutter.dev/docs/development/tools/sdk/upgrading)
- Upgrade [Go packages](https://golang.org/pkg/cmd/go/internal/get/)
- Upgrade [OCaml packages](https://opam.ocaml.org/)
- Upgrade [vcpkg](https://github.com/Microsoft/vcpkg) globally installed packages
- Upgrade [myrepos](https://myrepos.branchable.com/) managed sourcecode repositories
- Upgrade Python packages installed using [pipx](https://github.com/cs01/pipx)
- Upgrade [R globally installed packages](https://github.com/ankane/jetpack)
- Upgrade [stack](https://docs.haskellstack.org/en/stable/README/)
- Upgrade Vim/Neovim packages. Works with the following plugin frameworks:
  - [NeoBundle](https://github.com/Shougo/neobundle.vim)
  - [Vundle](https://github.com/VundleVim/Vundle.vim)
  - [Plug](https://github.com/junegunn/vim-plug)
  - [Dein](https://github.com/Shougo/dein.vim)
  - [Voom](https://github.com/airblade/voom)
- Node
  - Run `yarn global update` if yarn is installed.
  - Run `npm update -g`. In Unix systems other then macOS the step will be
    performed only if`npm root -g` is a path inside your home directory.
- Run `composer global update` if Composer's home directory is inside the home directory of the
  user. Run `valet install` after.
- Upgrade Atom packages
- Run `gem upgrade --user-install` if `~/.gem` exists
- **Linux**: Update Flatpak packages
- **Linux**: Update snap packages
- **Linux**: Run [fwupdmgr](https://github.com/hughsie/fwupd) to show firmware upgrade. (View
  only. No upgrades will actually be performed)
- **Linux**: Run [pihole](https://pi-hole.net/) updater
- Run custom defined commands
- Final stage
  - **Linux**: Run [needrestart](https://github.com/liske/needrestart)
  - **Windows**: Run Windows Update (You'll have to install [PSWindowsUpdate](https://marckean.com/2016/06/01/use-powershell-to-install-windows-updates/))
  - **macOS**: Upgrade App Store applications using [mas](https://github.com/mas-cli/mas)
  - **macOS**: Upgrade the system
  - **FreeBSD**: Run `freebsd-upgrade`
