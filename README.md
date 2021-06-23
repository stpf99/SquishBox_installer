# SquishBox_installer


SquishBox info:

"Put together an electronic synthesizer with lots of instruments that uses just a Raspberry Pi and your favorite MIDI controller! You can switch patches and banks using your controller's pads/buttons/knobs. This updated version has an install script that simplifies the setup - just log in to your Pi and enter"

main source: 
curl https://geekfunklabs.com/squishbox | bash

https://geekfunklabs.com/
https://github.com/albedozero/fluidpatcher
https://www.youtube.com/watch?v=ONuXCzcuj7E&t=497s
https://hackaday.io/project/9097-squishbox
https://www.tindie.com/products/15120/
https://www.tindie.com/products/22886/

for Armbian Focal (tested on LibreComputer LaFrite 1GB)

this is modified/fixed script to run SquishBox on other than Raspbeery Pi devices running Armbian "Focal"

To run:

cd "to source directory"

change permission to run

chmod +x squishbox

and run

./squishbox


Optonal if no sound in speakers after install :

for default soundcard change "0" to your main soundcard at lines 387 and 388 in "squishbox" install script...

sudo rm /etc/asound.conf

sudo echo defaults.pcm.card 0 >> /etc/asound.conf

sudo echo defaults.ctl.card 0 >> /etc/asound.conf



and run install script again but Answer "yes" to questions if only this is necessary

TIP:
In Armbian Focal based on ubuntu Focal you don't need to answer yes to quaestion about to build fluidsynth from source /updated version is already in repository...

