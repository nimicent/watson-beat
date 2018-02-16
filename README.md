The Watson Beat - Julia's Edit
===============

If you are a beginner - I will provide guidance for Windows and Mac OS. 
If you have Linux, I am going to make a vote of confidence and assume you know where your terminal is.

Using machine learning to spur human creativity is _so_ 2018!  Watson has used
a combination of reinforcement learning and neural networks to create the Watson Beat.

Inputs
------
 - a simple 10-20 second melody file in midi format
 - parameters for the creativity engine

Outputs
-------
 - Several layers of music in midi format that Watson created using your input
   as inspiriation

Getting Started
===============
This repo, is all the code for the The Watson Beat.  It all runs locally using 
the terminal.  To run it, there are a few things you need set up on your local computer first, like python 🐍!

Download the Watson Beat Project
=================================

1. Go to the landing page for the Watson Beat repository, here is a link to the 'root' directory for the project.
[open this link in a new tab.](https://github.com/watson-music/watson-beat)
</br>
Press the green button, then press "Download ZIP"

Do you have anything to unzip ZIP files on your computer? 

If not, you can find one on [FileHippo](https://filehippo.com/software/archiving/) like 7Zip.

Please unzip the project folder from here using what program you have to perform this extraction.

![image](https://i.imgur.com/VqyNwuF.jpg)

![image](https://i.imgur.com/dIQROX2.png)

2. If you know terminal commands for the operating system you are working on, ```cd``` into the project folder you downloaded.

If you do not know terminal commands, you are about to learn them! Follow this link: [Instructions on calling the directory](https://github.com/watson-music/watson-beat/blob/master/directory.md)

<hr>


Set you machine up for development
------------------------------------------------------
[Here are some directions to get your machine set up to run code](./initial_setup.md) 


Install Project Level Dependencies
----------------------------------
Open your terminal, and navigate to the directory where your Watson Beat downloaded project is on your computer.  If you do an `ls` you should see this file, `README.md`, and the
specfic python requirements for this project are in `requirements.txt`.  
You can install the specific python packages you need for your
Watson Beat Client with the following command (again, make sure you are in this directory):

`pip install -r requirements.txt`


Ready to Run
------------
There are two main ingredients to prepare to create your song with The Watson Beat.  First, you need
a midi file with a simple melody.  Best results come when you keep this short, about 10 seconds.  Also,
leave some space between your notes to give the creativity engine some wiggle room.

The second ingredient is the `ini` file.  The `ini` file give the creativity engine all of the spices
to use, including time signature, "mood," and tempo.  [Read this to learn more about ini files](./customize_ini.md).


```
Usage:
usage: wbDev.py [-h] [-i INIFILE] [-m MIDIFILEPATH] [-o OUTPUTPATH] [-u]

optional arguments:

  -h               show this help message and exit

  -i INIFILE       Store the ini File

  -m MIDIFILEPATH  Midi File Path

  -o OUTPUTPATH    Path were all the output mid files are stored (default ./output/)

  -u               usage
```

To run, clone this git project in your filesystem if you haven't already.  Open a terminal window, navigate to the 
project home `$WB_HOME` (for example, this might be `/Users/Moe/watson-beat`)

`cd $WB_HOME/src` 

Now, in the current working directory, there is a python script that will call the code, `wbDev.py` with the
parameters you pass it. To get help, just pass it the `-h` flag:

`python wbDev.py -h`

If you pass it no paramaters, 

`python wbDev.py`

it will use the default Ini file `$WB_HOME/src/Ini/Space.ini`, the default midi
file `$WB_HOME/src/Midi/mary.mid`, and output all the files to `./output/`

To pass in specific midi and ini files use the following syntax:

`python wbDev.py -i Ini/ReggaePop.ini -m Midi/mary.mid -o /Users/Moe/midifiles/`


Putting it together
-------------------
This is where you get to have some fun! Now, you have a set of midi files, you can use your favorite 
audio tools to apply virtual instruments to the sections and mix them together into a song. 

Audio Tools
-------------------
Unix: [Download Garageband](https://www.apple.com/mac/garageband/)
Windows, Linux: [You can use MuseScore](https://musescore.org/en/download)

HAPPY COMPOSING!


Video Tutorials
-------------------
[How to Change the Length of a Composition](https://www.youtube.com/watch?v=suND0biUTKQ&feature=youtu.be)

[Importing MIDI Files](https://www.youtube.com/watch?v=0mWz3h1ZiJE&feature=youtu.be)

[How to Customize Moods Part 1](https://www.youtube.com/watch?v=OUDXpJJhoK8&feature=youtu.be)

[How to Customize Moods Part 2](https://www.youtube.com/watch?v=PSqLVEJexrU&feature=youtu.be)


License
-------
See [LICENSE.txt](./LICENSE.txt)

###### Original Authors: Janani Mukundan, Jeremy Hodge, and Richard Daskas 
###### Assign Pull Requests to: amchaney

