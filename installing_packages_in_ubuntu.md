
Steps for installing packages in ubuntu
=======================================

Step 1) apt-get update (press Enter)

Step 2) apt-get install openssh-server (press Enter)

Step 3) passwd (press Enter)

Note: Enter your new root password

Step 4) start the service of ssh

        service ssh start (press Enter)

This shall appear:

* Starting OpenBSD Secure Shell server sshd  [ OK ] 

Step 5) apt-get install lxde (press Enter)

Step 6) cd /root (press Enter)

Step 7) mkdir .vnc (press Enter)

Step 8) cd .vnc (press Enter)

Step 9) vi xstartup (press Enter)

          add these lines:
          #!/bin/sh
          xrdb $HOME/.Xresources
          xsetroot -solid grey 
          icewm &
          lxsession

Step 10) apt-get install tightvncserver (press Enter)

Step 11) export USER=root  (press enter)

         vncserver -geometry 1024x800  (press Enter)

	       enter a password at the prompt.


Method I - using connectbot (ssh)
--------------------------------- 


Step 1) Now on cubieboard click on web-browser and type:

        https://play.google.com/store/apps?hl=en

Step 2) click on Sign in and enter your gmail account and password and type:

        https://play.google.com/store/search?q=connectbot&c=apps&hl=en

Step 3) click on the ConnectBot app.It is open source and developed by Kenny Root and Jeffrey Sharkey.

Step 4) Click on Install button then, Accept. It will be installed.

Step 5) now click on connectbot icon which appears inside menu option

Step 6) select “ssh” from the drop down list and type:

	      root@127.0.0.1 (click on Done)

Step 7) type root password which has been recently created on Step 3

Congratulations !!! you are now running ubuntu operating system from connectbot application on cubieboard A20.

However, there is another method of running ubuntu by using android vnc.


Method II) - using android vnc
------------------------------

Step 1) Now on cubieboard click on web-browser and type:

        https://play.google.com/store/apps?hl=en

Step 2) click on Sign in and enter your gmail account and password and type:

	      https://play.google.com/store/apps/details?id=android.androidVNC

Step 3) select the android-vnc-viewer. It is open source and developed by androidVNCteam+antlersoft

Step 4) click on Install button then, Accept. It will be installed

Step 5) click on android vnc application on cubieboard

Step 6)  Enter the following details:

	        nickname: root

          password: entered at Step 11

          Address: localhost

          Port: 5901

          click on Connect button

That's it !!! you are now running ubuntu through android vnc.


Method III) - Directly booting ubuntu from external sdcard
----------------------------------------------------------

Step 1) put the sdcard into sdcard reader and attach it to computer

Step 2) Download the file from [here]

Step 3) save it on desktop and extract it

Step 3) open the terminal, go inside the Cubiuntu0.x.x directory and type:

        sudo dd bs=10m if=/home/ashish/Desktop/Cubiuntu0.6.5a-a20.img of=/dev/sdb (press enter)

Note: Here, ashish is the username of my computer.Enter your username. sdb is partiton name of my sdcard it could be different at your               end such as sdb1 or sdc.Be careful to enter the correct path.

Step 4) once the image has been flashed on to the sdcard unmount the sdcard

	      umount /dev/sdb (press enter)

Step 5) insert the sdcard into cubieboard and power on the device.

ubuntu will now start booting

username:linaro

password:linaro

That's it !!!

[here]: http://dl.cubieforums.com/patwood/Cubiuntu0.6.5a-a20.img.xz
