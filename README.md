#Visual-Pi-ser

A low cost classroom visualiser based on the Raspberry Pi.

This project is created from the [PC Raspberry Pi Model B+ Camera Kit](http://ucreatekit.co.uk/camera-kit.html) but you could also make this from the individual components and a suitable box.

  ![Raspberry Pi Model B+ Camera Kit](/images/kit.jpg)

##Step 0: Gather the components

For this project you will need:

1. A Raspberry Pi Model B+ (b could work but the B+ port configuration works better for this project).

  ![Raspberry Pi B+](/images/RpiB+.jpg)
  
1. A Raspberry Pi Camera Module (or Pi NoIR if you are using the Kit).

  ![Raspberry Pi Camera Module](/images/rpicam.png)

1. A Raspberry Pi Power Supply.
1. SD Card with OS installed.
1. Case with mount for Pi Camera.

  ![Case with camera mount](/images/case.jpg)

1. A suitable sized box (if using the abve kit the provided box is ideal).
1. A suitable light source to illuminate your items. (I'm using the [Mighty Bright E reader LEd lamp](http://www.johnlewis.com/mighty-bright-led-e-reader-light-black/p431589?sku=231956681&kpid=231956681&s_kenid=2024374f-2661-32c9-b22d-0000736710b9&s_kwcid=404x101016&tmad=c&tmcampid=73&kpid=231956681) as I was given one for christmas, but any small light source would work)

  ![Light](/images/light.jpg)

1. Raspberry Pi Sticker (optional).

  ![sticker](/images/sticker.jpg)


##Step 1: Set up the Raspberry Pi and Camera Module

Set up the Raspberry Pi with the Pre-installed SD card. You will need to connect the RPi to the internet to complete the set up. Raspian is probably the best choice for this project.

When running the config ensure the camera is enabled. 

If you are unsure of how to set up the RPi or the camera here are guides to set up the [Raspberry Pi](http://raspberrypi.org/.....) and set up the [Pi Camera](Http://raspberrypi.org/....)

##Step 2: Prepare the box

The first stage is to set up the framework using the kit box.

1. First mark around the case to judge the size of the case. Take case to ensure the camera mount hole will be in the middle of the box at the open side.

2. Use a craft knife to cut a hole for the RPi to fit into. It is important to cut slightly smaller than the case so that it is a snug fit. More can be cut off but it is very hard to add card back after. If the fit is a little loose some electricians tape can be used to tighten the fit.

  ![Cutting out](/images/cut.jpg)

3. Test fit the RPi repeatedly to get the fit right. Once the case fits nicely the stand is complete.

4. Clip the light source to the side of the box (or position to illuminate the items).
  
  ![Front on](/images/fronton.jpg)

5. Add the Rapsberry Pi sticket to the front of the box.

  ![Sticker](/images/back.jpg)


##Step 3: Program the Raspberry Pi to control the camera

This can be a really simple program to initiate the camera or could be complicated depending on what you wish to achive. In fact the `raspistill` command can be used in LXTerminal or at the command line to show a preview image (we don't need to save a file for this to work.

`raspistill -p`

Will show a preview of the image on the screen 

`raspistill -f`

Will give a full screen preview.

##Step 4: Use the Visual-Pi-ser

With the simpele set up above the RPi can be connectyed directly to the projector and used as a visualiser.


##Future Improvements

1. Further options (such as the possibility to capture still pictures from the visualiser)can be added using a python or BASH script.

2. Buttons could be connected to the GPIO pins on the Pi and the script used to define extra functionality (such as stills or short video recordings.

3. LED lighting could be connected to the Pi GPIO pins and controlled using the RPi this only using the lighting when needed.


##Licence

Unless otherwise specified, everything in this repository is covered by the following licence:

![Creative Commons License](http://i.creativecommons.org/l/by-sa/4.0/88x31.png)

***Visual-Pi-ser*** by [Neil Bizzell](http://twiter.com/neilbizzell) is licenced under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).
