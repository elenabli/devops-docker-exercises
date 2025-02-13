## Exercise 1/9 - Volumes

### Command used:
```bash 
docker run -v "$(pwd)/text.log/:/usr/src/app/text.log" --name loger devopsdockeruh/simple-web-service
```

Output is:

```bash
Starting log output
Wrote text to /usr/src/app/text.log
Wrote text to /usr/src/app/text.log
Wrote text to /usr/src/app/text.log
```

The result:

```bash
2025-02-13 12:20:21 +0000 UTC
2025-02-13 12:20:23 +0000 UTC
2025-02-13 12:20:25 +0000 UTC
2025-02-13 12:20:27 +0000 UTC
2025-02-13 12:20:29 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2025-02-13 12:20:31 +0000 UTC
```