# homeseer2mqtt
HomeSeer MQTT interface via Node-Red.

<B><I>Control a HomeSeer device via MQTT:</I></B>
<BR>
<BR>
MQTT Topic: homeseer/in

To control via value send: (eg msg.payload.name = "Office" and msg.payload.value = "50")
<BR>
msg.payload.ref or msg.payload.name
<BR>
msg.payload.value
  
To control via label send: (eg msg.payload.name = "Office" and msg.payload.label = "On")
<BR>
msg.payload.ref or msg.payload.name
<BR>
msg.payload.label
