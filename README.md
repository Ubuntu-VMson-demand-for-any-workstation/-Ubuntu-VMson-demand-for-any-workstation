# Ubuntu-VMson-demand-for-any-workstation
https://assets.ubuntu.com/v1/f401c3f4-Ubuntu_Server_CLI_pro_tips_2020-04.pdf?_ga=2.83651030.1946703254.1635890714-2008591924.1635890714
https://ubuntu.com/download/server
https://ubuntu.com/appliance/plex
https://ubuntu.com/appliance/openhab/raspberry-pi
Installation instructions
Ubuntu
Windows
macOS
What you’ll need
A microSD card (4GB minimum, 8GB recommended) A Raspberry Pi 3 or 4 A computer with a microSD card drive A micro-USB power cable (USB-C cable for the Pi 4) A monitor with an HDMI interface AHDMI cable for the Pi 3 and a MicroHDMI cable for the Pi 4 A USB keyboard
These steps will flash your OpenHAB Ubuntu Appliance to your Raspberry Pi with a Ubuntu machine, and get you logged in.

Install the Raspberry Pi Imaging Tool
Download the Imaging Tool for Ubuntu 

Prepare the microSD card
Warning
This will completely erase the microSD card.

Insert the microSD card into your computer
Run the imager and click CHOOSE OS
CHOOSE OS
Next, choose Use Custom. Select the image you downloaded.
Custom
Select your microSD card and click WRITE.
While it is preparing the disk you can go on to the next step and create your SSH keys for secure access to the appliance.

Generate Secure Shell (SSH) keys
The ‘Secure Shell’ protocol provides access to your Ubuntu Appliance and uses cryptographic keys to authenticate you to the device. You need SSH software and keys.

Run the following command:

ssh-keygen -t rsa
This starts the key generation process. When you execute this command, the ssh-keygen utility prompts you to indicate where to store the key
Press the ENTER key to accept the default location. The ssh-keygen utility prompts you for a passphrase
Type in a passphrase
You now have a public and private key that you can use to authenticate.

Create an Ubuntu SSO account
Your Ubuntu Appliance will be added to your Ubuntu cloud account and use your SSH keys to identify you. Add your keys to your account at https://login.ubuntu.com/ssh-keys.

To do so, run the following command in your terminal.

cat ~/.ssh/id_rsa.pub

Copy the result into the text field on the website. Click import and will have the key set up.

Boot your Raspberry Pi from the microSD card
Wait for the Raspberry Pi images to complete. Remove the microSD card from your computer and insert it into the Raspberry Pi. Attach your monitor and keyboard to the Pi, you will use them for the initial device configuration.

If you want to use a wired network, connect your ethernet cable to the Pi before booting.

Power up the Pi by connecting it to your USB power supply.

Your Pi will boot, and present you with a series of configuration choices. You need to ensure that the Pi has internet access so that it can get updates and verify your SSH keys. If you need more help there is a tutorial that goes through these steps in more detail.

Next, you will need to enter your Ubuntu cloud account email address. Your Pi will connect to your cloud account and retrieve your SSH keys.

SSH in
Your Pi will show an ssh command like:

ssh <Ubuntu SSO user name>@<device IP address>

Your user name is your Ubuntu SSO user name.

Your terminal will welcome you to Ubuntu Core.

That’s it
Now that you’re in your Pi you will be able to use your OpenHAB Ubuntu Appliance image.
  https://ubuntu.com/appliance/openhab/raspberry-pi
  https://github.com/canonical/multipass
  https://ubuntu.com/appliance/openhab
  https://discourse.ubuntu.com/c/multipass/21?_ga=2.188026088.1946703254.1635890714-2008591924.1635890714
  
