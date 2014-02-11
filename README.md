Docker PHP (with OCI8 support) base image definition set up with day-to-day PHP development tools.

Usage
=====

In your Dockerfile, use the following as the first line to build on this base image:

```
    FROM fabrizzio/docker-php-oci8
```

Important
=========

When running a container based on this base image, the `/etc/tnsnames.ora` has to be mounted at runtime using the `-v` flag:

```
    docker run -v /etc/tnsnames.ora:/etc/tnsnames.ora fabrizzio/docker-php-oci8
```
