# PiHole

## Pihole Network

### Network for using static IP address

```sh
# when using static address in the container
docker network create -d qnet --opt iface=eth0 --ipam-driver qnet --ipam-opt iface=eth0 --subnet=192.168.0.0/22 --gateway=192.168.0.1 qnet-vlan0
# when you have Port Trunking
docker network create -d qnet --opt iface=bond0 --ipam-driver qnet --ipam-opt iface=bond0 --subnet=192.168.0.0/22 --gateway=192.168.0.1 qnet-vlan0
```

### Network for using DHCP

```sh
docker network create -d qnet --opt=iface=eth0 --ipam-driver=qnet --ipam-opt=iface=eth0 qnet-vlan1
```

## References

[Qnet](https://qnap-dev.github.io/container-station-api/qnet.html)
