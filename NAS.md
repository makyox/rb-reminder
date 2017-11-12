Make the system writable
```
mount -o remount,rw /dev/root
```

Edit the file `/boot/recalbox-boot.conf`

```
sharedevice=NETWORK

sharenetwork_smb1=SHARE@192.168.0.10:Public/recalbox/share:guest
sharenetwork_smb2=BIOS@192.168.0.10:Public/recalbox/bios:guest
sharenetwork_smb3=ROMS@192.168.0.10:Public/recalbox/roms:guest
sharenetwork_smb4=SAVES@192.168.0.10:Public/recalbox/saves:guest
```
