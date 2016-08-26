# Installation git-1.8.5
Installation git-1.8.5 on centos 6

yum update -y

##show git version
git --version

##uninstall lower git version
yum remove git -y

##install some packages dependencies
yum install -y libperl gcc curl-devel expat-devel gettext-devel openssl-devel zlib-devel perl-devel

##download git-1.8.5
```
cd /usr/src
wget https://git-core.googlecode.com/files/git-1.8.5.3.tar.gz
tar -xzf git-1.8.5.3.tar.gz
cd git-1.8.5.3
make prefix=/usr/src/git all
make prefix=/usr/src/git install
echo "export PATH=$PATH:/usr/src/git/bin" >> /etc/bashrc
source /etc/bashrc
```
##check git version
git --version


