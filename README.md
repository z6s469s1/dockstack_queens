# dockstack_queens

## requirement
- ubuntu 18.04
- docker
- docker compose

## installation
```console
$ https://github.com/z6s469s1/dockstack_queens.git
$ cd DockStack
$ make
$ docker exec --tty --interactive  dockstack  bash
```


## debug
- docker error creating aufs mount to xxxx
https://stackoverflow.com/questions/38514361/docker-error-creating-aufs-mounts-invalid-argument-booting-from-live-usb
Change /etc/default/docker to have this in it:
```console
DOCKER_OPTS="--storage-driver=devicemapper"
```

## ref
https://github.com/janmattfeld/DockStack
