## Exercise 1.5 - Sizes of images

### Commands for pulling images
```bash
docker pull devopsdockeruh/simple-web-service:ubuntu
docker pull devopsdockeruh/simple-web-service:alpina
```

### Results:

**Ubuntu**:

```bash
ubuntu: Pulling from devopsdockeruh/simple-web-service
Digest: sha256:d44e1dce398732e18c7c2bad9416a072f719af33498302b02929d4c112e88d2a
Status: Image is up to date for devopsdockeruh/simple-web-service:ubuntu
docker.io/devopsdockeruh/simple-web-service:ubuntu
```

**Alpine**:

```bash
alpine: Pulling from devopsdockeruh/simple-web-service
ba3557a56b15: Pull complete 
1dace236434b: Pull complete 
4f4fb700ef54: Pull complete 
Digest: sha256:dd4d367476f86b7d7579d3379fe446ae5dfce25480903fb0966fc2e5257e0543
Status: Downloaded newer image for devopsdockeruh/simple-web-service:alpine
docker.io/devopsdockeruh/simple-web-service:alpine
```

**Sizes**:
```bash
REPOSITORY                                        TAG       IMAGE ID       CREATED         SIZE
devopsdockeruh/simple-web-service                 ubuntu    4e3362e907d5   3 years ago     83MB
devopsdockeruh/simple-web-service                 alpine    fd312adc88e0   3 years ago     15.7MB
```
Alpine is much smaller then Ubuntu (15.7MB against 83MB).

### Run the alpine container

```bash
docker run -d --name alpine-container devopsdockeruh/simple-web-service:alpine
WARNING: The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested
ec10070bf2331e690dfb857a6bad6fc046299d409f9c4bd09e1b789415c94bd2
```

### Passing inside the container and check the secret message

```bash
docker exec -it alpine-container sh
/usr/src/app # tail -f ./text.log
2025-02-12 14:44:19 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
```
The secret message is the same as in the Ubuntu container.