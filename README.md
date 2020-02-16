# redis

[![Build Status](https://cloud.drone.io/api/badges/rolehippie/redis/status.svg)](https://cloud.drone.io/rolehippie/redis)

Ansible role to configure redis

## Table of content

* [Default Variables](#default-variables)
  * [redis_databases](#redis_databases)
  * [redis_image](#redis_image)
  * [redis_maxconn](#redis_maxconn)
  * [redis_network](#redis_network)
  * [redis_publish](#redis_publish)
  * [redis_publish_server](#redis_publish_server)
  * [redis_volume_server](#redis_volume_server)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

## Default Variables

### redis_databases

Number of databases to create

#### Default value

```YAML
redis_databases: 1
```

### redis_image

Docker image to use

#### Default value

```YAML
redis_image: webhippie/redis:latest
```

### redis_maxconn

Max allowed connections

#### Default value

```YAML
redis_maxconn: 10000
```

### redis_network

Docker network to connect to

#### Default value

```YAML
redis_network: traefik
```

### redis_publish

Publish the service on that binding

### redis_publish_server

#### Default value

```YAML
redis_publish_server: 127.0.0.1:6379
```

### redis_volume_server

Path to server volume

#### Default value

```YAML
redis_volume_server: /var/lib/redis
```

## Dependencies

None.

## License

Apache-2.0

## Author

Thomas Boerger
