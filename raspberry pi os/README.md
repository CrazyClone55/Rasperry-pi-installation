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
<ol>
  <li>download raspberry pi os from https://downloads.raspberrypi.org/raspios_armhf_latest.torrent. This is the actual operating system</li>
  <li>while that is loading also download the raspberry pi imager for your operating system, if on linux use snap install rpi-imager and launch it with sudo, it will take a while to launch so be patient https://www.raspberrypi.org/downloads/. This allows us to write the operating system to our external drive, in this case, an sd card</li>
  <li>right click and extract the .img file from the zip file</li>
  <li>insert sd card into computer and run the imager</li>
  <li>select use custom and select the extracted .img file</li>
  <li>select the sd card as your target and click write (click yes after)</li>
  <li>once it is done click continue and remove the sd card</li>
  <li>reinsert sd card and navigate to it using your file browser. It will be called boot and have ~256 mb storage</li>
  <li>create a new file in that boot folder named "ssh" with no file extension</li>
  <li>eject the card</li>
 </ol> 
<h1>Run on Pi</h1>
<ol>
  <li>insert sd card into raspberry pi</li>
  <li>plug in display, usb splitter, usb mouse and keyboard, and power
  wait, until you get this screen
    <img src=""> //image of desktop5</li>
    <li>this is the desktop. Raspberry Pi Os, formerly called Raspian is a Linux based operating system with a pre installed gui. This is one of the more user friendly operating systems you can install. It is plug and play, and works right out of the box with no configuration.</li>
  <li>now click in the top right on the 2 arrows and 2 Xs to connect to your wifi (if met with warning such as this <img src=""> click ok) </li>//image of warning
  <li>Once connected, a local ip adress should show up above the next button on the welcome window <img src=""></li>//image of ip
  <li>if on windows, download free application, putty https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html, if on linux/mac use console and type ssh pi@[ip adress here] and login with raspberry as password</li>
  <li>launch putty and input ip adress in host name box, leave port at 22 and connection type on SSH</li>
  <li>click open, and if greeted with security alert click yes, then enter pi as username and click enter and enter raspberry as password and click enter</li>
  <li>what we have done is called Secure Shell, which is a way of securely remotely desktoping into a computer. This way we can control the raspberry pi from our laptop or computer.</li>
  <li>now type sudo raspi-config and hit enter, if prompted enter password, raspberry</li>
  <li>go to interfacing options and click enter, select VNC and click enter, select yes and select ok</li>
  <li>next select advanced options and select expand filesystem then click ok when done</li>
  <li>select finish to exit config and reboot computer with sudo reboot</li>
  <li>download vnc viewer on your computer https://www.realvnc.com/en/connect/download/viewer/</li>
  <li>In vnc viewer type in ip address of pi and hit enter, enter in pi as user and raspberry as the password</li>
  <li>now we are doing what is called virtural network computing, we are controlling the computer over the network. This allwos us to see everything, not only the command line</li>
  <li>Now we will walk through the setup (you dont have to do this through vnc, you can use tthe monitor and usb keyboard/mouse if you want)</li>
     <ol>a. click next and set country, language, and time zone and click next
        <li>now set a new password</li>
        <li>if there are black bars around your screen check the box, if not just click next</li>
        <li>we should already be connected to wifi, if not, connect and click next</li>
        <li>click next to update the computer</li>
        <li>once done, setup is done, click restart</li>
    </ol>
  <li>Have fun, you can do anything you want now from use the pi as a media server to make a self driving car out of it, the possibilities are endless</li>
    
</ol>