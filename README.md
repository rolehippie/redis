# redis

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/redis)
[![General Workflow](https://github.com/rolehippie/redis/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/redis/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/redis/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/redis/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/redis/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/redis/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/redis)](https://github.com/rolehippie/redis/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.redis-blue)](https://galaxy.ansible.com/rolehippie/redis)

Ansible role to install and configure redis key-value store.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of contents

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [redis_databases](#redis_databases)
  - [redis_image](#redis_image)
  - [redis_maxconn](#redis_maxconn)
  - [redis_network](#redis_network)
  - [redis_publish](#redis_publish)
  - [redis_publish_server](#redis_publish_server)
  - [redis_pull_image](#redis_pull_image)
  - [redis_volume_server](#redis_volume_server)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

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
redis_network:
```

#### Example usage

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

### redis_pull_image

Pull image as part of the tasks

#### Default value

```YAML
redis_pull_image: true
```

### redis_volume_server

Path to server volume

#### Default value

```YAML
redis_volume_server: /var/lib/redis
```

## Discovered Tags

**_redis_**

## Dependencies

- [rolehippie.docker](https://github.com/rolehippie/docker)
- [community.docker](https://github.com/ansible-collections/community.docker)

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
