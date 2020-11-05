<h1>welcome to installation of Tiny Core Linux</h1>
<p>I am going to assume that if you are installing tiny core linux that you are already familiar with computers and have common sense so this guide may be a bit harder, also I will expect you to click yes on diaoglues and read things for yourself, this is a guide not a </p>
<h2>Materials</h2>
<ul>
  <li>raspberry pi zero w</li>
  <li> micro sd card</li>
  <li>micro sd card reader</li>
  <li>usb splitter</li>
  <li>usb mouse and keyboard</li>
  <li>hdmi monitor</li>
  <li>usb ethernet adapter</li>
</ul>
<h2>Setup</h2>
<ol>
	<li>download tiny core linux from http://tinycorelinux.net/9.x/armv6/releases/RPi/piCore-9.0.3.zip</li>
	<li>while that is loading also download the raspberry pi imager for your operating system https://www.raspberrypi.org/downloads/, if on linux use snap install rpi-imager and launch it with sudo, it will take a while to launch so be patient. This allows us to write the operating system to our external drive, in this case, an sd card</li>
	<li>right click the downloaded tinycore zip and extract the folder from the zip file</li>
	<li>insert sd card into computer and install/run the imager</li>
	<li>select use custom and select the .img file from the extracted folder</li>
	<li>select the sd card as your target and click write</li>
	<li>Now eject sd card and plug in keyboard/mouse, display, sd card, and power to raspberry pi</li>
	<li>some keys will be generating, wait for them to stop and enter clear</li>
	<li>to save the generated file keys enter filetool.sh -b</li>
	<li>to expand file storage enter sudo fdisk -u /dev/mmcblk0</li>
	<li>enter p and write down starting LBA</li>
	<li>then enter d and then 2 to delete the second partition</li>
	<li>enter n to make a new partition, then enter p for primary partition, and then 2 for second partition, and then the starting LBA we saw earlier. hit enter to use the default end LBA</li>
	<li>enter w to write changes</li>
	<li>type sudo reboot to restart computer</li>
	<li>now do sudo resize2fs /dev/mmcblk0p2 to resize partition</li>
	<li>enter df -h to verify partition is expanded</li>
	<li>now we will install the wifi drivers</li>
	<li>enter sudo mount /dev/mmcblk0p1 /mnt/mm cblk0p1</li>
	<li>then cp /mnt/mmcblk0p1/opt/* /mnt/mmcblk0p2/tce/optional</li>
	<li>we do this because p1 is non persisitent storage, tinycore runs off of the ram, so anything we try and install or do has to be on the new partition, p2 which is on the sd card making it persistent</li>
	<li>hit enter to overite everything</li>
	<li>to load wifi, tce-load -i firmware-rpi3-wireless</li>
	<li>then run tce-load -i wifi</li>
	<li>now run sudo wifi.sh -a to launch wifi tui</li>
	<li>use ctrl+c to exit and type echo "wifi.sh -a" >> /opt/bootlocal.sh</li>
	<li>now connect to your wifi using wifi.sh -a (make sure your router supports 2.4ghz networks, or if you have a dedicated 2.4 wifi use than one)</li>
	<li>to install the rest of the software run tce-load -iw TC.tcz</li>
	<li>after it finishes enter filetool.sh -b again</li>
	<li>now reboot computer using sudo reboot</li>
	<li>you should reboot into the gui and you are done</li>
	
