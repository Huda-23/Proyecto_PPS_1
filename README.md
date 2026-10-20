docker run --name web-pps -d -p 127.0.0.1:8080:8000 pps_1:latest
docker ps
curl -s -o /dev/null -w '%{http_code}\n' http://localhost:8080


otra forma (me ha funcionado):

```bash
sudo docker rm -f web-pps
sudo docker build -t pps_1:latest .
sudo docker run -d -p 8080:80 --name web-pps pps_1:latest
```
