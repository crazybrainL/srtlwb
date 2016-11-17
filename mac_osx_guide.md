# whlin's Mac OS X Guide

### Software
* [iterm2]
* Xcode

### Package And Programming Language:
* [homebrew]
* [dotfilers]
* zsh
    - Install zsh
    - Install oh-my-zsh
    - Install zsh-completions
    - Setup [zshrc]
* [golang]
* python
    - Simple Python version management: [pyenv]
* [node]
* vim
    - Setup [vimfilers]
* haskell
* [virtualbox] and [vagrant]
    - Plugin: [vagrant-vbguest]
* Setup [rc]

### To Do
* Update dotfilers installation
* New brew_install.sh for new environment setup.

---

## Software
### iterm2

Download stable releases from following link: [iterm2]

### Xcode

* Install [Xcode] from the App store or the Apple developer website.
* Install Xcode command line tool:

```sh
$ xcode-select --install
```

## Package And Programming Language:
### Golang

[Download the archive](https://golang.org/dl/) and extract it into /usr/local, creating a Go tree in /usr/local/go.
For example:
```sh
tar -C /usr/local -xzf go$VERSION.$OS-$ARCH.tar.gz
```

Add /usr/local/go/bin to the PATH environment variable. (~/.zshec has already setting)
```sh
export PATH=$PATH:/usr/local/go/bin
```

### vim
#### Install vim
```sh
$ brew install vim --with-lua --with-python
```

#### Setup [vimfilers]
[Important] There are some vim plugin for python, golang and nodeJS use these command to install YouCompleteMe or other plugins so you have to finish python, golang and nodeJS installation first.

```sh
$ cd ~/Documents
$ git clone https://github.com/whlin/vimfilers.git
$ cd vimfiles
$ ./install_unix.sh
```

#### Install haskell
```sh
$ brew install haskell-platform
$ cabal install hasktags
$ cabal install hlint
```

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
[rc]: <https://github.com/whlin/rc>
[zshrc]: <https://github.com/whlin/zshrc>
[vimfilers]: <https://github.com/whlin/vimfilers>

<!--software and package link-->
[homebrew]: <http://brew.sh/>
[Xcode]: <https://developer.apple.com/xcode/>
[iterm2]: <https://www.iterm2.com/downloads.html>
[icarus4]: <http://icarus4.logdown.com/posts/177661-from-bash-to-zsh-setup-tips>
[virtualbox]: <https://www.virtualbox.org/wiki/Downloads>
[vagrant]: <https://www.vagrantup.com/downloads.html>
[vagrant-vbguest]: <https://github.com/dotless-de/vagrant-vbguest>

<!--programming language link-->
[golang]: <https://golang.org/doc/install>
[pyenv]: <https://github.com/yyuu/pyenv-installer>
[node]: <https://docs.npmjs.com/>
