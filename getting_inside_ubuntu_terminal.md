Steps to get inside ubuntu terminal
-----------------------------------

Step 1) put sdcard (8Gb) inside the sdcard reader

Step 2) put the card reader into usb port of your computer

Step 3) to download "ubuntu.zip" visit [here] and click on "CLICK HERE to Download".

Step 4) save the file on desktop

Step 5) open the terminal and type:

	      cd ~/Desktop (press ENTER)

	      unzip ubuntu.zip (press ENTER)

Note: A folder named ubuntu shall appear on Desktop.

Step 6) copy the “ubuntu” folder in sd card

	      cp  -dpR ubuntu /media/boot (press ENTER)

Note: Here, boot is the name of my sdcard. The name of your sdcard could be something like an alpha-numeric number like c7e9b0a1-6bb5-2246. 

Step 7) after ubuntu folder has been copied, umount the sdcard

	      sudo umount /media/boot (press ENTER)

Step 8) power on the cubieboard

Step 9) insert the sdcard into cubieboard A20 sdcard slot

Step 10) connect cubieboard via usb cable to ubuntu desktop system

Now, open the command terminal on your system and type:

Step 11) cd ~/Desktop/adt-bundle-windows-x86-20130917 (press Enter)

Step 12) cd sdk/platform-tools (press Enter)

Step 13) sudo su (press enter)
	       enter your password

Step 14) ./adb devices (press enter)

Step 15) ./adb shell (press enter)

If you see something like this:

root@android:/ #

then, you are inside android shell.

Step 16) su (press Enter)

Step 17) Get inside ubuntu directory of the sdcard

	       cd /mnt/extsd/ubuntu (press Enter)

Step 18) Change the file permission of ubuntu.sh file.

	       chmod 755 ubuntu.sh (press Enter)

Step 19) execute ubuntu.sh shell file

	       sh ubuntu.sh (press Enter)

Step 20) Now, type:

	       bootubuntu (press Enter)

Note: At stage if you see something like this:

root@localhost:/#

Then, congratulations !!! you are now running Ubuntu on your device!!


[here]: http://mirror22.downloadandroidrom.com/download/AndroidUbuntu/ubuntu.zip?token=841322312
