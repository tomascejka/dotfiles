# Compton
What is [compositor](https://dev.to/l04db4l4nc3r/compositors-in-linux-1hhb#what-are-compositors) and why you should use it. Tool [compton](https://github.com/chjj/compton) is compositor implemetation. It is not critial component but it's useful to use it.

## Install
Install compton via package manager (I am using debian/apt)
```bash
$ apt-get install compton
```

## Configuration
After instalation create file in `~/.config/compton.conf`:

```bash
$ touch ~/.config/compton.conf
```

Content of compton file could be taken from:
* oficial [compton.conf](https://github.com/chjj/compton/blob/master/compton.sample.conf) file
* another [compton.conf](https://duncanlock.net/blog/2013/06/07/how-to-switch-to-compton-for-beautiful-tear-free-compositing-in-xfce/) which contains comments

... and restart compton (see below).

## Restart
Change .conf file and restart `compton`:

```bash
$ pkill compton && compton
```
... repeat the way until you are success with configuration (eg. inactive window transparency)

## Cooperation with window manager
I am Awesome fan so there is a way how to cooperate with one; edit main configuration file ~/.config/awesome/rc.lua:

```bash
$ vi ~/.config/awesome/rc.lua

# rc.lua; add these lines anywhere
-- Autorun
awful.spawn.with_shell("compton")
```
## Sources
* https://github.com/chjj/compton << homepage
* https://dev.to/l04db4l4nc3r/compositors-in-linux-1hhb << Compositors in linux
* https://manpages.debian.org/buster/compton/compton.1.en.html << manpage for debian
* https://dev.to/l04db4l4nc3r/compositors-in-linux-1hhb
