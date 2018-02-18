Watson Beat Developer Repo Initial Setup
========================================

Just make sure everyone is on the same page, please make sure you have downloaded the Watson Beat project before proceeding.

Anytime `you see something in gray like this` that indicates its a terminal command for you to execute

Go to A. if your operating system is Windows.
Go to B. if your operating system is anything other than Windows.

## A. Windows

1. Go to your Start Menu, type in the search "cmd". Right click on it, and "Run as Administrator". 
2. First, make sure if python has been installed at any point in time. type ```python -V```
3. If you had a ```python is not recognized as an internal or external command``` error then we need to install python!

* If you did get a Python version, check if it is Python 2.7. Note: If your Python version is Python 3, you will have to complete an additional step. First, install [Pip](https://bootstrap.pypa.io/get-pip.py) and then install [virtualenv](https://fernandofreitasalves.com/virtualenv-tutorial-for-beginners-windows/), then proceed.

4. To install Python and Pip, go through these detailed steps here - [Set up Python and Pip](https://github.com/BurntSushi/nfldb/wiki/Python-&-pip-Windows-installation)

5. Remember to open a new command prompt ("cmd" from Step 1) and test out if python and pip are installed! ```python -V``` and ```pip freeze```. 

Once you have this done, you can install the dependencies for the project to run!

6. `pip install numpy python-midi requests`

You are done with this step! 


## B. Not Windows

Pre-reqs

python
pip

Dependencies

numpy
python-midi
requests

### MAC OS

#### Install homebrew

Directions were found [here](http://sourabhbajaj.com/mac-setup/Homebrew/README.html), as listed below

1. `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

2. "One thing we need to do is tell the system to use programs installed by Hombrew (in /usr/local/bin) rather than the OS default if it exists. We do this by adding /usr/local/bin to your $PATH environment variable":

`echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile`

3. Execute the command `brew` in terminal window and see if you get a bunch of information pertaining to `brew`, if you do - homebrew installed correctly!


#### Install python

brew install python

d) check if python has been installed

python -V

This command should give you the python version

#### Install pip

a) sudo easy_install pip

How to Install Python on Mac:
http://docs.python-guide.org/en/latest/starting/install/osx/

#### Install dependencies for the project

`pip install numpy python-midi requests`

you are done with this step!

### Linux

Okay, I am assuming you know a bit of what you are doing per you using Linux

#### How to install Python in ubuntu linux:

Follow these directions: https://tecadmin.net/install-python-2-7-on-ubuntu-and-linuxmint/
Listed below are the directions per this link given.

a) Install dependencies
`sudo apt-get update` 
<br>
`sudo apt-get install build-essential checkinstall`
<br>
`sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev`

b) Download source

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

#### Install pip

https://tecadmin.net/install-pip-linux/

#### Install dependencies

`pip install numpy python-midi requests`

you are done with this step!
