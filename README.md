# openwrt-extras

An additional OpenWRT packages feed for extra packages.

## Included packages

* rsyslog
* libestr (required for rsyslog)

## Usage

Edit `feeds.conf` in the OpenWRT source directory and add the following line:

    src-git extras https://github.com/ibm-security-innovation/openwrt-extras.git

Update the feeds (fetch the latest package definitions from GitHub):

    scripts/feeds update extras

Activate packages:

    scripts/feeds install -a -p extras

Run `make menuconfig` to select the relevant packages to be included in the
OpenWRT build.
