# Gunicorn NGINX proxy

This is a simple docker image based on the official [nginx](https://hub.docker.com/_/nginx) docker image, which includes a template based on some of recommendations from [gunicorn docs](https://docs.gunicorn.org/en/latest/deploy.html).

## How to

Originally, this image is meant to be run as a service in `docker compose`, together with the `gunicorn` app that needs to be proxied.

- Add this container to the same network as the `gunicorn` app (e.g. add it as a service in `docker-compose.yml`).
- Edit port bindings in `docker-compose.yml` to suit your needs, and set `TARGET_HOSTNAME` to the hostname of the target container.
