# graalnative4s

Employ Scala for serverless applications

![build](https://img.shields.io/github/workflow/status/usommerl/graalnative4s/CI?style=for-the-badge)
[![codecov](https://img.shields.io/codecov/c/github/usommerl/graalnative4s?style=for-the-badge)](https://codecov.io/gh/usommerl/graalnative4s)

## Rationale
This is a showcase project for a combination of purely functional Scala libraries that can be used with GraalVM native image without much effort. It uses [http4s][http4s] for general server functionality, [circe][circe] for JSON processing, [tapir][tapir] to describe HTTP endpoints and [odin][odin] for logging. Applications that where built with Graal have beneficial properties such as lower memory consumption and fast startup. This makes them suitable for serverless use cases.

### Build
Use `sbt docker` to build a docker image with the native image binary. You don't need to install anything, the build process downloads all required GraalVM tooling. The [created image][image] will be as minimal as possible by using a multi-stage build.

### Deploy
This repository contains a [workflow][workflow] that will deploy the created image to Google Cloud Run. You could also use the button below to deploy it to your own GCP account.

[![Run on Google Cloud](https://deploy.cloud.run/button.svg)](https://deploy.cloud.run)

### Try
The most recent version of this sample application is online here: [https://graalnative4s.usommerl.dev](https://graalnative4s.usommerl.dev)

### Attribution & Contribution
I have taken a lot of inspiration and knowledge from [this blog post by James Ward][inspiration]. You should also check out his [hello-uzhttp][uzhttp] example. Suggestions and contributions are welcome.

[http4s]: https://github.com/http4s/http4s
[circe]: https://github.com/circe/circe
[tapir]: https://github.com/softwaremill/tapir
[odin]: https://github.com/valskalla/odin

[image]: https://github.com/users/usommerl/packages/container/package/graalnative4s
[workflow]: .github/workflows/ci_cd.yaml
[inspiration]: https://jamesward.com/2020/05/07/graalvm-native-image-tips-tricks/
[uzhttp]: https://github.com/jamesward/hello-uzhttp

