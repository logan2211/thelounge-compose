# thelounge-compose

A docker-compose implementation of thelounge fronted by an nginx https proxy.

[![Build Status](https://travis-ci.org/logan2211/thelounge-compose.svg?branch=master)](https://travis-ci.org/logan2211/thelounge-compose)

## Requirements

- [docker](https://docs.docker.com/install/)
- [docker-compose](https://docs.docker.com/compose/install/)

## Install

1. Clone the repo
2. `cd thelounge-compose/nginx; ./genkey; cd ../`
3. Alternatively, populate `thelounge-compose/nginx/cert.{pem,key}`
4. `docker-compose up -d`
5. The service is available by default using https://<ip>:4600

### Disable Public Mode
1. Disable public mode: `sed -ir 's/public: true/public: false/' thelounge/config/config.js`
2. Restart thelounge: `docker-compose stop thelounge; docker-compose start thelounge`
3. Create a user: `docker-compose exec thelounge thelounge add <username>`

## License

Apache2

## Author Information

Logan V.
