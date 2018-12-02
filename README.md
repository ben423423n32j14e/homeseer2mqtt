# homeseer2mqtt
HomeSeer MQTT interface via Node-Red.
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
2) Fill out the MQTT node settings (homeseer/in and homeseer/out)
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
