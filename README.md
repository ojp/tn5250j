# tn5250j
Dockerfile for tn5250j

This Dockerfile creates a container with java and tn5250j. I use it on my MBP (with Boot2Docker and Quartz X11) in combination with socat.

Set this once: socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\“$DISPLAY\”

After this you can use the image like this: docker run -e DISPLAY=192.168.59.3:0 oscarp/tn5250j

The GUI is redirected to X11 and the application starts without the need of installing java on my MBP.
