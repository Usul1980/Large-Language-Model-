# Large-Language-Model
creating an offline assistant on a tiny raspberry pi4
###How to run an AI assistant on Raspberry Pi 4 Model B with 8GB RAM

OK hi folks. I bought my raspberry pi 4 model b a while back, 2 years ago at least. It has 8GB of RAM and this was novel at the time I would say.
Recently I got interested in running an LLM on it. The rest of this article details how I went about that.
Upgrading from 32bit to 64bit architecture
So the necessary prerequisite was to upgrade my raspberry pi’s outdated architecture. 
What you will need to do this is:
•	A separate computer with
•	An SD card reader
OK you will need to download raspberry pi imager onto your other computer using this link:
https://www.raspberrypi.com/software/
I used my windows surface so downloaded the windows version:
 
Once you install it, run it.
You should see this:
 

Click on CHOOSE DEVICE and find your pi:
 

Next click on CHOOSE OS and choose the 64 bit Bookworm option at the top:
 
Next click on STORAGE and choose your SD Card:
 

Next you can choose NO for custom settings application during install if you like. All this means is that when you put the SD card back in to your pi4 and start it up, some setup questions will be asked of you on the pi4, such as settings for WIFI, browser preference etc.
The next screen will be a prompt reminding you that all existing data on the card will be erased. Make sure you have backed up anything you want before proceeding to continue! Writing the OS to the card may take 5 minutes or more.

###Moving over to the raspberry pi

So now that that’s done, you can eject your card and reinsert it into your raspberry pi. On startup you should be faced with raspberry pi desktop, a nice GUI with which to interface. Go through the initial setup and you are done you should be looking at a nice home screen, perhaps similar to this one:
 

Installing Ollama

Now we are ready to install Ollama, the framework we are going to use to run a tiny LLM.
Fire up Terminal, and run the following line of code:
curl https://ollama.ai/install.sh | sh

 
If you see a screen similar to the above, then the installation was a success!
Now to download a tiny LLM, the one I initially went with is called phi3 and is around 2.2GB.
Run the following line to download it and start running it:
ollama run phi3
it will download it and start it up automatically!

Once that’s done, give it a question:

![alt text](https://github.com/Usul1980/Large-Language-Model-/blob/main/recording.mp4?raw=true)






