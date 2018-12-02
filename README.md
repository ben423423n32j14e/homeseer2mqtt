# homeseer2mqtt
HomeSeer MQTT interface via Node-Red.

<B><I>Control a HomeSeer device via MQTT:</I></B>
<BR>
<BR>
MQTT Topic: homeseer/in

To control via value send:
<BR>
msg.payload.ref or msg.payload.name
<BR>
msg.payload.value
  
To control via label send:
<BR>
msg.payload.ref or msg.payload.name
<BR>
msg.payload.label
