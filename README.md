# inv_vzw31-sn_WeatherTrend_Notification  
This is code for HomeAssistant and ZWaveJS for the Inovelli VZW31-SN Red2-1 Switches.   
  
This is **IN PROGRESS AND INCOMPLETE**. Please see [Inovelli Community - VZW31-SN: Per LED with Effects - What comes first?](https://community.inovelli.com/t/vzw31-sn-per-led-with-effects-what-comes-first/16145?u=b07ymriv) for more information and tracking.  

**GOAL:** Set up an hourly notification based on the rising or falling of the temperature to go off hourly across multiple switches.  
**Current Configuration:**  
  
Ive set up a script for each group of commands that needs to be run. All of these use the `zwave_js.multicast_set_value` for each call. A total of 7 calls have to be made for each LED.
Here's what I have so far:  
* One for duration  
* Two for color selection  
* One for effect  
* One for level (although this one will likely be a one-off command for the time being)  
* An automation that turns the LEDs off prior to the changes and then executes the scripts  
* A trend binary sensor that detects whether the temperature is rising/falling to a certain threshold
