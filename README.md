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
   
## Led Pixels
Primarylry using WS2812 (pixles on cord https://www.wiredwatts.com/sn12v50bkp3-r) and WS2815 (LED strips)
Controll WLED, FPP using xLights https://www.youtube.com/watch?v=LkGCo9Gi8mk 
  1. WLED (https://github.com/Aircoookie/WLED)
     1. ESP32 micro controller
        * can support up to 10 strings on standard ESP32  (https://kno.wled.ge/features/multi-strip/)  
        * Suggest that limit to about 512 LEDs/pin and about 4 outputs for a total of 2048 LEDs.  
        * Supports using LedFx for music effects https://github.com/LedFx/LedFx  
        * Supports control from xLights / FPP  
        * Suggested to use a WT32-ETH01 if planning on using in a bigger system and running over ethernet not wifi. (If syncing of effects is not time critical then wifi may work)  
        * Will need a level shifter to deal with 3v3 vs 5v signaling  
     2. AThom WLED ESP32 controller
        * https://www.athom.tech/blank-1/wled-esp32-music-addressable-led-strip-controller
        * More of a Plug in play WLED controller over wifi. In mounted case so better for bench work / testing / higher partner acceptance factor.
        * Built in level shifter for 3v3 to 5v signaling
        * Built in microphone for sound pulsing and optional infrared remote.
   2. Pixel Controllers 
      * There are a number of dedicated controllers for running LED Pixels that are supported by the comerical companies depending on the number of Pixels that one is wanting to support the following have been found but not tested.  
        *  https://pixelcontroller.com/store/products/70-f16v4.html  
        *  https://microcyb.com/index.html  
      * Check out https://xlights.org/16-port-rgb-pixel-controllers/ for list of controllers. (From what i have seen the Falcon controllers from Pxelcontroller seem to be spoken well of.)
  * Store that may or maynot be any good for getting leds https://www.rgb-man.com/online-store  
  * China stores:
    * https://www.ledyilighting.com/the-ultimate-guide-to-addressable-led-strip/
    * https://www.aliexpress.us/item/3256802704468559.html
    * https://www.aliexpress.us/item/2251832774866810.html

