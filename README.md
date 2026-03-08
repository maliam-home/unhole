# PiHole

## Pihole Network

### Network for using static IP address

```sh
docker network create -d macvlan --opt parent=ens1 --subnet=192.168.0.0/24 --gateway=192.168.0.1 --ip-range=192.168.0.192/26 mcvlan0
```

## Deploy in Portainer

when you are going to deploy in Portainer, you need to create first a shared folder like `/opt/stacks`, where you are going to save the github repo downloaded, we recommend to create. Also for saving passwords you might want to create the following file in

```sh
/opt/stacks/unhole/.secrets/webpassword.txt
```

## References
