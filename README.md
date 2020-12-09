# sushi-snap
A snap package for Sushi Digital Audio Workstation


## Install

To install the snap from the store use:

`snap install sushi-snap`

then manually connect the following interfaces:
`
snap connect sushi-snap:alsa
snap connect sushi-snap:home
snap connect sushi-snap:process-control
`


## Run
To run sushi-snap:

1. Plug-in your USB midi keyboard

2. Restart services
`snap restart sushi-snap.jackd`
`snap restart sushi-snap.sushi`
`snap restart sushi-snap.connect-keyboard`

3. ... play!

## Note
- sushi-snap is shipped with jackd and MDA JX10 VST3 plugin. T
- if you want to change sushi or jackd command line, you can view/change with snap get / snap set
`
$ snap get sushi-snap
Key             Value
jackd-cmd-line  -d alsa
sushi-cmd-line  -j --connect-ports -c /root/snap/sushi-snap/x1/VST3/config_play_vst3_desktop.json
`
`snap set sushi-snap jackd-cmd-line="your custom command line"`
`snap set sushi-snap sushi-cmd-line="your custom command line"`

  
## Building

Simply clone this tree and call `snapcraft` in the toplevel dir
