# homeseer2mqtt
Two way MQTT interface for HomeSeer via Node-Red.

<B>Control device HomeSeer via MQTT</B>
MQTT Topic: homeseer/in

* To control via value send:
  *msg.payload.ref
  *msg.payload.value
  
* To control via label send:
  msg.payload.ref
  msg.payload.label
  
For example I want to control device with ref 105 and turn it on using the label: On
