# Installing multiple instances of Ubuntu in WSL2

## Step 1: Install the latest version of Ubuntu in WSL2
wsl --Install

## Step 2: Download the Ubuntu WSL tarball
https://cloud-images.ubuntu.com/releases/hirsute/release/ubuntu-21.04-server-cloudimg-amd64-wsl.rootfs.tar.gz

## Step 3: Install the second instance of Ubuntu in WSL2
wsl --import <Distribution Name> <Installation Folder> <Ubuntu WSL2 Image Tarball path>

### sample line
wsl --import angular13 "c:\wsls\angular13" ubuntu-21.04-server-cloudimg-amd64-wsl.rootfs.tar.gz

## Step 4: Login to the second instance of Ubuntu in WSL2
wsl -d <Distribution Name>

## Step 5: Setup user accounts
run the following commands where <USERNAME> is the new username
NEW_USER=<USERNAME>
useradd -m -G sudo -s /bin/bash "$NEW_USER"
passwd "$NEW_USER"

## Step 6: Configure default user
Next, we need to configure Ubuntu to log in as your new user by default instead of root.
To do so, run the below command: paste the entire block of code below into your teminal and press enter.

tee /etc/wsl.conf <<_EOF
[user]
default=${NEW_USER}
_EOF

## Step 7: Login as the new user
First, exit the WSL by running logout, then shutdown the second Ubuntu by running

logout
wsl -t <Distribution Name>
 // wsl --shutdown <Distribution Name>
Finally, login to the second instance of Ubuntu again:

wsl -d <Distribution Name>

## Step 8: Update Ubuntu
sudo apt-get update
sudo apt-get dist-upgrade

## wsl 1 is better for angular if the files will be in windows partition
wsl --set-version <Distribution Name> 1

## Link of the web site 
https://cloudbytes.dev/snippets/how-to-install-multiple-instances-of-ubuntu-in-wsl2