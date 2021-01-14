# Linux

## Audio

### Static noise

Not sure why is this happening but for example if you start listening on firefox audio quality is great but if you start on chrome or any other application it sucks

Most users suggest modifying this line `load-module module-udev-detect` so it looks like that `load-module module-udev-detect tsched=0` in `/etc/pulse/default.pa`
It didn't work in my case

I had to enable noise cancellation by adding following lines

```bash
.ifexists module-echo-cancel.so
load-module module-echo-cancel aec_method=webrtc source_name=echocancel sink_name=echocancel1
set-default-source echocancel
set-default-sink echocancel1
.endif
```

to the `/etc/pulse/default.pa`

Source: [www.linuxspring.com](https://www.linuxuprising.com/2020/09/how-to-enable-echo-noise-cancellation.html)
