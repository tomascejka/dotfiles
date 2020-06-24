# Compton
What is [compositor](https://dev.to/l04db4l4nc3r/compositors-in-linux-1hhb#what-are-compositors) and why you should use it. It is not critial but useful to use it.

## Install
Install compton via package manager (I am using debian/apt)
```bash
$ apt-get install compton
```

## Configuration
After instalation create file in ~/.config/compton.conf

```bash
$ touch ~/.config/compton.conf
```

Content of compton file could be taken from:
* https://github.com/chjj/compton/blob/master/compton.sample.conf << oficial 
* https://duncanlock.net/blog/2013/06/07/how-to-switch-to-compton-for-beautiful-tear-free-compositing-in-xfce/ << contains comments 
... and restart compton (see below).

## Restart
Change .conf file (see above) and restart `compton` until you are success with configuration (eg. inactive window transparency)

```bash
$ pkill compton && compton
```

## Sources
* https://github.com/chjj/compton << homepage
* https://dev.to/l04db4l4nc3r/compositors-in-linux-1hhb << Compositors in linux
* https://manpages.debian.org/buster/compton/compton.1.en.html << manpage for debian
* https://duncanlock.net/blog/2013/06/07/how-to-switch-to-compton-for-beautiful-tear-free-compositing-in-xfce/ << contains example of compton.conf file
