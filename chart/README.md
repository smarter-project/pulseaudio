# smarter-pulseaudio

Provides pulseaudio server for a smarter edge node. Simplifies audio access to other containers.
It uses alsa devices available on the host (needs /dev/snd/ from smarter-device-manager)

For more information look at [README](https://gitlab.com/smarter-project/edge-workloads/pulseaudio.git)

```console
helm install smarter-pulseaudio chart
```

