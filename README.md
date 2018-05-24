# Instruction with some essentials to Git/html/JS and so on.

### VM creation / Linux installation:
1. Install Git, Vagrant and Webstorm (for further activity)
1. Open Git Bash
1. Choose later VM folder
1. Insert: `vagrant init ubuntu/_version(xenial64)_` `vagrant up` `vagrant ssh`
1. Open /vagrant folder (synced with main OS) `cd /vagrant`

**You are awesome** 

### Working with repository:
1. Open and register on **github.com**
1. Create an empty repository
1. Open Webstorm 
**!!!So on everything will be explained as in the Webstorm!!!**
1. Create a new project in your VM folder
1. In plugins install **markdown support** (for .md files)
1. Create new file with the name **README.md**
1. Write something there
1. Open terminal and `vagrant up` `vagrant ssh` your previously created VM
1. Insert: `ssh-keygen -b 4096 -C "_your email_"` in order to create SSH-key which is used to connect to your git repository
1. Insert: `cat ~/.ssh/id_rsa.pub` to show your SSH-key
1. Copy it and go to **https://github.com/settings/keys** and add your SSH-key
1. Insert: `git init` and `git remote add origin git@github.com:_username_/_rep.name_.git` to make a connection with your repository
1. Insert `git config user.name "_Your name_"` and `git config user.email "_your email_"` in order to be identified

**You are the best**

### Git / Linux commands:
* `git clone git@github.com:_username_/_rep.name_.git` - establish the connection your PC <==> Github repository
* `git commit -a -m "_Comment_"` - send changes to local repository
* `git push [-u origin master]` - send changes to your github repository
* `mkdir _folder name_` - create new folder
* `cd _folder name_` - go to folder
* `cd ..` - go one folder back
* `git status` - check whether there are some uncommited changes
* `git rm --cached __file name_` - delete file from Git

### Working with nginx:
1. Insert command `sudo apt-get install nginx`
1. Open `/etc/nginx/sites-enabled/default`
1. Change `server _name _;` and `root /vagrant;`
1. Open **Vagrantfile**
1. Uncomment `config.vm.network "forwarded_port", guest: 80, host: 80` and `config.vm.network "private_network", ip: "192.168.33.10"`
1. Restart VM (`vagrant reload`)
1. Insert `sudo service nginx start`

**You are the coolest person**