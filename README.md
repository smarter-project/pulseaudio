# Pulse Audio

## Functionality
- https://www.freedesktop.org/wiki/Software/PulseAudio/
- Configures pulseaudio server that manages all audio devices available on host
- Actors are not granted access to dev/snd, but connect to PA server and recieve/stream audio over tcp socket
- Provides management script pulse_master.py that can dynamically manage PA server
    - Script maintains list of allowed host names and configures ACL for server
    - If host is on list but not alive, spawns new thread awaiting the containers connection to the cni when it spins up