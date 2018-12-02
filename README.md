# homeseer2mqtt
Creates an MQTT interface for HomeSeer via Node-Red.
<BR>
* Polls HomeSeers JSON interface identifying device status changes and relaying them to a MQTT channel (typically with less than 200ms delay), eg this level of delay is typically not noticable to humans.
* Battery level is automatically added to the MQTT payload for each battery device (enhancement)
* Control devices by name instead of ref (enhancement)

<BR>
<B><I>Instructions:</I></B>
<BR>
<BR>
1) Import the "homeseer2mqtt flow" into Node-Red
<BR>
2) Fill your MQTT server settings in the (homeseer/in and homeseer/out) nodes.
<BR>
3) Correct the HomeSeer URL as per the screenshot below:
<BR>
<BR>

![Screenshot](/images/setup.png)

<BR>
<B><I>Control a HomeSeer device via MQTT:</I></B>
<BR>
<BR>
MQTT Topic: homeseer/in

msg.payload.ref or msg.payload.name
<BR>
msg.payload.label or msg.payload.value
  
<I>Example:</I> (eg msg.payload.name = "Office" and msg.payload.label = "On")
<BR>
<BR>
Import flow "Sample Control Device Flow" in Node-Red for a simple working example.

<BR>
<B><I>Receive device status updates via MQTT</I></B>
<BR>
<BR>
When a devices status changes it is automatically output to MQTT Topic: homeseer/out
<BR>
<BR>
Example showing homeseer/out MQTT output in Node-Red debug when a device updates:
<BR>
<BR>
  
![Screenshot](/images/examplenoderedoutput.JPG)

<BR>
<BR>
<B><I>Notes:</I></B>
<BR>
* Expect this flow and HomeSeer to consume a lot of cpu. When enabled for me with about 30 Z-Wave nodes in HomeSeer it's using about 3% of my dual 8 core xeon cpus at the default "delay 100ms". It's possible to roughly halve the cpu utilization by increasing the delay node from 100ms to 200ms, you may need to do this or even more if you try to use this solution with eg a Raspberry Pi. Even 200ms though is hardly noticable for a human when turning a light on or off (I personally start to notice a very small delay when it is set at 400ms).
* This solution is in no way affiliated with HomeSeer and is licensed under the GNU GENERAL PUBLIC LICENSE Version 3 (see the LICENSE file).
