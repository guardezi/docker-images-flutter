# Docker Images for [Flutter](https://flutter.dev/) 2.10

[![Docker Image CI](https://github.com/Silicon-Village-Tech/docker-images-flutter/actions/workflows/docker-image.yml/badge.svg)](https://github.com/Silicon-Village-Tech/docker-images-flutter/actions/workflows/docker-image.yml)


You can either [use it in CI](https://cirrus-ci.org/examples/#flutter) or run locally via Docker:

```bash
docker run --rm -it -v ${PWD}:/build --workdir /build cirrusci/flutter:stable flutter test
```

The example above simply mount current working directory and runs `flutter test`

## Available Docker Tags

[![](https://images.microbadger.com/badges/version/cirrusci/flutter:latest.svg)](https://microbadger.com/images/cirrusci/flutter:latest) [![](https://images.microbadger.com/badges/image/cirrusci/flutter:latest.svg)](https://microbadger.com/images/cirrusci/flutter:latest)

[![](https://images.microbadger.com/badges/version/cirrusci/flutter:stable.svg)](https://microbadger.com/images/cirrusci/flutter:stable) [![](https://images.microbadger.com/badges/image/cirrusci/flutter:stable.svg)](https://microbadger.com/images/cirrusci/flutter:stable)

[![](https://images.microbadger.com/badges/version/cirrusci/flutter:beta.svg)](https://microbadger.com/images/cirrusci/flutter:beta) [![](https://images.microbadger.com/badges/image/cirrusci/flutter:beta.svg)](https://microbadger.com/images/cirrusci/flutter:beta)

[![](https://images.microbadger.com/badges/version/cirrusci/flutter:dev.svg)](https://microbadger.com/images/cirrusci/flutter:dev) [![](https://images.microbadger.com/badges/image/cirrusci/flutter:dev.svg)](https://microbadger.com/images/cirrusci/flutter:dev)
