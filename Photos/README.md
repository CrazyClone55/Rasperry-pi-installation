hi, welcome to guide.

<h1>Required Materials</h1>
  <ul>
  <li>raspberry pi zero w</li>
  <li> micro sd card</li>
  <li>micro sd card reader</li>
  <li>usb splitter</li>
  <li>usb mouse and keyboard</li>
</ul>
  
  
<h1>Setup</h1>  
<p>
  download raspberry pi os from https://downloads.raspberrypi.org/raspios_armhf_latest.torrent. This is the actual operating system<p>
  while that is loading also download the raspberry pi imager for your operating system, if on linux use snap install rpi-imager and launch it with sudo, it will take a while to launch so be patient https://www.raspberrypi.org/downloads/. This allows us to write the operating system to our external drive, in this case, an sd card<p>
  right click and extract the .img file from the zip file<p>
  insert sd card into computer and run the imager<p>
  select use custom and select the extracted .img file<p>
  select the sd card as your target and click write (click yes after)<p>
  once it is done click continue and remove the sd card<p>
  reinsert sd card and navigate to it using your file browser. It will be called boot and have ~256 mb storage
  create a new file in that boot folder named "ssh" with no file extension
  eject the card
  
<h1>Run on Pi</h1>
<p>
  1. insert sd card into raspberry pi<p>
  2. plug in display, usb splitter, usb mouse and keyboard, and power<p>
  3. wait, until you get this screen<p>
    <img src=""> //image of desktop5<p>
    this is the desktop. Raspberry Pi Os, formerly called Raspian is a Linux based operating system with a pre installed gui. This is one of the more user friendly operating systems you can install. It is plug and play, and works right out of the box with no configuration.<p>
  4. now click in the top right on the 2 arrows and 2 Xs to connect to your wifi (if met with warning such as this <img src=""> click ok) //image of warning<p>
  5. Once connected, a local ip adress should show up above the next button on the welcome window <img src="">//image of ip<p>
  6. if on windows, download free application, putty https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html, if on linux/mac use console and type ssh pi@[ip adress here] and login with raspberry as password<p>
  7. launch putty and input ip adress in host name box, leave port at 22 and connection type on SSH<p>
  8. click open, and if greeted with security alert click yes, then enter pi as username and click enter and enter raspberry as password and click enter<p>
  9. what we have done is called Secure Shell, which is a way of securely remotely desktoping into a computer. This way we can control the raspberry pi from our laptop or computer.<p>
  10. now type sudo raspi-config and hit enter, if prompted enter password, raspberry<p>
  11. go to interfacing options and click enter, select VNC and click enter, select yes and select ok<p>
  12. next select advanced options and select expand filesystem then click ok when done<p>
  13. select finish to exit config and reboot computer with sudo reboot<p>
  14. download vnc viewer on your computer https://www.realvnc.com/en/connect/download/viewer/<p>
  15. In vnc viewer type in ip address of pi and hit enter, enter in pi as user and raspberry as the password<p>
  16. now we are doing what is called virtural network computing, we are controlling the computer over the network. This allwos us to see everything, not only the command line<p>
  17. Now we will walk through the setup (you dont have to do this through vnc, you can use tthe monitor and usb keyboard/mouse if you want)<p>
    <p>  a. click next and set country, language, and time zone and click next</p>
    <p>  b. now set a new password</p>
    <p>  c. if there are black bars around your screen check the box, if not just click next</p>
    <p>  d. we should already be connected to wifi, if not, connect and click next</p>
    <p>  e. click next to update the computer</p>
    <p>  f. once done, setup is done, click restart</p>
  18. Have fun, you can do anything you want now from use the pi as a media server to make a self driving car out of it, the possibilities are endless<p>
    
