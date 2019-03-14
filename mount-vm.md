## mount vm on centos 7.6

given a new vm, how to mount

### make partition
check disk
```
fdisk -l
fdisk /dev/vdb
```

command sequence
n - new a partition
p - parimay partition
1
enter
enter
w

### format disk and mount

```
mkfs.xfs /dev/vdb1
mkdir /data
mount /dev/vdb1 /data
```

### auto mount

```
echo "/dev/vdb1 /data xfs defaults 0 0" >> /etc/fstab
```
