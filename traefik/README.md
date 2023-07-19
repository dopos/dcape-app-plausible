# Using plausible with traefik plugin

* [traefik](https://traefik.io/)
* [Plausible Feeder Traefik Plugin](https://plugins.traefik.io/plugins/6436731fcb56144f9bdcb473/plausible-feeder)
* [Plausible Feeder Traefik Plugin repo](https://github.com/safing/plausiblefeeder)

## Requirements

Host with traefik and plausible installed

## Install

### 1. Add plugin into traefik static config (traefik.yml)

```
experimental:
  plugins:
    plausiblefeeder:
      moduleName: "github.com/safing/plausiblefeeder"
      version: "v1.0.0"

```

### 2. Add plugin config into traefik dynamic config ([custom/plausible.yml](plausible.yml))


### 3. Add app labels

```
    labels:
      - "traefik.http.routers.APP_TAG.middlewares=my-plausiblefeeder@file"
```

## Endpoint notes

There is mistake in [traefik plugin](https://github.com/safing/plausiblefeeder/blob/master/.traefik.yml#L21) probably.
Correct endpoint is `/api/event` as noted in [plausible docs](https://plausible.io/docs/events-api)

```
                    eventEndpoint: http://plausible:8000/api/event
```

