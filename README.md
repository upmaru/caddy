# Uplink Caddy

Custom build of caddy for use with [uplink](https://github.com/upmaru/uplink). This configuration builds caddy into a `.apk` alpine package.

## Modules

Modules included in this build configuration:

- [certmagic-s3](https://github.com/ss098/certmagic-s3) for storing ssl certificate in s3 bucket.
- [cache-handler](https://github.com/caddyserver/cache-handler) for cache handling.