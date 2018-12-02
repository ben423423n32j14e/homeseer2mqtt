# homeseer2mqtt
HomeSeer MQTT interface via Node-Red.

<B><I>Control a HomeSeer device via MQTT:</I></B>
<BR>
<BR>
MQTT Topic: homeseer/in

To control via value send: (eg ref value of 105 and value 50 to set brightness if applicable)
<BR>
msg.payload.ref
<BR>
msg.payload.value
  
To control via label send: (eg ref value of 105 and value On or Off)
<BR>
msg.payload.ref
<BR>
msg.payload.label
