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
  - [redis_cpu_shares](#redis_cpu_shares)
  - [redis_databases](#redis_databases)
  - [redis_default_labels](#redis_default_labels)
  - [redis_default_publish](#redis_default_publish)
  - [redis_default_volumes](#redis_default_volumes)
  - [redis_extra_labels](#redis_extra_labels)
  - [redis_extra_publish](#redis_extra_publish)
  - [redis_extra_volumes](#redis_extra_volumes)
  - [redis_group](#redis_group)
  - [redis_image](#redis_image)
  - [redis_maxconn](#redis_maxconn)
  - [redis_memory_limit](#redis_memory_limit)
  - [redis_memory_soft_limit](#redis_memory_soft_limit)
  - [redis_memory_swap](#redis_memory_swap)
  - [redis_network](#redis_network)
  - [redis_number_of_cpus](#redis_number_of_cpus)
  - [redis_pull_image](#redis_pull_image)
  - [redis_user](#redis_user)
  - [redis_volume_server](#redis_volume_server)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### redis_cpu_shares

CPU shares with Docker deployment

#### Default value

```YAML
redis_cpu_shares:
```

#### Example usage

```YAML
redis_cpu_shares: '512'
```

### redis_databases

Number of databases to create

#### Default value

```YAML
redis_databases: 1
```

### redis_default_labels

List of default labels to assign to docker

#### Default value

```YAML
redis_default_labels: []
```

### redis_default_publish

List of default port publishing for docker

#### Default value

```YAML
redis_default_publish: []
```

#### Example usage

```YAML
redis_default_publish:
  - 127.0.0.1:6379:6379
```

### redis_default_volumes

List of default volumes to mount for docker

#### Default value

```YAML
redis_default_volumes:
  - '{{ redis_volume_server }}:/var/lib/redis'
```

### redis_extra_labels

List of extra labels to assign to docker

#### Default value

```YAML
redis_extra_labels: []
```

### redis_extra_publish

List of extra port publishing for docker

#### Default value

```YAML
redis_extra_publish: []
```

#### Example usage

```YAML
redis_extra_publish:
  - 127.0.0.1:6379:6379
```

### redis_extra_volumes

List of extra volumes to mount for docker

#### Default value

```YAML
redis_extra_volumes: []
```

#### Example usage

```YAML
redis_extra_volumes:
  - /path/to/host/folder1:/path/within/container1
  - /path/to/host/folder2:/path/within/container2
  - /path/to/host/folder3:/path/within/container3
```

### redis_group

System group for the Redis service

#### Default value

```YAML
redis_group: redis
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

### redis_memory_limit

Memory limit with Docker deployment

#### Default value

```YAML
redis_memory_limit:
```

#### Example usage

```YAML
redis_memory_limit: 1024m
```

### redis_memory_soft_limit

Soft memory limit with Docker deployment

#### Default value

```YAML
redis_memory_soft_limit:
```

#### Example usage

```YAML
redis_memory_soft_limit: 512m
```

### redis_memory_swap

Swap usage with Docker deployment

#### Default value

```YAML
redis_memory_swap:
```

#### Example usage

```YAML
redis_memory_swap: 2048m
```

### redis_network

Optional docker network to attach

#### Default value

```YAML
redis_network:
```

### redis_number_of_cpus

Number of CPUs with Docker deployment

#### Default value

```YAML
redis_number_of_cpus:
```

#### Example usage

```YAML
redis_number_of_cpus: '1.0'
```

### redis_pull_image

Pull image as part of the tasks

#### Default value

```YAML
redis_pull_image: true
```

### redis_user

System user for the Redis service

#### Default value

```YAML
redis_user: redis
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
