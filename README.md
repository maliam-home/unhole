# Unhole

Pi-hole + Unbound DNS stack with ad-blocking, local resolution, and encrypted upstream (DoT).

## Quick start

1. Copy `.env.example` to `.env` and adjust values
2. Ensure `proxy` networks exist
3. Run `docker compose up -d`

## Pihole Network

### Network for static IP address

```sh
docker network create proxy
```

## Deploy in Portainer

1. Create a shared folder (e.g. `/opt/stacks`) and clone this repo
2. Copy `.env.example` to `.env` and set your values
3. For Portainer, set `UNBOUND_DATA_PATH=/opt/stacks/unhole/unbound` so the Unbound volume uses the correct path
4. For passwords, you can use `.env` (ensure it's in `.gitignore`)

## References
