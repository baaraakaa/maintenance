# Maintenance Page
A simple static maintenance page in a docker-compose

`master` branch on this repo will not run locally, it attempts to set up SSL certs with certbot, this requires an active domain pointing at your machine and open ports.

The `local` branch exposes port 8080 and does not set up SSL, use this for local dev.

## Dependencies
docker-compose or compatible alternative

## Usage
- Adjust the static html in this repo's `/webroot` to your liking
- change`server_name localhost` in `conf.d/nginx.conf` to your domain i.e. `server_name example.com`
- set `CERTBOT_EMAIL` environment variable, many ways to do this, but you can just do `echo "CERTBOT_EMAIL=user@example.com" >> .env` in the root of this directory (with your own email address obviously)
- run with `docker-compose up`


[Photo by Arthur Brognoli from Pexels](https://www.pexels.com/photo/high-angle-shot-of-mountain-2327372)