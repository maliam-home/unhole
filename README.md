# Unhole

Pi-hole + Unbound DNS stack with ad-blocking, local resolution, and encrypted upstream (DoT).

## Quick start

1. Create a shared folder (e.g. `/opt/stacks`) and clone this repo then `cd unhole`
2. Copy `.env.example` to `.env` and adjust values
3. For passwords, you can use `.env` (ensure it's in `.gitignore`)
4. Ensure `proxy0` and `macvlan0` networks exist, see below for how to create
5. Run `docker compose up -d`

## Pihole Network

### Network for static IP address

```sh
docker network create -d macvlan --opt parent=ens1 --subnet=192.168.0.0/24 --gateway=192.168.0.1 --ip-range=192.168.0.192/26 macvlan0
docker network create -d bridge --subnet=172.19.0.0/24 --gateway=172.19.0.1 --ip-range=172.19.0.0/24 proxy0
```

## Troubleshoot

In case of accesing via url or ping is not working in your mac, do this

```sh
sudo killall mDNSResponder; sudo mDNSResponder -v
# Now, in another terminal window, try:
ping jolt.maliam.net
```

## References
