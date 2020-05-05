# mc
自作コンテナっぽいことをする

## rootfsの作り方
docker export $(docker create busybox) | tar -C rootfs -xvf -

## howtorun
```
mkdir rootfs
docker export $(docker create busybox) | tar -C rootfs -xvf -
go build main.go
sudo ./main
# you are in a container
```
