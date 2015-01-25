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

  ![power supply](/images/power.jpg)

1. SD Card with OS installed.

  ![Rapian SD Card](/images/Rasp.jpg)

1. Case with mount for Pi Camera.

  ![Case with camera mount](/images/case.jpg)

1. A suitable sized box (if using the abve kit the provided box is ideal).
1. A suitable light source to illuminate your items. (I'm using the [Mighty Bright eReader LEd Lamp](http://www.johnlewis.com/mighty-bright-led-e-reader-light-black/p431589?sku=231956681&kpid=231956681&s_kenid=2024374f-2661-32c9-b22d-0000736710b9&s_kwcid=404x101016&tmad=c&tmcampid=73&kpid=231956681) as I was given one for christmas, but any small light source would work).

  ![Light](/images/light.jpg)

1. A small, sharp craft knife.

 ![Craft knife](/images/knife.jpg)

1. Magnifying glass or Helping hand.

  ![Helping hand](/images/helphand.jpg)

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

5. Add the Rapsberry Pi sticker to the front of the box.

  ![Sticker](/images/back.jpg)


##Step 3: Program the Raspberry Pi to control the camera

This can be a really simple program to initiate the camera or could be complicated depending on what you wish to achive. In fact the `raspivid` command can be used in LXTerminal or at the command line to show an imagae on the screen (we don't need to save a file for this to work). To show the image we use the `-t x` extension where x is the time in miliseconds. We also need to use the `-rot 90` extension to rotate the view 90 degrees as the camera top faces the side of the box when installed in the case. If you use your own larger box you may be able to position the camera upright. In this case you can ommit the `-rot 90 extension`

The full command we will use is:

`raspivid -t  300000 -rot 90`

This show a video image on the screen for five minutes. If you require more or less time you can alter the numer of miliseconds (60000 for each minute) or you can terminate this early by pressing `ctrl+c`. You can also start it again quickly with the up arrow and enter.

  ![At the Command line](/images/cmd.jpg) ![in the GUI](/images/GUI.jpg)

##Step 4: Focus the Camera

If you have used the box from the kit you will find that the image is out of focus. The minimum focus distance of the Camera module is around 47cm and this is somewhat less than that.

To change the focus on the camera you will neeed to turn the lens on the board. Unfortunatly the Camera Module is designed to be fixed focus so the lens is glued in place with three small blobs of glue.

These blobs of glue can be cut using a craft knife and magnifying glass until the lens is free to move. To do this grab a sharp small craft knife and a magnifying glass (a helping hand device is ideal for this). You first will need to remove the camera moduile from the case to do this. 

![Cutting the lens free](/images/cutlens.jpg)


Once the lens is free to move turn the lens anticlockwise to make the area in focus closer to the camera. To do this it is best to set the camera running and keep testing the focus unti it is correct. Once you are happy with the focual distance of the camera then fix it back into the case. 


###Warning!!!

  ![Warning](/images/warn.jpg)

Take care when handling the camera module as they can be sensitive to static and they are not very firmly attached to the boards. It is really easy to break the module when trying to turn the lens so make sure the bottom part of the camera does not turn against the board when trying to turn the lens. The author takes no reposnsibility for camera modules if you ateempt this. If you do not wish to modify the lens you can always find a larger box to use.


##Step 5: Use the Visual-Pi-ser

With the simpele set up above the RPi can be connectyed directly to the projector and used as a visualiser. 

  ![set up](/images/setup.jpg)
  
This is most useful in a classroom where the pi can be connected directly to a projector. To make the Set up more like the seemless AV setups in universities you could [set up a VNC connection](http://www.raspberrypi.org/documentation/remote-access/vnc/README.md) and then minimise / maximise the VNC window when required. This will require permission to install VNC software if not already part of the school image so you might need to talk nicely to your IT Department to make this happen. You could of course purchase a KVM switch but that would cost money.

The construction of the box provided with this kit gives a fairly small area for working in but it is an ideal size for simple physical computing demonstrations and other small items. The advantage of this is it is slightly magnified so the students can easily see which pins are in use.

If you require a larger area for your demonstrations (lager physical computing projects or set up demonstrations) then you could use a larger box. An alternative idea is to borrow a clamp and clamp stand from the science department and secure the case a suitable distance above the desk. A sheet of A3  or A4 paper wil give a nice background for this.

Another potential bonus of using the box that comes with the kit is that due to the construction of the box you can still use it to store components in. So if you use more than one classroom or travel round showing people all thing RPi you have a handy carry case for your demo kit.

  ![All Packed in](/images/store.jpg) ![Box](/images/box.jpg)


##Future Improvements

1. Further options (such as the possibility to capture still pictures from the visualiser)can be added using a python or BASH script.

2. Buttons could be connected to the GPIO pins on the Pi and the script used to define extra functionality (such as stills or short video recordings.

3. LED lighting could be connected to the Pi GPIO pins and controlled using the RPi this only using the lighting when needed.


##Licence

Unless otherwise specified, everything in this repository is covered by the following licence:

![Creative Commons License](http://i.creativecommons.org/l/by-sa/4.0/88x31.png)

***Visual-Pi-ser*** by [Neil Bizzell](http://twiter.com/neilbizzell) is licenced under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).
