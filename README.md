# Firebird Legacy Docker images (GHCR)

Unofficial GHCR builds of legacy Firebird images based on
[jacobalberty/firebird-docker](https://github.com/jacobalberty/firebird-docker/).

> ⚠️ Firebird 2.5 is EOL. Use only for legacy compatibility.


[![GHCR](https://img.shields.io/badge/GHCR-available-blue?logo=github)](https://github.com/pavlozt/firebird-legacy-docker/pkgs/container/firebird-legacy-docker)

I created this project to use GHCR.  
The original project is located at: [https://github.com/jacobalberty/firebird-docker/](https://github.com/jacobalberty/firebird-docker/).
You can use the images for yourself.  


## 📦 Images

Images are available in [GHCR](https://github.com/pavlozt/firebird-legacy-docker/pkgs/container/firebird-legacy-docker). 

try use it:

```
docker pull ghcr.io/pavlozt/firebird-legacy-docker:2.5-ss
```

## Quick start

```bash
docker pull ghcr.io/pavlozt/firebird-legacy-docker:2.5-ss

docker run -d \
  --name firebird \
  -p 3050:3050 \
  -e ISC_PASSWORD=masterkey \
  -e FIREBIRD_DATABASE=example.fdb \
  -v firebird_data:/firebird/data \
  ghcr.io/pavlozt/firebird-legacy-docker:2.5-ss
