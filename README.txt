docker-ubuntu-journaldnotify-build

This is a Dockerfile whose sole purpose is to build a deb package for Ubuntu
Xenial for the journald-notify tool.

In order to get the package once you have built the image, run the container
and mount a volume at /data inside of the container.

Note that the generated package does NOT introduce a dependency on the
python3-click package in the Xenial repositories. You will need to use pip3
to install the click package manually. You will also need to use pip3 to install
the proc package should you wish to use the notify-send-headless command with
the notify-send notifier.

https://github.com/djmattyg007/journald-notify
