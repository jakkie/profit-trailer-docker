# profit-trailer-docker

Profit Trailer Docker

[![Docker Pulls](https://img.shields.io/docker/pulls/jakkie/profit-trailer-docker.svg)](https://hub.docker.com/r/jakkie/profit-trailer-docker/)
[![](https://images.microbadger.com/badges/image/jakkie/profit-trailer-docker.svg)](https://microbadger.com/images/jakkie/profit-trailer-docker "Get your own image badge on microbadger.com")
[![](https://images.microbadger.com/badges/version/jakkie/profit-trailer-docker.svg)](https://microbadger.com/images/jakkie/profit-trailer-docker "Get your own version badge on microbadger.com")
[![Docker Build Status](https://img.shields.io/docker/build/jakkie/profit-trailer-docker.svg)](https://hub.docker.com/r/jakkie/profit-trailer-docker/)

Compatible with Profit Trailer bot version : v2.1.3
`https://wiki.profittrailer.com/doku.php?id=start`

## Install Docker

- Windows `https://docs.docker.com/toolbox/toolbox_install_windows/`
- Mac OS `https://docs.docker.com/docker-for-mac/install/`
- Linux Ubuntu `https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-ce`

## Quick Guide

### Run latest Profit Trailer version

- download the configure files from `https://github.com/jakkie/profit-trailer-docker/blob/master/configs`
- Edit all configs especially application.properties with your license key and exchange apis, other wise the bot will not start. See for `https://wiki.profittrailer.com/doku.php?id=start` reference.
- To Run Container and replace `<your path>` with the full path where the config files are.

```bash
docker run -v <your path>/application.properties:/app/ProfitTrailer/application.properties -v <your path>/initialization:/app/ProfitTrailer/initialization -p 8081:8081 --name pt jakkie/profit-trailer-docker
```

- After Profit Trailer is running browse to the url example `http://your-ip:8081`

```bash
http://localhost:8081
```

## DIY Guide

### Installing the container

- Build the container from the Dockerfile.

```bash
docker build -t profit-trailer .
```

- To build with a specific Profit Trailer version from version v2.1.3 and later. Just change the Profit Trailer version to the version you want. To see which versions are available go to `https://github.com/taniman/profit-trailer/releases`

```bash
docker build -t profit-trailer --build-arg PT_VERSION=2.1.3 .
```

### Running Profit Trailer with docker-compose

- To install docker compose see `https://docs.docker.com/compose/install/`
- Copy your configs files to where your docker-compose file is.
- To start docker-compose to run the container.

```bash
docker-compose up -d
```

- After Profit Trailer is running check the Profit Trailer logs.

```bash
docker logs profittrailer
```

### Upgrade to new version

- To upgrade to the latest Profit Trailer bot version, pull the latest version from docker hub.

```bash
docker-compose pull
```

- Stop and remove container.

```bash
docker-compose down
```

- Run it again.

```bash
docker-compose up -d
```

Donations are also very welcomed and appreciated:

BTC: 1JvpPGe22ViBYNiNrA3nwtg71Jta5vqXAi

BCH: qzndnssc368k5h5ndg6h2d5pewmkycd50c9gxcpre6

LTC: LWRDbKva26cATarA2PoTXTpKVJwCRCzbNC

ETH: 0x13346b1DcF1f923bD357a1C8900C4475342e5255

ZEC: t1YgFzgYdRymwJcwTBaS1harBf1sPakgbZ4

DASH: XanACebtJkEZsfRaMahbnqCU4LPt42e3mE