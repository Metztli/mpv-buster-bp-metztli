mpv-0.28 from https://github.com/mpv-player/mpv master (05-28-2018)

To build for Debian stretch-backports, after all dependencies,
 i.e., ffmpeg, etc., were fulfilled:

./bootstrap.py
(to download waf)

quilt push -a
(to apply all debian/patches as there is a link at current mpv source)

dpkg-buildpackage -d -F -us -uc -jX -T binary
(where X above stands for number of CPU cores,
 and -d to not check library dependencies relevant to Sid/Unstable)


Huelmati [Enjoy]!
