# dev env prepare

## install docker

[follow the steps](https://docs.docker.com/install/linux/docker-ce/centos/)

### change docker root dir

use soft link

```
systemctl stop docker
mv /var/lib/docker /data/docker
ln -s /data/docker /var/lib/docker
systemctl start docker
```
