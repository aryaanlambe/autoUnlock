# autoUnlock
Lock/Unlock your Ubuntu box via USB

## Usage Instructions:

1. Open Terminal (CTRL + ALT + T) & type the following to install xscreensaver


                        **sudo apt install xscreensaver**


2. Again, in Terminal type the below command to locate your USB Device (can be run without sudo privileges):


                                   **lsusb**


3. Copy "autoUnlock" to the current user's home folder (or any folder of your choice, as long as its for the current user)

4. Open the script and edit as per your system (instructions on how to do this are provided in the comments of "autoUnlock")

5. Make the script executable using the following command (modify the command according to where "autoUnlock has been placed")


                        **chmod +x <INS DIR HERE>/autoUnlock**


6. Access the Crontab of the current user by:


                     **crontab -u <USER IN SMALL LETTERS> -e**


7. Scroll down to the end of the Crontab and add the following entry. After that save the file by CTRL + X followed by y then ENTER (modify the command according to where "autoUnlock has been placed")

                  
                     * * * * * bash <INS DIR HERE> & >/dev/null 2>&1


8. Restart the Crontab unit with the following command

                         
                      **/etc/init.d/cron restart**

9. Type in the following command ONLY if nautilus (File manager for Ubuntu) keeps on opening after USB insertion:


                **gsettings set org.gnome.desktop.media-handling automount-open false**
