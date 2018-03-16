# linux
### Day by day and Step by step
---
## Day 0: Try readme.md
# This is header 1
## This is header 2
### This is header 3
##### This is header 4
---
> this is text-field
---

## Day 1: Git to Github ##

### 1-1:install git on ubuntu
type in terminal: "sudo apt-get install git"

### 1-2:connect github to localhost
##### 1-2-1 sign in github 
##### 1-2-2 press the icon and chose your profile
##### 1-2-3 choose Repositories 
##### 1-2-4 Create a new repositories and go into it
##### 1-2-5 Click "Clone or download" and copy "git@github.com:*accountName/*repositoriesName.git"
##### 1-2-6 go to the folder where you wanna place your files in local
##### 1-2-7 right-click the folder > open in Terminal
##### 1-2-8 keyin 'git init' to create a git in folder
##### 1-2-9 keyin 'git clone git@github.com:*accountName/*repositoriesName.git

### 1-3:Add SSH Key
to skip enter userName and pw while "git push" 
##### 1-3-1 check ssh key
open terminal and type

	$ cd ~/.ssh
	# Check if there's a directory named ".ssh" in user directory

it will show "No such file or directory" then you can start to add a new one, if not try delete it and create a new one

##### 1-3-2 create a new ssh keys

	$ ssh-keygen -t rsa -C "yourEmail@xxx.com"
	
Generating public/private rsa key pair.
Enter file in which to save the key (/home/userName/.ssh/id_rsa):[Enter] 

	hit Enter to keep create /.ssh

Created directory '/home/userName/.ssh'.
Enter passphrase (empty for no passphrase):

	hit Enter 
 
Enter same passphrase again: 

	Enter again

Your identification has been saved in /home/userName/.ssh/id_rsa.
Your public key has been saved in /home/userName/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:jfldajfldsajfkjsaljflsajlvz  userName@email.com
The key's randomart image is:
+---[RSA 2048]----+
|.................|
+----[SHA256]-----+

if you didn't install geomview before plz keyin 

	$ sudo apt-get install geomview

after that key in

	$ clip < ~/.ssh/id_rsa.pub
	$ gedit ~/.ssh/id_rsa.pub

it will open id_rsa.pub with gedit, plz copy all the text in the id_rsa.pub and open github in browser

	account > setting > SSH and GPG keys > New SSH Key

give a name and paste what you copied from id_rsa.pub
 
