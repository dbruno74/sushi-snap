# sushi-snap
A snap package for Sushi Digital Audio Workstation


## Install

To install the snap from the store use:

`sudo snap install sushi-snap --classic`

## Run
To run sushi-snap:

1. Download your favourite plugin. We suggest to start with mda-vst3, available here:
https://github.com/elk-audio/elk-examples/releases/download/examples_01/mda-vst3.vst3.tar.xz

2. Unpack it in your home

3. Create a config.json file (for mda-vst3, you can take it from here:
https://github.com/elk-audio/elk-examples/blob/master/mda-jx10-vst3/config_play_vst3_desktop.json

4. Set the right path to your plugin (look for "plugins" stanza, then "path")

5. Launch sushi
`sudo sushi-snap.sushi -j-- --connect-ports  -c config.json` 

6. plug your midi keyboard/controller and connect it to sushi
`aconnect xx yy`
where xx is the client id of your keyboard/controller and yy is the client id of sushi
Client ids can be found with
`aconnect -l`

7. play!
  
## Building

Simply clone this tree and call `snapcraft` in the toplevel dir
