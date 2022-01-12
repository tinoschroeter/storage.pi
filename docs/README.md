# Storage

![pi storage](https://raw.githubusercontent.com/tinoschroeter/storage.pi/master/docs/storage.jpg)

[![k3s](https://img.shields.io/badge/run%20on%20-Raspberry%20Pi-red)](https://github.com/tinoschroeter/k8s.homelab)
[![GitHub Super-Linter](https://github.com/tinoschroeter/storage.pi/workflows/Lint%20Code%20Base/badge.svg)](https://github.com/tinoschroeter/storage.pi/actions/workflows/linter.yml)

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

zpool destroy data
zfs snapshot [pool]/[dataset name]@[snapshot name]
zfs list -t snapshot
zfs rollback -r [pool]/[dataset]@[snapshot name]
```

[power 2 external usb 3hdds](https://raspberrypi.stackexchange.com/questions/104038/can-the-pi-4-power-2-external-usb-3-hdds)

[ZFS Cheat Sheet](https://www.thegeekdiary.com/solaris-zfs-command-line-reference-cheat-sheet/)
