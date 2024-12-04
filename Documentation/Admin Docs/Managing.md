# Certbot

The swag container includes certbot for automatic SSL certificate generation and renewal. We use http validation for this, which is why port 80 is opened for this container. See the docker-swag resource.

# Nginx reverse proxy

Nginx serves as our reverse proxy. It comes with premade proxy config files located under:

```
/config/nginx/proxy-confs
```