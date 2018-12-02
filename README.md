# homeseer2mqtt
Two way MQTT interface for HomeSeer via Node-Red.

<B>Control device HomeSeer via MQTT</B>
<BR>
<BR>
MQTT Topic: homeseer/in

To control via value send:
<BR>
<BR>
*msg.payload.ref
<BR>
*msg.payload.value
  
To control via label send:
<BR>
<BR>
*msg.payload.ref
<BR>
*msg.payload.label
  
For example I want to control device with ref 105 and turn it on using the label: On
