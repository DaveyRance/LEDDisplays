# LED Displays / Decorations used.
Information for LED displays for Led Matrix / Pixel art

This is mainly a dumping ground for what i have fonud usefull for LED displays that i have running around the place.

## Matrix Panels
Panel Type is indor p2.4 with 4 * 3 panels
5v 30A meanwell powersupply
(Adding in a small 5v Super Cap to try to add more ripple control)

### Raspberry PI as controller.  
Common PI hat (https://www.acmesystems.it/HAT-A3) that was used for the build.
  1. https://github.com/hzeller/rpi-rgb-led-matrix  
     * Worked fine but on large mount of white display would give flicker and strange sounds from display..  
     * Schedules were done by editing the rc.local and un commenting for season schedule
  2. FPP Player (Falcon Christmas Player) Running On PI 
     * https://github.com/FalconChristmas/fpp (6.3)  
     * Configuration from webpage  
     * Create play lists as needed for season  
     * Schedule Play Lists  
     * Multi Controller system  
     * Still flicked on displaying on strong white display colors 
     * Can be controlled by xLights

### Beagle Bone Black. 
The BBB has 2 realtime CPU's in it that allow better realtime performance for controling the LED matrix. (Not having main CPU having to deal with refreshing pixels)
For the BBB switching over to the card https://www.wiredwatts.com/octoplus 
   1. FPP Player (Falcon Christmas Player) Running BBB
     * https://github.com/FalconChristmas/fpp (6.3)  
     * Configuration from webpage  
     * Create play lists as needed for season  
     * Schedule Play Lists  
     * Multi Controller system  
     * Still flicked on displaying on strong white display colors 
     * Can be controlled by xLights
   
# Led Pixels
1. WLED on ESP32
Enabled 
