## Exercise 1.4. - Missing dependencies

### Command used to start the process:
```bash
docker run -d -it --name website ubuntu sh -c 'while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'
```

### Commands used to fix missing dependencies:
```bash
docker exec -it website bash
apt-get update
apt-get install -y curl
```

### Output for 'helsinki.fi':
```html
<html>
    <head><title>301 Moved Permanently</title></head>
    <body>
        <center><h1>301 Moved Permanently</h1></center>
        <hr><center>nginx/1.24.0</center>
    </body>
</html>