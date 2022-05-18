# build-gost-nginx

This is a Dockerfile and Gitlab CI pipeline to build Nginx with GOST encryption capability.

Inspired by [https://github.com/rnixik/docker-openssl-gost/tree/master/nginx-gost](https://github.com/rnixik/docker-openssl-gost/tree/master/nginx-gost).

## How-to

Command line to build image:

```bash
docker build
      -t ${built_image_tag}
      --build-arg NGINX_VERSION=${nginx_version}
      --build-arg OPENSSL_VERSION=${openssl_version}
      --build-arg GOST_ENGINE_VERSION=${gost_engine_version}
      -f "Dockerfile"
```

Gitlab:

* Add pipeline and commit .gitlab-ci.yml
