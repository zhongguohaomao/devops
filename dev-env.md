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

## install zsh and autojump

install zsh
```
yum install zsh -y
chsh -s /bin/zsh
yum install git -y
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

install autojump
```
yum install autojump -y
yum install autojump-zsh -y
```

modify `~/.zshrc`
```
plugins=(git autojump)
```
