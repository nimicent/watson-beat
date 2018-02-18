The Watson Beat Workshop
===============

## AGENDA

Step 1: Download the project
<br>
Step 2: Set up for development and install dependencies
<br>
Step 3: Choosing a song (MIDI file)!
<br>
Step 4: Choose how Watson interpretes your song (ini file!)
<br>
Step 5: Create a folder for music and run terminal command with MIDI and ini selected
<br>
Step 6: You now have a song from Watson. Open the auio editor
<br>
Step 7: Import MIDI files from Watson to audio editor
<br>
Step 8: Apply virtual instruments to the song 
<br>
Step 9: Export the file as a .wav or .mp3
<br>
Step 10: Listen to it 800 thousand times, email it to friends & fam or put on your resume "made music with Watson DBN"!
<br>


If you are a beginner - I will provide guidance for Windows and Mac OS. 
If you have Linux, I am going to make a vote of confidence and assume you know where your terminal is.

Using machine learning to spur human creativity is _so_ 2018!  Watson has used
a combination of reinforcement learning and neural networks to create the Watson Beat.

This repo, is all the code for the The Watson Beat.  It all runs locally using 
the terminal.  To run it, there are a few things you need set up on your local computer first, like python 🐍!

Inputs
------
 - a simple 10-20 second melody file in midi format
 - parameters for the creativity engine

Outputs
-------
 - Several layers of music in midi format that Watson created using your input
   as inspiriation

# Start Here!

Step One: Download the Watson Beat Project
=================================

1. Go to the top of this page for the Watson Beat repository, and download it. Images of how to do this are below.

Press the green button, then press "Download ZIP"

Do you have anything to unzip ZIP files on your computer? 

If not, you can find one on [FileHippo](https://filehippo.com/software/archiving/) like 7Zip.

Please unzip the project folder from here using what program you have to perform this extraction.

![image](https://i.imgur.com/VqyNwuF.jpg)

![image](https://i.imgur.com/dIQROX2.png)

2. If you know terminal commands for the operating system you are working on, ```cd``` into the project folder you downloaded.

If you do not know terminal commands, you are about to learn them! Open this following link in a new tab (right-click the link and select "Open in new tab"): [Instructions on calling the directory](https://github.com/watson-music/watson-beat/blob/master/directory.md)

<hr>


Step Two: Set up for development
------------------------------------------------------
[Here are some directions to get your machine set up to run code](./initial_setup.md) 



Step Four: Choose a song (`MIDI` file)
------------------------------

1. In your terminal where you are in your project directory, `cd src`. 
<br>
2. If you are on Windows, now `dir`, for UNIX (Mac & Linux, etc), `ls`
<br>
NOTE: See the directory called `Midi`? MIDI stands for Musical Instrument Digital Interface. It is a protocol (not an audio file) designed for recording and playing back music on digital synthesizers that is supported by many makes of personal computer sound cards. AKA, these are the songs we are telling Watson to translate. If you already know this, you have used audio editors before, and you have Reaper or audio editors that can modify MIDI files already, you can use whatever MIDI files you have on your system, or from here https://freemidi.org/ and modify the file down to about 30 seconds for Watson to consume. If you want an entire song past 30 minutes, you will have to do this in batches.
<br>
2. Pick a song! It might be hard to do without knowing what the song sounds like though.

So open up Soundation for [Chrome](https://chrome.soundation.com/) or [Firefox](https://soundation.com/studio)!

Following this image below, open File and "Import MIDI file". 

[FileHippo](https://filehippo.com/software/archiving/) 

![image](https://i.imgur.com/tTl1eO5.png)



Step Five: Choose how Watson interpretes your song (`ini` file)
--------------------


Step Six: Create a folder for music and run terminal command with MIDI and ini selected
------------


Step Seven: You now have a song from Watson. Open the auio editor per your operating system or Soundation!
--------------

Step Eight: Import MIDI files from Watson to audio editor
-------------

Step Nine: Apply virtual instruments to the song 
----------

Step Ten: Export the file as a .wav or .mp3
--------------



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

