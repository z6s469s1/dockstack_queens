# dockstack_queens

## requirement
- ubuntu 18.04
- docker as root
https://ithelp.ithome.com.tw/articles/10239123


```console
$ sudo apt install make      
$ sudo apt install make-guile
```

## installation
```console
$ git clone https://github.com/z6s469s1/dockstack_queens.git
$ cd dockstack_queens
$ make
$ docker exec --tty --interactive  dockstack  bash
```


## debug
- docker error creating aufs mount to xxxx </br>
https://stackoverflow.com/questions/38514361/docker-error-creating-aufs-mounts-invalid-argument-booting-from-live-usb </br>
Change /etc/default/docker to have this in it:
```console
DOCKER_OPTS="--storage-driver=devicemapper"
```
- create instance error </br>
wait 60min and then executre below commands
```console
$ docker stop dockstack
$ docker start dockstack
```

## ref
https://github.com/janmattfeld/DockStack
