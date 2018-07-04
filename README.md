# alexa_wemo_SprinklerSwitch

I created this project because I wanted to automate watering the garden!

We have lots of plants in pots (no border plants as we just have Clay instead of dirt!), and it takes a while, and I'm a little lazy and not too interested in watering the garden.

For years I had a timer on the garden tap, that connects up to a pipe that goes around all the plants, with sprinklers for each plant. But every year the timers break - they only seem to last one season and the timers were just too simple.

I use Domoticz for a lot of my home automation, plus Alexa for voice control - integrated with Domotics using HABridge, so it made a lot of sense to create something that would work with both.

For this project I used an ESP8266 device - the Wemos D1 Mini https://wiki.wemos.cc/products:d1:d1_mini complete with a Relay Sheild : https://wiki.wemos.cc/products:d1_mini_shields:relay_shield

The relay shield was then connected up to a 12v Solenoid Valve like these: https://www.ebay.co.uk/p/DC-12v-1-2-Electric-Solenoid-Valve-Magnetic-Water-Air-N-c-Normally-Closed/26020073664?iid=323299429281

I actually used 3 of these devices to control 3 spurs of the watering system - allowing me to control them individually, which helps with the water pressure, as it was very low if all 3 were on at the same time.

The core of the code comes from this repo: https://github.com/kakopappa/arduino-esp8266-alexa-multiple-wemo-switch so my thanks go to them! I only changed it slightly to fit my needs.

I installed my 3 devices inside a water proof box with just the wires to control the valves coming out, and the 12v power going in. I hid all the wires under gravel etc, and I also used a 4 way water garden splitter to hook up the valves.

Once all the harware was in place, I used Alexa to discover the devices and now I can control the system just by speaking to Alexa!

I also used Domotics to create a Scene - One for Sunrise and one for Sunset - this way the garden gets watered at the right times of day. I put delays in so that it only watered Zone 1 first, then stopped that Zone, watered Zone 2 etc. I used the Wemo scripts for Domoticz to control the devices from within Domoticz: https://www.domoticz.com/wiki/Wemo I had issues with the python plugin, so resorting to scripts helped.

I think that's everything!
