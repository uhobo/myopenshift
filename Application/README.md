# Application

This is a Node.js application.

## How to build the Docker image

To build the Docker image for this application, navigate to the root directory of the project (where the `Dockerfile` is located) and run the following command:

```bash
docker build -t quay.io/gelleroni1/myopenshift:v2 .
```

This command will build a Docker image named `openshift-app` using the `Dockerfile` in the current directory.

## How to push the Docker image to quay.io

To push the built Docker image to quay.io, run the following command:

```bash
docker login -u gelleroni1 -p mypassword quay.io
docker push quay.io/gelleroni1/myopenshift:v2
```
## Cluster Openshift Console ##
https://console-openshift-console.apps.cluster-lb9xm.dynamic2.redhatworkshops.io

user1

https://user1-argocd-server-user1-argocd.apps.cluster-lb9xm.dynamic2.redhatworkshops.io

## Access to my hello world ##
http://user1-hello-world-user1-application.apps.cluster-lb9xm.dynamic2.redhatworkshops.io/

## How to run the Docker image

To run the built Docker image, use the following command:

```bash
docker run -p 8080:8080 openshift-app
```

This will start the application in a Docker container and map port 8080 of the container to port 8080 on your host machine, allowing you to access the application via `http://localhost:8080`.
