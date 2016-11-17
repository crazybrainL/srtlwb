# whlin's Mac OS X Guide

### [Software](#software)
* [iterm2](#iterm2)
* [Xcode](#xcode)
* [Virtualbox and Vagrant](#virtualbox-vagrant)
    - Plugin: [vagrant-vbguest]

### Package And Programming Language:
* [homebrew](https://github.com/whlin/srtlwb/blob/master/brew_note.md)
* [dotfilers](https://github.com/whlin/dotfiles)
* [zsh](https://github.com/whlin/srtlwb/blob/master/zshrc_note.md)
* [golang](https://github.com/whlin/srtlwb/blob/master/golang_note.md)
* [python](https://github.com/whlin/srtlwb/blob/master/python_note.md)
* [node](https://github.com/whlin/srtlwb/blob/master/nodejs_note.md)

### To Do
* Update dotfilers installation
* New brew_install.sh for new environment setup.

---

## Software
<a name="iterm2"></a>
### iterm2

Download stable releases from following link: [iterm2]

<a name="xcode"></a>
### Xcode

* Install [Xcode] from the App store or the Apple developer website.
* Install Xcode command line tool:

```sh
$ xcode-select --install
```

<a name="virtualbox-vagrant"></a>
### Virtualbox and Vagrant
#### Install
Download the install package(.dmg) through following links to install virtualbox and vagrant:
* virtualbox: <https://www.virtualbox.org/wiki/Downloads>
* vagrant: <https://www.vagrantup.com/downloads.html>

#### Install Vagrant Plugin
* Reference: [vagrant-vbguest](https://github.com/dotless-de/vagrant-vbguest)

```sh
$ vagrant plugin install vagrant-vbguest
```

<!--github link-->
[Xcode]: <https://developer.apple.com/xcode/>
[iterm2]: <https://www.iterm2.com/downloads.html>
[virtualbox]: <https://www.virtualbox.org/wiki/Downloads>
[vagrant]: <https://www.vagrantup.com/downloads.html>
[vagrant-vbguest]: <https://github.com/dotless-de/vagrant-vbguest>

