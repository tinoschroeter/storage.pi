# Storage

```shell
ansible-playbook storage.yaml -i inventory
```

```shell
/boot/firmware/config.txt
gpu_mem=16
max_usb_current=1
program_usb_timeout=1
dtoverlay=disable-wifi
dtoverlay=disable-bt
```

```shell
zpool create data /dev/sda
zfs set mountpoint=/mnt/data data

zpool list
zpool status

zfs snapshot [pool]/[dataset name]@[snapshot name]
zfs list -t snapshot
zfs rollback -r [pool]/[dataset]@[snapshot name]
```

[power 2 external usb 3 hdds](https://raspberrypi.stackexchange.com/questions/104038/can-the-pi-4-power-2-external-usb-3-hdds)

[ZFS Cheat Sheet](https://www.thegeekdiary.com/solaris-zfs-command-line-reference-cheat-sheet/)
