The Watson Beat Workshop
===============

## AGENDA

Step 1: Download the project
<br></br>
Step 2: Set up for development and install dependencies
<br></br>
Step 3: Choosing a song (MIDI file)!
<br></br>
Step 4: Choose how Watson interpretes your song (ini file!)
<br></br>
Step 5: Create a folder for music and run terminal command with MIDI and ini selected
<br></br>
Step 6: You now have a song from Watson. Open the auio editor
<br></br>
Step 7: Import MIDI files from Watson to audio editor
<br></br>
Step 8: Apply virtual instruments to the song 
<br></br>
Step 9: Export the file as a .wav or .mp3
<br></br>
Step 10: Listen to it 800 thousand times, email it to friends & fam or put on your resume "made music with Watson DBN"!
<br></br>


If you are a beginner - I will provide guidance for Windows and Mac OS. 
If you have Linux, I am going to make a vote of confidence and assume you know where your terminal is.

Using machine learning to spur human creativity is _so_ 2018!  Watson has used
a combination of reinforcement learning and neural networks to create the Watson Beat.

[What is Watson Beat and how does any of this happen?](https://medium.com/@anna_seg/the-watson-beat-d7497406a202)

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



Step Three: Choose a song (`MIDI` file)
------------------------------

1. In your terminal where you are in your project directory, `cd src`. 
<br></br>
2. If you are on Windows, now `dir`, for UNIX (Mac & Linux, etc), `ls`
<br></br>
NOTE: See the directory called `Midi`? MIDI stands for Musical Instrument Digital Interface. It is a protocol (not an audio file) designed for recording and playing back music on digital synthesizers that is supported by many makes of personal computer sound cards. AKA, these are the songs we are telling Watson to translate. If you already know this, you have used audio editors before, and you have Reaper or audio editors that can modify MIDI files already, you can use whatever MIDI files you have on your system, or from here https://freemidi.org/ and modify the file down to about 10-30 seconds for Watson to consume. If you want an entire song past 10-30 seconds, you will have to do this in batches.
<br></br>
2. Pick a song! It might be hard to do without knowing what the song sounds like though.
<br></br>
So look into this directory outside of your terminal! Since we have already established where this is on your system by going through this via your terminal, it should be fairly easy for you to find in your file system! If not, you can likely search for it by the keyword 'midi'. When you click on them, do they play? If not, no worries, I will show you how to play them.
<br></br>
3. [TO PLAY MIDI FILES]: Open up Soundation for [Chrome](https://chrome.soundation.com/) or [Firefox](https://soundation.com/studio)!
<br></br>
Following this image below, open File and "Import MIDI file". Then press the PLAY icon at the bottom of the screen!
<br></br>
![image](https://i.imgur.com/tTl1eO5.png)
<br></br>
Have in mind which song you want to choose yet? Record this as a note of which MIDI file you want Watson to interprete!

Step Four: Choose how Watson interpretes your song (`ini` file)
--------------------
There are two main ingredients to prepare to create your song with The Watson Beat. First, you need a midi file with a simple melody. Best results come when you keep this short, about 10 seconds. Also, leave some space between your notes to give the creativity engine some wiggle room.
<br></br>
The second ingredient is the ini file. The ini file give the creativity engine all of the spices to use, including time signature, "mood," and tempo. [Reference to advanced usage of ini that is not a part of tutorial](https://github.com/cognitive-catalyst/watson-beat/blob/master/customize_ini.md)
<br></br>
For now, choose by keyword from the different ini files in your project directory for sake of simplicity! The folder with `ini` files is within the `src` directory.
<br></br>
![image](https://i.imgur.com/cckJPaw.png)

<br></br>

Make a note on the ini file you have selected!!!

Step Five: Create a folder for music and run terminal command with MIDI and ini selected
------------

1. Go back to the terminal that has your project directory we went into in regards to Step One.
<br></br>

Windows: type `cd` only. This shows you where you are right now in regards to directories. Are you in the `/src` directory? If not, `cd src`. 
<br></br>
 
UNIX people: type `pwd` to see your path. Are you in the `/src` directory? If not, `cd src` within your project directory.
<br></br>

From here, you are going to make a directory for your own music Watson processes! Then from there, you make your own jams with Watson in the audio editors! 

For every operating system in this tutorial, `mkdir [PICK A NAME FOR YOUR MUSIC DIRECTORY]`. 

For example, my music directory is creatively called `music`
<br></br>
2. Now, `cd [NEW MUSIC DIRECTORY]`. You might have a few songs you want to do with Watson. So what I did was made folders per the output Watson gives me for each song. So you can do what I did and make another directory for your first song!
<br></br>
`mkdir [FIRST SONG NAME]`
<br></br>
My first song's directory is called `first_song`. 
<br></br>
UNIX NOTE: If you want whitespace in your directory's name, for UNIX you can `Tab` after using a few of the letters of the directory's name when in the terminal or you can escape the whitespace via terminal with a backspace `\` for the whitespace. 
<br></br>

Okay so we are all set for neatly output of files from Watson!

#### 3. MAKING YOUR SONG!!!!

<p align="center">
  <br><br>
  <img src="https://static1.squarespace.com/static/583da8fdebbd1ac168f74fcb/t/59091c6bf5e2314ab7962653/1495035470825/Music-2-Color-Theory-3.gif">
</p><hr/>
Here is the command from the terminal we will be entering with your selected `MIDI` and `ini` and output folder you made!

```
python wbDev.py [-i INIFILE] [-m MIDIFILEPATH] [-o OUTPUTPATH]
```

In your `/src` directory, you should see this `wbDev.py` file. You should be in the directory in which if you `dir` (for Windows) or `ls` for UNIX, you should see this file. 

Now lets formulate your command here. Here is an example of what I did.

`python wbDev.py -i Ini/Space.ini -m Midi/reaper_ellie.mid -o /Users/jrnash/Documents/watson-beat-master/src/music/song-three/`

Using the example above, formulate your own command! Remember to see the full path of your output folder, you can `cd` on Windows per where that folder is located, or `pwd` the path per where that folder is located.

Now go look in that output folder you specified in your command? See a bunch of files?!!

Step Seven: You now have a song from Watson. Open the audio editor per your operating system or Soundation!
--------------
You should have a slew of files like this now.

Let this list below be a guide as far as the virtual instruments you apply to make your songs in the next steps!
<br></br>
![image](https://i.imgur.com/BkhFTJG.png)

Step Eight: Import MIDI files from Watson to audio editor
-------------

All Operating Systems can use Soundation in the browser as long as they can use Firefox or Chrome
<br></br>
Mac: Garageband
<br></br>
Windows: Mixcraft
<br></br>
Linux: Soundation

SOUNDATION 
----------
Using the image from Soundation above, you can import several MIDI files into Soundation
<br></br>
Open up Soundation for [Chrome](https://chrome.soundation.com/) or [Firefox](https://soundation.com/studio)!

GARAGEBAND
----------
Mac: [Download Garageband](https://www.apple.com/mac/garageband/)

 You can drag and drop your MIDI files from Watson into Garageband!
<br></br>
This is for Mac users only: Go to App Store and search for Garageband, its a free download. :)

![image](https://i.imgur.com/CGRUJcd.jpg)
<br></br>

MIXCRAFT
-------------
(Download: 7 minutes) 
 
You can drag and drop your MIDI files into Mixcraft as well!


[Download Mixcraft](https://www.acoustica.com/mixcraft/download.php)
<br></br>

Step Nine: Apply virtual instruments to the song 
--------------
**Soundation**, here is an image to show how to add new instruments
<br></br>
![image](https://i.imgur.com/48aeSqq.png)
<br></br>
**Mixcraft**, this is the "keyboard icon" per your track, [example image](https://i.ytimg.com/vi/Wavm-97Dl6U/maxresdefault.jpg)

**Garageband**, Its in the library on the lefthand side of your screen. Then you can even download new instruments too. 

Step Ten: Export the file
--------------
.... and make your mark on Watson music history 

**Soundation**: Export by going up to `File` in the navigation bar and click `Export to .wav file`

**Garageband**: Go to `Share` in your navigation bar and click `Export Song to Disk` or any of the other options

**Mixcraft**: Go to `File` in your navigation bar and click `Mix Down To` and select with audio file you want to do this.



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

