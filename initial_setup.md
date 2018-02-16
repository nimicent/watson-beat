Watson Beat Developer Repo Initial Setup
========================================

Just make sure everyone is on the same page, please make sure you have downloaded the Watson Beat project before proceeding.

Go to A. if your operating system is Windows.
Go to B. if your operating system is anything other than Windows.

## A. Windows

1. Go to your Start Menu, type in the search "cmd". Right click on it, and "Run as Administrator". 
2. First, make sure if python has been installed at any point in time. type ```python -V```
3. If you had a ```python is not recognized as an internal or external command``` error then we need to install python!

* If you did get a Python version, check if it is Python 2.7. Note: If your Python version is Python 3, you will have to complete an additional step. First, install [Pip](https://bootstrap.pypa.io/get-pip.py) and then install [virtualenv](https://fernandofreitasalves.com/virtualenv-tutorial-for-beginners-windows/), then proceed.

4. To install Python and Pip, go through these detailed steps here - [Set up Python and Pip](https://github.com/BurntSushi/nfldb/wiki/Python-&-pip-Windows-installation)

5. Remember to open a new command prompt ("cmd" from Step 1) and test out if python and pip are installed! ```python -V``` and ```pip freeze```. 

## B. Not Windows

Pre-reqs

python
pip

Dependencies

numpy
python-midi
requests

#### MAC OS
How to Install python on osx:
http://docs.python-guide.org/en/latest/starting/install/osx/


a) Install homebrew

/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

Add the following line to the bottom of the  ~/.profile file

export PATH=/usr/local/bin:/usr/local/sbin:$PATH

c) Install python

brew install python

d) check if python has been installed

python -V

This command should give you the python version

How to install pip in osx

a) sudo easy_install pip


#### Linux
How to install python in ubuntu linux:

From source: https://tecadmin.net/install-python-2-7-on-ubuntu-and-linuxmint/

a) install dependencies
sudo apt-get update ; sudo apt-get install build-essential checkinstall ; sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev

b) download source

cd /usr/src ; wget https://www.python.org/ftp/python/2.7.13/Python-2.7.13.tgz ; tar xzf Python-2.7.13.tgz

c) compile python source

cd Python-2.7.13

sudo ./configure

sudo make install

d) check the python version

python -V

This command should give you the python version

or using apt-get

a)sudo apt-get install python2.7

Now, go back to the [README](./README.md)

