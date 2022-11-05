# Pulse Audio

## Functionality
- https://www.freedesktop.org/wiki/Software/PulseAudio/
- Configures pulseaudio server that manages all audio devices available on host
- Actors are not granted access to dev/snd, but connect to PA server and recieve/stream audio over tcp socket
- Clients of this pulseaudio container can simply set the environment variables in their container like the following to be able to source audio via opening their default device with a framework like pyaudio:
  - `PULSE_SOURCE`=`alsa_input.hw_2_0`
  - `PULSE_SERVER`=`tcp:pulse:4713`

