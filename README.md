# Quake Team Fortress Server

## Overview
This repository has all the files needed to run a Team Fortress server on a Linux machine.

1. Clone this repo `git clone https://github.com/rictorres/quake-team-fortress-server.git` or download the [zipball](https://github.com/rictorres/quake-team-fortress-server/archive/master.zip)
2. Run `./start-public` or `start-priv[#]` (it will be attached to a different screen called `qwtf-pub` or `qwtf-priv[#]`, useful if you're using SSH)
3. Profit!


## Requirements
- Linux server (preferably Ubuntu)
- SSH
- Screen


## Installation
```
$ sudo apt-get update
$ sudo apt-get install screen
$ chmod 755 start-public
$ chmod 755 start-priv1
$ chmod 755 start-priv2
```


## Running
- Public server (default port 27500)
  ```
  ./start-public
  RUNNING TEAM FORTRESS PUBLIC SERVER ON PORT 27500
  ```
- Private server (default port 27501)
  ```
  ./start-priv1
  RUNNING TEAM FORTRESS PUBLIC SERVER ON PORT 27501
  ```
The above commands will first execute `./fortress/server.cfg` and then a specific config for each server (public or private)
You can edit `start-public` and `start-priv[#]` as needed.


## Additional info
- To get a list of `screens` in use:
  `$ screen -list`
- To re-attach the screen
  `$ screen -r qwtf-pub`
- To detach the screen and go back to your original SSH session
  `CTRL + A + D`


## Credits
- [SLUSAMSON](http://www.bluemunkey.com/?p=124)