# How to set up a server running Agoric for begginers
## Introduction
This guide is written for people that have absolutely no or little experience with terminal and remote server configuration. For that see the official Agoric docs here https://github.com/Agoric/agoric-sdk/wiki/Validator-Guide
### What will you need to start
1. a computer running Linux/MacOS X/Windows.
2. VPS/dedicated (2CPU 4RAM 40GB)  with full root access.You’ll need to open port 26656 to connect to the Agoric peer-to-peer network. As the usage of the blockchain grows, the server requirements may increase as well, so you should have a plan for updating your server as well.
3. Ubuntu 20.04.
4. courage and patience if this is the first time you are managing server.
## A complete step by step **Agoric Validator installation**
### Install Node.js (You can skip this step if you already have installed Node.js)
Node.js is a JavaScript platform for general-purpose programming that allows users to build network applications quickly. By leveraging JavaScript on both the front and backend, Node.js makes development more consistent and integrated.
```
# Download the nodesource PPA for Node.js
curl https://deb.nodesource.com/setup_12.x | sudo bash

# Download the Yarn repository configuration
# See instructions on https://legacy.yarnpkg.com/en/docs/install/
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

# Update Ubuntu
sudo apt update && sudo apt upgrade -y

# Install Node.js, Yarn, and build tools
# Install jq for formatting of JSON data
sudo apt install nodejs=12.* yarn build-essential jq -y
```
