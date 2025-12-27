# Redis for FreeBSD

Redis key-value store for [Immich](https://immich.app/) and other applications.

## Usage

```bash
podman run -d --name redis \
  -v /containers/redis:/config \
  ghcr.io/daemonless/redis:latest
```

## Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| REDIS_DATA | /config/data | Data directory |

## Volumes

- `/config` - Configuration and data directory

## Ports

- `6379` - Redis

## Configuration

A default `redis.conf` is created on first run at `/config/redis.conf`. Edit to customize.

Default settings:
- Bind: 0.0.0.0
- Append-only mode enabled
- Protected mode disabled (for container use)
