# Turn-on additional speakers on laptop (works in a HP envy-13 with Bang & Olufsen)
To turn-on the speakers we need to edit the file ```/etc/pulse/daemon.conf``` and uncomment and edit the lines
```bash
; remixing-produce-lfe = no
; remixing-consume-lfe = no
; default-sample-channels = 2
; default-channel-map = front-left, front-right
```
to
```bash
remixing-produce-lfe = yes
remixing-consume-lfe = yes
default-sample-channels = 6
default-channel-map = front-left, front-right, rear-left, rear-right, front-center, lfe
```
To test the new configuration, we first need to restart pulseaudio using
```bash
pulseaudio -k && pulseaudio --start
```
and then run
```bash
speaker-test --channels=6 --nloops=2 --test=wav --device=default
```