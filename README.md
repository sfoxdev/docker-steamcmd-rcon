# steamcmd-rcon

Barebone steamcmd in Ubuntu with rcon healthcheck

[![Docker Build Status](https://img.shields.io/docker/build/sfoxdev/steamcmd-rcon.svg?style=flat-square)]()
[![Docker Build Status](https://img.shields.io/docker/automated/sfoxdev/steamcmd-rcon.svg?style=flat-square)]()
[![Docker Build Status](https://img.shields.io/docker/pulls/sfoxdev/steamcmd-rcon.svg?style=flat-square)]()
[![Docker Build Status](https://img.shields.io/docker/stars/sfoxdev/steamcmd-rcon.svg?style=flat-square)]()

## Usage

### Envs

See [sfoxdev/steamcmd](https://hub.docker.com/r/sfoxdev/steamcmd/) plus

- `RCON_HOST=xyz` (default `localhost`): host of the rcon server, in case it is bound to a specific address
- `RCON_PORT=xyz` (default `27015`): port of the rcon server
- `RCON_PASS=xyz` (default `""`): password of the rcon server
- `RCON_HEALTH_COMMAND` (**mandatory**): command that is transmitted to the server which must responded with a non-zero-length answer for the container to be considered healthy
- `RCON_HEALTH_REGEXP` (default `""`): regexp that, if set, must match the rcon response for the container to be considered healthy

## Credits

- Uses SourceRcon.py from [frostschutz/SourceLib](https://github.com/frostschutz/SourceLib) under MIT license
