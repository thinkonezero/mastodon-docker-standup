# mastodon-docker-standup

## Getting started

Environment Variables:

```
### 
###  --------------------------------------------------------------
###  M A S T O D O N - D O C K E R   C O N F I G   S E T T I N G S
###  ---------------------------------------------------------------
###  The values configured here are applied during
###  $ docker-compose up
###  -----------------------------------------------
###  DOCKER-COMPOSE ENVIRONMENT VARIABLES BEGIN HERE
###  -----------------------------------------------
###

PUID=
PGID=
TZ=
LOG_FILE_NUM=5
LOG_FILE_SIZE=10m
LOCAL_DOMAIN=
CLOUDFLARED_TOKEN=
STACK_NAME=
BASE_DOCKER_PATH=/volume1/docker
MASTODON_DB_USER=mastodon
MASTODON_DB_NAME=mastodon
MASTODON_DB_PASS=mastodon
MASTODON_SECRET_KEY_BASE=
MASTODON_OTP_SECRET=
MASTODON_VAPID_PRIVATE_KEY=
MASTONDON_VAPID_PUBLIC_KEY=
SMTP_SERVER=mail.example.com
SMTP_PORT=25
SMTP_LOGIN=
SMTP_PASSWORD=
SMTP_FROM_ADDRESS=notifications@example.com
```

To generate keys for SECRET_KEY_BASE & OTP_SECRET run `docker run --rm -it -w /app/www --entrypoint rake lscr.io/linuxserver/mastodon secret` once for each.

To generate keys for VAPID_PRIVATE_KEY & VAPID_PUBLIC_KEY run `docker run --rm -it -w /app/www --entrypoint rake lscr.io/linuxserver/mastodon mastodon:webpush:generate_vapid_key`
