# tftp server with write access

To build

```
docker build --rm --tag=princeamd/tftp .
```

To run

```
docker run -p 0.0.0.0:69:69/udp -i -t princeamd/tftp
```

Mounts the following volume for persistent data

```
/var/tftpboot
```

To map the volume to a host directory

```
docker run --restart=always --name thomas-tftpd -p 0.0.0.0:69:69/udp -v /var/tftpboot:/var/tftpboot -i -d princeamd/tftp
```
