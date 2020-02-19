# Project Croissant Dual Boot (Beta)

For any question, you can find us on telegram: https://t.me/chromeosforpc

    Please, ask your questions at the group and don't PM the admins. :)

# Requirements
  - A generated ChromeOS image from our regular method, you can find it [here](https://github.com/imperador/chromefy/blob/master/README.md).
  - You need to have [rEFInd](http://www.rodsbooks.com/refind/) installed on your hard drive. There are many tutorials on the web teaching how to install it.

# Steps

  - Download both [dualboot.sh](https://raw.githubusercontent.com/imperador/chromefy/master/lab/dualboot.sh) and [dualboot.bin](https://github.com/imperador/chromefy/raw/master/lab/dualboot.bin) and place them on the same folder as your ChromeOS image.

  - Open a terminal (if you’re using ChromiumOS press CTRL + ALT + T, then type the command shell.) For any other Linux OS a normal terminal is fine, and then type the following commands:

      cd {path of the folder where your files are in}

      sudo bash dualboot.sh {yourchromeimage}.img dualboot.bin

  - Now deploy that Chrome image you generated to your usb stick, you can use programs like [Etcher](https://www.balena.io/etcher/) (Windows or Linux), [Rufus](https://rufus.ie/en_IE.html) (Windows only) and [Chromebook Recovery Utility](https://chrome.google.com/webstore/detail/chromebook-recovery-utili/jndclpdbaamdhonoechobihbbiimdgai?hl=en) (Chromium only).
  
  - The install script uses the free space on your hard drive to create the needed partitions, so you should use a program like [Gparted](https://gparted.org/) (usually comes with live Linux distros like Ubuntu) or partition manager on Windows. Remove the amount of space you need for ChromeOS from the other partition and just leave it like that (don't create another partition, the script will do that)

  - Boot into your usb stick, after you see the Chrome welcome screen press "CTRL + ALT + F2", it will ask for a login, type "chronos", type the following commands:

      sudo su

      sudo bash /usr/sbin/dual-boot-install -d /dev/sda
      (sudo bash /usr/sbin/dual-boot-install -d /dev/nvme0n1)

  - The script will start, it will ask for your consent, just accept. After the process is completed just type "reboot".

  - Now boot into rEFInd and you will see a FydeOS entry, just click on it.

      >You have ChromeOS Dual Booted, enjoy it. Don't forget to give us your feedback on the telegram group
      
# A big thanks to the [FydeOS Team](http://fydeos.com/) for the install script.      

