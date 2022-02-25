[DisplayCAL](https://displaycal.net/)


To get it working, you need to allow connections to X11

```
xhost +
```

You also need to allow access to the dbus socket on the host, e.g. use the `-B /var/run/dbus` argument to Singularity.

I'm not sure if `--nv` is strictly necessary but I didn't test without.


```
singularity exec -B /var/run/dbus --nv \
    docker://ghcr.io/tomharrop/container-displaycal
```
