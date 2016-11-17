# Homebrew

## Install

```sh
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### What Does Homebrew Do?
Homebrew installs packages to their own directory and then symlinks their files into /usr/local.

### Install Packages
1. cmake  
2. cscope 
3. ctags  
4. lua    
5. tree
    - This progeam can show the file list.
6. tmux
7. ...

```sh
$ brew install cmake cscope ctags lua tree tmux ...
```

After installing, you could

1. Use **tree** to make sure that brew install succeeds.
2. **cd** to /usr/local/bin and use **ls -l** to make sure that symbolic link is correct.
3. Use **which** to find out where a program is located.  

```sh
# Step 1.
$ tree /usr/local/Cellar -L 1 (layer one)
/usr/local/Cellar
├── ...
├── cmake
├── cscope
├── ctags
├── lua
├── tree
├── ...

# Step 2.
$ cd /usr/local/bin
$ ls -l
...
cmake -> ../Cellar/cmake/3.6.3/bin/cmake
cscope -> ../Cellar/cscope/15.8b/bin/cscope
ctags -> ../Cellar/ctags/5.8_1/bin/ctags
lua -> ../Cellar/lua/5.2.4_4/bin/lua
tree -> ../Cellar/tree/1.7.0/bin/tree
...

# Step 3.
$ which cmake cscope ctags lua tree
/usr/local/bin/cmake
/usr/local/bin/cscope
/usr/local/bin/ctags
/usr/local/bin/lua
/usr/local/bin/tree
```

### vim
#### Install vim
```sh
$ brew install vim --with-lua --with-python
```

#### Setup [vimfilers]
[Important] There are some vim plugin for python, golang and nodeJS use these command to install YouCompleteMe or other plugins so you have to finish python, golang and nodeJS installation first.

#### Install haskell
```sh
$ brew install haskell-platform
$ cabal install hasktags
$ cabal install hlint
```

## Reference
[homebrew](http://brew.sh/)
