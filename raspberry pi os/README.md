hi, welcome to guide.

<h1>Required Materials</h1>
  <ul>
  <li>raspberry pi zero w</li>
  <li> micro sd card</li>
  <li>micro sd card reader</li>
  <li>usb splitter</li>
  <li>usb mouse and keyboard</li>
  <li>hdmi monitor</li>
</ul>
 
<h1>Setup</h1>  
<ol>
  <li>download and torrent (if you don't know what torrent means, go look it up)raspberry pi os from https://downloads.raspberrypi.org/raspios_armhf_latest.torrent. This is the actual operating system</li>
  <li>while that is loading also download the raspberry pi imager for your operating system https://www.raspberrypi.org/downloads/, if on linux use snap install rpi-imager and launch it with sudo, it will take a while to launch so be patient. This allows us to write the operating system to our external drive, in this case, an sd card</li>
  <img src="../Photos/imagerdownload.PNG" width="50%">
  <li>right click the downloaded raspios zip and extract the .img file from the zip file. The .img file is the operating system itself.</li>
  <img src="../Photos/extract.PNG" width="50%">
  <li>insert sd card into computer and install/run the imager</li>
  <li>select use custom and select the extracted .img file</li>
  <li>select the sd card as your target and click write (click yes after). This is extracting all of the contents of the .img file onto the sd card.</li>
  <img src="../Photos/imager.PNG" width="50%">
  <li>once it is done click continue and remove the sd card</li>
  <img src="../Photos/continue.PNG" width="50%">
  <li>reinsert sd card and navigate to it using your file browser. It will be called boot and have ~256 mb storage, if asked to format card, DO NOT FORMAT CARD</li>
  <img src="../Photos/files.PNG" width="50%">
  <li>create a new file in that boot folder named "ssh" with no file extension. This allows us to remotely control the raspberry pi</li>
  <img src="../Photos/sshfile.PNG" width="50%">
  <li>eject the card</li>
 </ol> 
<h1>Run on Pi</h1>
<ol>
  <li>insert sd card into raspberry pi</li>
  <li>plug in display, usb splitter, usb mouse and keyboard, and power.
  wait, until you get this screen
    <img src="../Photos/IMG_0312.jpg" width="50%"></li>
    <li>this is the desktop. Raspberry Pi Os, formerly called Raspian is a Linux based operating system with a pre installed gui. This is one of the more user friendly operating systems you can install. It is plug and play, and works right out of the box with no configuration.</li>
  <li>now click in the top right on the 2 arrows and 2 Xs to connect to your wifi</li>
  <img src="../Photos/IMG_0313.jpg" width="50%">
  <li>Once connected, a local ip adress should show up above the next button on the welcome window <img src="../Photos/IMG_0307.jpg" width="50%"></li>
  <li>if on windows, download free application, putty https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html, if on linux/mac use console and type ssh pi@[ip adress here] and login with raspberry as password</li>
  <li>launch putty and input ip adress in host name box, leave port at 22 and connection type on SSH</li>
  <img src="../Photos/putty.PNG" width="50%">
  <li>click open, and if greeted with security alert click yes, then enter pi as username and click enter and enter raspberry as password and click enter</li>
  <img src="../Photos/puttyyes.PNG" width="50%">
  <img src="../Photos/puttylogin.PNG" width="50%">
  <li>what we have done is called Secure Shell, which is a way of securely remotely desktoping into a computer. This way we can control the raspberry pi from our laptop or computer.</li>
  <li>now type sudo raspi-config and hit enter, if prompted enter password, raspberry</li>
  <img src="../Photos/raspi-configcli.PNG" width="50%">
  <li>go to interfacing options and click enter, select VNC and click enter, select yes and select ok</li>
  <img src="../Photos/Interfacingoptions.PNG" width="50%">
  <img src="../Photos/VNC.PNG" width="50%">
  <li>next select advanced options and select expand filesystem then click ok when done</li>
  <img src="../Photos/advanced.PNG" width="50%">
  <img src="../Photos/expand.PNG" width="50%">
  <li>select finish to exit config and select yes to reboot computer. We just enabled VNC and expanded the filesystem to take up then entire sd card.</li>
  <li>download vnc viewer on your computer https://www.realvnc.com/en/connect/download/viewer/</li>
  <li>In vnc viewer type in ip address of pi and hit enter after it restarts, enter in pi as user and raspberry as the password, if you see a screen saying server identity check failed click continue</li><img src="../Photos/VNCip.PNG" width="50%"><br><img src="../Photos/VNClogin.PNG" width="50%"><img src="../Photos/identity.PNG" width="50%">
  <li>now we are doing what is called virtural network computing, we are controlling the computer over the network. This allows us to see everything, not only the command line</li>
  <li>Now we will walk through the setup (you dont have to do this through vnc, you can use the monitor and usb keyboard/mouse if you want)</li>
     <ol>
        <li>click next and set country, language, and time zone and click next</li>
        <img src="../Photos/setlocation.PNG" width="50%">
        <li>now set a new password</li>
        <img src="../Photos/newpass.PNG" width="50%">
        <li>if there are black bars around your screen check the box, if not just click next</li>
        <li>we should already be connected to wifi, if not, connect and click next</li>
        <li>click next to update the computer</li>
        <li>once done, setup is done, click restart</li>
    </ol>
  <li>Have fun, you can do anything you want now from use the pi as a media server to make a self driving car out of it, the possibilities are endless</li>
    
</ol>
