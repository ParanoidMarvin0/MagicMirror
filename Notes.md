# Worklog Notes and ToDo list

# Jan 26
## Screen Rotatation issue with Rasbian Buster
display_rotate=1 no longer works. MichMich solution in configuration also does not work.

>Date: 2019-04-08 Kernel: 4.14 to /etc/xdg/lxsession/LXDE-pi/autostart ):

>nano ~/.config/lxsession/LXDE-pi/autostart
>And add the following line:

>@xrandr --output HDMI-1 --rotate right

Found another suggestion of using "@xrandr -o right" also does not work.

### working solution as of Jan 26
run raspi-config 
    advanced options-> video/resolution -> enable full kms
reboot
@xrandr set in lxde-pi and display_rotate=1 set in boot/config.txt

## Added Modules

on-this-day 
    Random trivia facts about current date


## Calendar

https://calendar.google.com/calendar/b/1?cid=M28xaTVqaXZhZGtlNm9kZDZia2l1Z2lrbTRAZ3JvdXAuY2FsZW5kYXIuZ29vZ2xlLmNvbQ