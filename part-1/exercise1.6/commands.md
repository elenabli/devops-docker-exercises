## Exercise 1.6 - Hello Docker Hub

### Run the container

```bash
docker run -it devopsdockeruh/pull_exercise
Unable to find image 'devopsdockeruh/pull_exercise:latest' locally
latest: Pulling from devopsdockeruh/pull_exercise
8e402f1a9c57: Pull complete 
5e2195587d10: Pull complete 
6f595b2fc66d: Pull complete 
165f32bf4e94: Pull complete 
67c4f504c224: Pull complete 
Digest: sha256:7c0635934049afb9ca0481fb6a58b16100f990a0d62c8665b9cfb5c9ada8a99f
Status: Downloaded newer image for devopsdockeruh/pull_exercise:latest
WARNING: The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested
```

### The command waits for the password

Password is 'basics', which is on the Docker Hub, in the Readme file of the devopsdockeruh/pull_exercise image.

```bash
Give me the password: basics
You found the correct password. Secret message is:
"This is the secret message"
```

