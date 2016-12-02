# zsh note

#### Notice

Install zsh-rc by using [dotfiles](https://github.com/whlin/dotfiles)

#### Install zsh
```sh
$ brew install zsh

# Change to new zsh (/usr/local/bin/zsh).
$ chsh -s /usr/local/bin/zsh
```

Check install succeeds
```sh
# Step 1.
$ tree /usr/local/Cellar -L 1 (layer one)
/usr/local/Cellar
├── ...
├── zsh
├── ...

# Step 2.
$ cd /usr/local/bin/
$ ls -l
zsh -> ../Cellar/zsh/5.2/bin/zsh

# Step 3.
$ which zsh
/usr/local/bin/zsh
```

#### Install oh-my-zsh
```sh
$ sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

If you want to install other path you can use git clone and remeber to change .zshrc setting.
```sh
$ git clone git://github.com/robbyrussell/oh-my-zsh.git [your_path]
```

#### Install zsh-completions
Reference: [icarus4]
```sh
$ brew install zsh-completions  
```

Check install succeeds, you can use **ls** command to make sure that package install succeeds.
```sh
$ ls /usr/local/share
aclocal         doc             git-gui         info            systemtap       zsh-completions
autoconf        emacs           gitk            lua             vim
cmake           git-core        gitweb          man             zsh
```

#### Setup [zshrc]
```sh
$ cd ~/Documents/
$ git clone https://github.com/whlin/zshrc.git
$ cd ~/Documents/zshrc
$ ./install_unix.sh
```

[icarus4]: <http://icarus4.logdown.com/posts/177661-from-bash-to-zsh-setup-tips>
