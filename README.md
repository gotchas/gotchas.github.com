# gotchas.github.com

### [instal gcc-7 from ppa:ubuntu-toolchain-r/test on ubuntu version earlier then 17.04](https://askubuntu.com/questions/863517/how-do-i-install-g-7-on-ubuntu)


```bash
sudo add-apt-repository -y ppa:ubuntu-toolchain-r/test
sudo cat <<- LEADING_TABS_IGNORED  | sudo tee -a /etc/apt/preferences
Package: gcc-7
Pin: release n=zesty
Pin-Priority: 990
LEADING_TABS_IGNORED
sudo cat /etc/apt/preferences
sudo apt-get update
sudo apt-get install gcc-7
```
note how here document can be redirected to a file with root priviledges: pipe to a `tee -a` command run by root
### [preparation on ubuntu to build gcc from source code tarball](https://help.ubuntu.com/community/CompilingEasyHowTo)

```bash
sudo apt-get install build-essential checkinstall
sudo apt-get install cvs subversion git-core mercurial
sudo chown $USER /usr/local/src
sudo chmod u+rwx /usr/local/src
```
