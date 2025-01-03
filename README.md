# Large-Language-Model

### How to run an offline tiny LLM on a Raspberry Pi 4 Model B with 8GB RAM

OK hi folks. I bought my raspberry pi 4 model b a while back, 2 years ago in 2022 at least. It has 8GB of RAM and this was novel at the time I would say.
Recently I got interested in running an LLM on it. The rest of this article details how I went about that.

### Upgrading from 32bit to 64bit architecture

So the necessary prerequisite was to upgrade my raspberry pi’s outdated architecture. 
What you will need to do this is:
•	A separate computer with
•	An SD card reader
OK you will need to download raspberry pi imager onto your other computer using this link:

https://www.raspberrypi.com/software/

I used my windows surface so downloaded the windows version:
 ![Picture1](https://github.com/user-attachments/assets/cb0b4fd4-ba73-4857-9edc-2b3c3c0e1950)

Once you install it, run it.

You should see this:
 
![Picture2](https://github.com/user-attachments/assets/e48629ca-c058-4975-8752-752517618ecf)

Click on CHOOSE DEVICE and find your pi:
 
![Picture3](https://github.com/user-attachments/assets/023ff074-7300-4b52-9397-170ac5d9e326)

Next click on CHOOSE OS and choose the 64 bit Bookworm option at the top:

 ![Picture4](https://github.com/user-attachments/assets/4c04e889-2052-4aca-b47c-4f13e1ba8063)

Next click on STORAGE and choose your SD Card:
 
![Picture5](https://github.com/user-attachments/assets/1958a328-5405-4db2-a1d3-18fbead72eb0)

Next you can choose NO for custom settings application during install if you like. All this means is that when you put the SD card back in to your pi4 and start it up, some setup questions will be asked of you on the pi4, such as settings for WIFI, browser preference etc.
The next screen will be a prompt reminding you that all existing data on the card will be erased. Make sure you have backed up anything you want before proceeding to continue! Writing the OS to the card may take 5 minutes or more.

### Moving over to the raspberry pi

So now that that’s done, you can eject your card and reinsert it into your raspberry pi. On startup you should be faced with raspberry pi desktop, a nice GUI with which to interface. Go through the initial setup and you are done you should be looking at a nice home screen, perhaps similar to this one:
 
![Picture6](https://github.com/user-attachments/assets/49506042-4d5e-479c-80db-e07ef07c1800)

### Installing Ollama

Now we are ready to install Ollama, the framework we are going to use to run a tiny LLM.
Fire up Terminal, and run the following line of code:
`curl https://ollama.ai/install.sh | sh`

Once that's done, you now need to choose a tiny llm.
You can see the ollama library here: 

https://ollama.com/library

I opted for tinlyllama, which is around 600MB.
Run the following line in terminal to download it and start running it:

`ollama run tinyllama`

it will download it and start it up automatically!

Once that’s done, give it a question:



https://github.com/user-attachments/assets/4fb9891a-84fc-4f00-bfb1-1c8ed575da19

And you are done! Well done on your first offline LLM!








