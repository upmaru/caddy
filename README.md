# Uplink Caddy

Custom build of caddy for use with [uplink](https://github.com/upmaru/uplink). This configuration builds caddy into a `.apk` alpine package.

## Modules

Modules included in this build configuration:

- [certmagic-s3](https://github.com/ss098/certmagic-s3) for storing ssl certificate in s3 bucket.
- [cache-handler](https://github.com/caddyserver/cache-handler) for cache handling.

## Configuration

You may notice the `config.json` and it has a reference to `http://localhost:4080/caddy`. This is `uplink`'s internal service that supplies caddy with the initial configuration. Since caddy will run inside the same container as `uplink` it has access to this internal service.

Once caddy starts it will call the endpoing in the configuration to fetch it's initial configuration.

## Supervision

The build tool will make sure caddy is supervised by the `s6` supervisor and output logs to stdout. Logs will be handled by the `s6-log` program.

