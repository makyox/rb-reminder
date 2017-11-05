# Recalbox

## Make system writable
```
mount -o remount,rw /dev/root
```

## Build Root

clone build root

Install dependencies based on the DockerFile:
```
apt-get update -y
apt-get -y install build-essential git libncurses5-dev qt5-default qttools5-dev-tools mercurial libdbus-glib-1-dev texinfo zip openssh-client libxml2-utils software-properties-common wget cpio bc locales rsync imagemagick nano vim automake mtools dosfstools subversion openjdk-8-jdk libssl-dev
```

Build it
```
make list-defconfigs
make raspberrypi3_defconfig
```

## Build a custom EmulationStation

In the build root, replace the output/build emulation-station folder by your updated sources (does not support symlink)

```
cd /recalbox/output/build/
rm -rf recalbox-emulationstation2-c4c4ad6e416a285400f6a2016b40f65224e4ceae
cp -R /path-to-your-custom/recalbox-emulationstation/ recalbox-emulationstation2-c4c4ad6e416a285400f6a2016b40f65224e4ceae
cd /recalbox/
make recalbox-emulationstation2-build
```
