# Multimedia support for openSUSE (Tumbleweed)

```sh
###  Add Packman repo (here for Tumbleweed)
sudo zypper ar http://ftp.halifax.rwth-aachen.de/packman/suse/openSUSE_Tumbleweed/Essentials/ packman-essentials
### Reduce priority of Packman
sudo zypper mr -p 110 packman-essentials
### Install packages from Packman
sudo zypper in --from packman-essentials -f gstreamer-plugins-bad-orig-addon gstreamer-plugins-ugly-orig-addon gstreamer-plugins-libav libavcodec57 k3b-codecs vlc-codecs chromium-ffmpeg
### For updating use
sudo zypper dup --no-allow-vendor-change
```
