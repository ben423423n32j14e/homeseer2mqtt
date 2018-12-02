# homeseer2mqtt
HomeSeer MQTT interface via Node-Red, control devices and receive device updates.
<BR>
<BR>
* Polls HomeSeers JSON interface identifying device status changes and relaying them to a MQTT channel (typically with less than 200ms delay), eg this level of delay is typically not noticable to humans.
* Battery level is automatically added to the MQTT output for each battery device (enhancement)
* Control devices by name instead of ref (enhancement)

<B><I>Control a HomeSeer device via MQTT:</I></B>
<BR>
<BR>
MQTT Topic: homeseer/in

msg.payload.ref or msg.payload.name
<BR>
msg.payload.label or msg.payload.value
  
<I>Example:</I> (eg msg.payload.name = "Office" and msg.payload.label = "On")
