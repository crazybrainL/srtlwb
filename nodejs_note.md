# NodeJS note
#### Install NodeJS
```sh
$ brew install nodeJS
```

#### What is npm?
npm makes it easy for JavaScript developers to share and reuse code, and it makes it easy to update the code that you're sharing.

#### what is ~/.npm dir for?
~/.npm is a cache that npm uses to avoid re-downloading the same package multiple times. There's no harm in removing it. You can empty it with the command:
```sh
npm cache clean
```

#### Installing npm packages locally or globally
There are two ways to install npm packages: locally or globally. You choose which kind of installation to use based on how you want to use the package.

If you want to depend on the package from your own module using something like Node.js' require, then you want to install locally, which is npm install's default behavior. 

On the other hand, if you want to use it as a command line tool, something like the grunt CLI, then you want to install it globally.

#### [Installing npm packages locally](https://docs.npmjs.com/getting-started/installing-npm-packages-locally)

A package can be downloaded with the command
```sh
$ npm install <package_name>
```
This will create the node_modules directory in your current directory(if one doesn't exist yet), and will download the package to that directory.

#### [Installing npm packages globally](https://docs.npmjs.com/getting-started/installing-npm-packages-globally)

To download packages globally, you simply use the command
```sh
$ npm install -g <package_name>
```
The package will be installed in the global package set: node_modules (Path: /usr/local/lib/node_modules)

Reference: 
* [How to Install Node.js and NPM on a Mac](http://blog.teamtreehouse.com/install-node-js-npm-mac)
* [nodeJS document] [node]

[node]: <https://docs.npmjs.com/>
