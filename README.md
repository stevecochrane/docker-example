# docker-example

Here's my example code as I learn [Docker](https://www.docker.com) by working
through the [Shipping Docker](https://shippingdocker.com) video series. So far,
this can be used to start up a web application with four services: PHP, MYSQL,
NGINX, and Redis, all configured to connect to each other on the same virtual
network.

If you'd like to give this a try you'll need to have Docker installed. The
application itself is not included here but if you add an `/application/public`
directory with an `index.php` file inside, that should be what you see when you
start this up.

To run with the default configuration:

```bash
docker-compose up -d
```

To run with a configuration that accepts environment variables:

``` bash
docker-compose -f docker-compose.var.yml up -d
```

To run with an extended configuration that adds to a base file:

``` bash
docker-compose -f docker-compose.base.yml -f docker-compose.dev.yml up -d
```

To run with an extended configuration that extends a base file:

``` bash
docker-compose -f docker-compose.extends.yml up -d
```
