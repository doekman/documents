Ubuntu Installation
===================

Maybe we should also fork/create a project to do this automatically.
http://yuez.me/cong-ling-da-jian-he-pei-zhi-osxkai-fa-huan-jing/


Pre-Installation
----------------

Backup: .bashrc .vimrc .vim .zshrc .mozilla .thunderbird .gitconfig


Installation
------------

Ubuntu16.04, there is a gxfboot.c32 error,  after the "boot:" promote, 
fix it manually, input "tab" => "live" or "liveinstall" => press ENTER


Post-Configurations
-------------------

Restore: .bashrc .vimrc .vim .mozilla .thunderbird .gitconfig
(If you have not formated the /home partition, you don't need to do this)

All Settings => Languages
All Settings => Dispalys
All Settings => Appearance => Behavior => Auto-hide the Launcher


Post-Intallations
-----------------

First time Upgrade::

    sudo apt-get update && sudo apt-get upgrade

Change default shell::

    sudo dpkg-reconfigure dash --> select No for set bash as default shell

Basic packages::

    sudo apt-get install git-core git-email kdiff3 gitg
    sudo apt-get install vim ctags g++ tofrodos quilt tree
    sudo apt-get install rar unrar p7zip p7zip-rar p7zip-full
    sudo apt-get install ntfs-3g ntfs-config
    sudo apt-get install python-pip

Packages for Developer::

    sudo apt-get install \
        autoconf autoconf2.64 autoconf-doc autoconf-archive \
        glib2.0 glib2.0-data glib2.0-dev \
        libdbus-1-dev libdbus-glib-1-dev \
        libtool libtool-doc \
        texlive texinfo libxml-parser-perl libxml-simple-perl \
        diffstat texi2html gawk chrpath \
        gcc-multilib g++-multilib  libc6-dev-i386 libzip-dev \
        libc6-i386

Installing the ia32 libs needs the ubuntu 13.04 sources,
because this package is droped after this ubuntu 13.04::

    sudo -i
    cd /etc/apt/sources.list.d
    echo "deb http://old-releases.ubuntu.com/ubuntu/ raring main restricted universe multiverse" > ia32-libs-raring.list
    apt-get update
    apt-get install ia32-libs
    rm /etc/apt/sources.list.d/ia32-libs-raring.list
    apt-get update


youtao-dict
-----------

To avoid gstreamer0.10-plugins-ugly dependence issue, use deepin version but not ubuntu version.
http://codown.youdao.com/cidian/linux/youdao-dict_1.1.0-0-deepin_amd64.deb

sudo apt-get install python3-pyqt5 python3-xlib
sudo apt-get install tesseract-ocr tesseract-ocr-chi-sim tesseract-ocr-chi-tra
sudo apt-get install ttf-wqy-microhei
sudo apt-get install python3-pyqt5.qtmultimedia python3-pyqt5.qtquick python3-pyqt5.qtwebkit
sudo apt-get install qtdeclarative5-controls-plugin libqt5multimedia5-plugins
sudo dpkg -i youdao-dict_1.1.0-0-deepin_amd64.deb


python3
-------

Maybe the python3 is already installed, but you need to install pip3::

    sudo apt-get install python3-pip

Then you can install python3 modules using ``sudo pip3 install xxx``
