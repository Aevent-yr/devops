- docker ps
```
 NAME                IMAGE            COMMAND                  SERVICE   CREATED         STATUS                   PORTS
guestbook-nginx-1   nginx:alpine     "/docker-entrypoint.…"   nginx     2 minutes ago   Up 2 minutes             0.0.0.0:8080->80/tcp, [::]:8080->80/tcp
guestbook-redis-1   redis:7-alpine   "docker-entrypoint.s…"   redis     2 minutes ago   Up 2 minutes (healthy)   6379/tcp
guestbook-web-1     guestbook-web    "python app.py"          web       2 minutes ago   Up 2 minutes (healthy)   5000/tcp
guestbook-web-2     guestbook-web    "python app.py"          web       2 minutes ago   Up 2 minutes (healthy)   5000/tcp
guestbook-web-3     guestbook-web    "python app.py"          web       2 minutes ago   Up 2 minutes (healthy)   5000/tcp
```
- 호스트명은 scale 3 기준, 7fe27ee6b55f, eedf9bdad2fa, c91f17bb96cd 로 바뀜...
- down 후 up은 볼륨의 정보가 그대로 남아있고, down -v 후 up은 볼륨의 정보가 모두 삭제되어 있다. 방명록으로 치면 원래는 down 후 up의 경우, 방명록이 남아있지만, down -v한 경우 방명록이 다시 up을 하면 사라진다
- .env에 민감한 정보(password)가 포함되어 있기에, 공개되어선 안되기 때문에 .env는 .gitignore에 추가되어야 한다
