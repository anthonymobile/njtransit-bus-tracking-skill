# <img src='https://raw.githack.com/FortAwesome/Font-Awesome/master/svgs/solid/bus.svg' card_color='#40DBB0' width='50' height='50' style='vertical-align:bottom'/> NJTransit Bus Tracking for Mycroft voice assistant
Announce arrivals of NJTransit buses. 

## About
Mycroft will announce estimated arrival times of NJTransit buses at your stop so you never leave the house before you have to.  All data and arrival predictions used by this skill are provided by the NJTransit.  

See below for full documentation, including how to track buses traveling toward your stop, but to get started just say "Hey Mycroft, Bus Arrivals".  You will be prompted for the bus route, direction and stop name.  Mycroft will respond with all estimated arrival times at your stop.

<details><summary>View Sample dialog</summary>
<dl>
<dt>Hey Mycroft Bus Arrivals</dt>
<dd>Which route are you riding?</dd>
<dt>Eighty-Five</dt>
<dd>Are you going outbound toward Journal Square or Inbound toward Hoboken?</dd>
<dt>Inbound</dt>
<dd>Which stop?</dd>
<dt>Palisade and South Street</dt>
<dd>Route Eighty-Five service to Hoboken arrivals for Palisade and South Street:<dd>
<dd>Arriving in 11 minutes<dd>
<dd>Arriving in 21 minutes<dd>
<dd>Arriving in 34 minutes<dd>
</dl>
</details>

<details><summary>View Full Documentation</summary>

#### bus or Transit

Wherever this documentation calls for saying "bus" to Mycroft it can be replaced with "transit", and vice versa.  If Mycroft is having difficulty understanding  one, try the other.

#### Arrival Times

To provide bus arrival times the skill requires three pieces of information:  bus route, traveling direction and bus stop.  If you do not provide all information needed the skill will prompt you for the rest.  For example, saying

> Bus arrivals route 57 going inbound stop Brighton Ave and Linden Street

will retrieve all arrival times predicted for the stop.  The arrival times could also be retrieved by any of the following:

> Bus arrivals route 57 going inbound

> Bus arrivals route 57

> Bus arrivals

Mycroft will prompt for any missing information.

#### Bus Tracking

Bus tracking is similar to Arrival Times but Mycroft will continue to track buses, periodically updating their predicted arrival times, until they have passed the stop.  By default Mycroft will track the next three buses and will announce updated arrival predictions every 30 seconds.  These values can be changed in the skill settings on Mycroft Home.  The minimum frequency of updates  is 30 seconds.

As with Arrivals, say

> Bus tracking

to begin.  Predicted arrival times of the next three tracked buses will be announced right away and updated every 30 seconds.  Be aware that there may be any number of buses heading to your stop but only the arrival predictions for the tracked buses will be announced.

When a bus passes your stop it will drop off the tracking list and there will be one fewer arrival time announced on subsequent updates.  When all buses have passed your stop Mycroft will automatically stop tracking.  If you would like tracking to end at any time say

> Bus shutdown

#### Shortcuts

If you ride the same route from the same stop often you will want to use shortcuts.  After Mycroft announces arrivals or starts tracking buses you may save the route, direction and stop combination as a shortcut using any name you wish.

Suppose you take the bus to work and went through the process of asking for arrivals, telling Mycroft the bus route, direction and stop.  Now say

> transit save shortcut

and Mycroft will prompt you for a name.  If you say

> rat race

you may get Arrivals or begin Bus Tracking using the shortcut

> Bus tracking rat race

Two additional phrases

> list bus shortcuts

> bus remove shortcut rat race

allow you to list and delete saved shortcuts.

#### API Key (N/A for NJTransit version)

When installed this skill does not use an API key when getting data from the NJTransit servers.  XXX Using a key allows a higher rate limit when requesting data.  It should not be necessary to use an API key but if you like you may obtain one on the [MBTA website](https://api-v3.mbta.com/register). In the skill settings on Mycroft Home check the box next to "Use my API key" and enter your key in the text field.

</details>


## Examples
* "Bus Arrivals"
* "Bus Tracking"
* "Save Transit Shortcut"

## Credits
Original [MBTA Bus Tracking Skill](https://github.com/richhowley/mbta-bus-tracking-skill) by [Rich Howley](https://github.com/richhowley)
, NJTransit adaptation by [Anthony Townsend](https://github.com/anthonymobile) November 2020

## Category
**Transport**

## Tags
#NJTransit, #MBTA,#Boston
