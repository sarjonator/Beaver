<p align="center">
    <img alt="Beaver Logo" src="https://raw.githubusercontent.com/Clivern/Beaver/master/assets/img/logo.png" height="80" />
    <h3 align="center">Beaver</h3>
    <p align="center">A Real Time Messaging Server.</p>
</p>

## Documentation

### Config & Run The Application

Hamster uses [dep](https://github.com/golang/dep) to manage dependencies so you need to install it

```bash
# For latest dep version
$ curl https://raw.githubusercontent.com/golang/dep/master/install.sh | sh

# For latest stable version
$ curl https://raw.githubusercontent.com/golang/dep/v0.5.0/install.sh | sh

$ dep ensure
```

Then Create a dist config file.

```bash
$ cp config.json config.dist.json
```

Then add your `app_mode`, `app_port`, `app_log_level`, `app_domain`, `log_path`, `redis_*`, `api_token` ...etc.

```json
{
    "app_mode": "dev",
    "app_port": "8080",
    "app_log_level": "info",
    "app_domain": "example.com",
    "log_path": "var/logs",
    "redis_addr": "127.0.0.1:6379",
    "redis_password": "",
    "redis_db": "0",
    "api_token": "123"
}
```

And then run the application.

```bash
$ go build beaver.go
$ ./beaver

// OR

$ go run beaver.go

// To Provide a custom config file
$ ./beaver -config=/custom/path/config.dist.json
$ go run beaver.go -config=/custom/path/config.dist.json
```

Also running beaver with docker still an option. Just don't forget to update environment variables on `docker-compose.yml` file. Then run the following stuff

```bash
$ docker-compose build
$ docker-compose up -d
```

## Badges

[![Build Status](https://travis-ci.org/Clivern/Beaver.svg?branch=master)](https://travis-ci.org/Clivern/Beaver)
[![GitHub license](https://img.shields.io/github/license/Clivern/Beaver.svg)](https://github.com/Clivern/Beaver/blob/master/LICENSE)
[![Version](https://img.shields.io/badge/Version-Under%20Development-red.svg)](https://github.com/Clivern/Beaver/releases)
[![Go Report Card](https://goreportcard.com/badge/github.com/Clivern/Beaver)](https://goreportcard.com/report/github.com/Clivern/Beaver)


## Changelog

* Version 1.0.0:
```
Initial Release.
```


## Acknowledgements

© 2018, Clivern. Released under [MIT License](https://opensource.org/licenses/mit-license.php).

**Beaver** is authored and maintained by [@Clivern](http://github.com/clivern).