# nodejs-webapp-demo
Sample nodejs app on docker

- create `package.json`
- crate `server.js`
- create `Dockerfile`
- create a `.dockerignore` file

Build container image

```shell
docker build . -t <your username>/node-web-app
# or
podman build . -t ginigangadharan/node-web-app
```

check images

```shell
$ podman images
REPOSITORY                              TAG         IMAGE ID      CREATED        SIZE
localhost/ginigangadharan/node-web-app  latest      483904087d42  5 minutes ago  934 MB
```

run the containers

```shell
$ podman run -p 49160:8080 -d ginigangadharan/node-web-app

$ curl -i localhost:49160
```

Ref:
 https://awstip.com/lets-deploy-our-first-nodejs-application-on-kubernetes-874870270b5b