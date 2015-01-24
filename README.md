#Visual-Pi-ser

A low cost classroom visualiser based on the Raspberry Pi.

This project is created from the [PC Raspberry Pi Model B+ Camera Kit](http://ucreatekit.co.uk/camera-kit.html) but you could also make this from the individual components and a suitable box.

##Step 0: Gather the components

For this project you will need:
1. A Raspberry Pi Model B+ (b could work but B+ prot configuration work better for this project).
1. A Raspberry Pi Camera Module (or Pi NoIR if you are using the Kit).
1. A Raspberry Pi Power Supply.
1. SD Card with OS installed.
1. Case with mount for Pi Camera.
1. A suitable sized box (if using the abve kit the provided box is ideal).
1. A suitable light source to illuminate your items.
1. Raspberry Pi Sticker (optional).

##Step 1: Set up the Raspberry Pi and Camera Module

Set up the Raspberry Pi with the Pre-installed SD card. You will need to connect the RPi to the internet to complete the set up. Raspian is probably the best choice for this project.

When running the config ensure the camera is enabled. 

If you are unsure of how to set up the RPi or the camera here are guides to set up the [Raspberry Pi](http://raspberrypi.org/.....) and set up the [Pi Camera](Http://raspberrypi.org/....)

##Step 2: Prepare the box

The first stage is to set up the framework using the kit box.

1. First mark around the case to judge the size of the case. Take case to ensure the camera mount hole will be in the middle of the box at the open side.

  ![Marking up](/images/mark.jpg)

2. Use a craft knife to cut a hole for the RPi to fit into. It is important to cut slightly smaller than the case so that it is a snug fit. More can be cut off but it is very hard to add card back after. If the fit is a little loose some electricians tape can be used to tighten the fit.

![Cutting out](../images/cut.jpg)

3. Test fit the pi repeatedly to get the fit right. Once the case fits nicely the stand is complete.

4. Clip the light source to the side of the box (or position to illuminate the items.
![Front on](../images/fronton.jpg)

5. Add the Rapsberry Pi sticket to the front of the box.

![Sticker](../images/back.jpg)


##Step 3: Program the Raspberry Pi to control the camera

This can be a really simple program to initiate the camera or could be complicated depending on what you wish to achive.

`Raspistill -p`

##Licence
