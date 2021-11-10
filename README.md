## hegduino.js
Contains USB, BLE, and WiFi Event Source protocols to connect to the HEGduino devices.
They all use the same calls, just specify which mode you want.

```
npm i hegduinojs
```


```
import {hegduino} from 'hegduinojs'

let heg = new hegduino('usb',ondata(newline)=>{},onconnect()=>{},ondisconnect=>{},hostURL);

// Fill out the ondata, onconnect, and ondisconnect functions to handle device events.

// newline will contain the string which you can then split.

heg.sendCommand('S'); //send a command to the device from any protocol.

heg.connect(); //runs the connect protocol based on the mode you set it up for.
heg.disconnect(); //disconnect from the device stream

```

In the code you can find a full BLE, Serial (for general web serial or chrome serial), and WiFi (event sources and xmlHTTPrequests) code demonstrations for working with the device in javascript. 

It's fairly barebones, just barely evolved beyond some tutorials I followed, but you can update the device via BLE or WiFi if you dig into those APIs, and generally this is a simple way to get data for any protocol available.


By: Joshua Brewster
License: AGPL v3.0


Contributors:
Diego Schmaedech (chrome serial)
