# gotchas.github.com

### [instal gcc-7 from ppa:ubuntu-toolchain-r/test on ubuntu version earlier then 17.04](https://askubuntu.com/questions/863517/how-do-i-install-g-7-on-ubuntu)


```bash
sudo add-apt-repository ppa:ubuntu-toolchain-r/test
sudo cat  <<- LEADING_TABS_IGNORED >> /etc/apt/preferences
Package: gcc-7
Pin: release n=zesty
Pin-Priority: 990
LEADING_TABS_IGNORED
sudo cat /etc/apt/preferences
sudo apt-get update
sudo apt-get install gcc-7
```
