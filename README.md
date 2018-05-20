# linux-environment-setup

## Basics:
### Update
* ```sudo apt-get update```
### Vim Setup
* Install Vim
	* ``` sudo apt-get install vim```
### Alias Setup
* ``` echo "alias vz="vim ~/.zshrc"" >> ~/.zshrc```
* ``` echo "alias sz="source ~/.zshrc"" >> ~/.zshrc```
### Zsh Setup
* Check shell info: 
	* ```echo $0``` : check **current** shell
	* ```echo $SHELL``` : check **default** shell
* Change shell to zsh:
	* ```sudo apt install zsh```
 	* ```chsh -s $(which zsh)```
	* close current terminal and open a new one and populate ~/.zshrc
 	* logout and log back in if any problems happened
* Install "Oh My Zsh":
	* Install curl: ``` sudo apt-get install curl```
	* Install git: ``` sudo apt-get install git-core```
	* ``` -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"```
	
	  (it should automatically edit your ~/.zshrc and ready for use)
* Install Auto suggestion:
	* ``` git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions```
	* ``` echo "source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh" >> ~/.zshrc ```
	* ``` source ~/.zshrc```
### Terminator Setup
* Install Terminator
	* ``` sudo add-apt-repository ppa:gnome-terminator```
	* ``` sudo apt-get update```
	* ```ssudo apt-get install terminator```

### Guake Setup
* Clone Guake Repo at https://github.com/Guake/guake
* cd to guake local guake repo and  ```./dev.sh --install```
	
### Sougou Pingyin Setup
sougou is based on fcitx, yet ubuntu is based on iBus. Therefore we need to first install fcitx and then intall sougou.

* install fcitx
	* get source: ```sudo add-apt-repository ppa:fcitx-team/nightly```
	Notice: this ppa is no longer maintained, hence you might need to go to "software and updates/other software"to disable it before apt-get update 
	* update system: ```sudo apt-get update```
	* install fcitx: ```sudo apt-get install fcitx```
    * install config tool: ```sudo apt-get install fcitx-config-gtk```
    * install table-all: ```sudo apt-get install fcitx-table-all```
    * install im-switch: '''sudo apt-get install im-switch'''
    * check if fcitx is installed correclty by search its name in search bar

* install sougou
    * go to sougou website and download the linux version
    * install: ```sudo dpkg -i package_name```

* configure
    * open ***system settings -> language support***, and change ***keyboard input method system *** from ***iBus***
    to ***fcitx***
    * logout
    * go to upright corner on the screen and go to ***Peference*** (note: might be in Chinese ***She Zhi***), and add sougou pingyin
	
Manually change "input method" on upright corner of the screen, and then you should be able use ***Shift*** key to switch between two mthods.
Reference: http://www.linuxdiyf.com/linux/22075.html
		
