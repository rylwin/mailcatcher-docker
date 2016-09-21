# Mailcatcher Docker [![](https://images.microbadger.com/badges/version/rylwin/mailcatcher.svg)](https://hub.docker.com/r/rylwin/mailcatcher/)

The smallest [mailcatcher] docker image there is.
[![](https://images.microbadger.com/badges/image/rylwin/mailcatcher.svg)](https://microbadger.com/images/rylwin/mailcatcher
"Get your own image badge on microbadger.com")

## Usage

The mailcatcher gem serves as a local SMTP server (and HTTP-based email client)
to facilitate working with emails during development.

To run the image with docker:
`docker run -p 1080:1080 -p 1025:1025 rylwin/mailcatcher`.

And to use with docker compose, add the following service to your
`docker-compose.yml`:

```
email:
  image: rylwin/mailcatcher
  ports:
    - "1025:1025"
    - "1080:1080"
```

[mailcatcher]: https://github.com/sj26/mailcatcher
