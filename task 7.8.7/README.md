# Задание 7.8.7
## Docker-образ приложения, которое будет при запуске контейнера скачивать favicon заданного приложению сайта

* Создал Dockerfile

## Улучшить этот Docker-образ согласно изученным лучшим практикам

* Использование имени при создании образа:
```
docker image rm favicon; docker build . -t favicon
```
* Задание тега исходного образа (FROM) в Dockerfile,
* Использование ключа `--rm` при старте, чтобы не плодить остановленные контейнеры при каждом запуске:
```
$ docker run --rm --mount type=bind,source=/home/al/Projects/devops/b7_docker/task\ 7.8.7/out,destination=/out favicon dzen.ru
--2024-11-15 18:29:24--  https://dzen.ru/favicon.ico
Resolving dzen.ru (dzen.ru)... 62.217.160.2
Connecting to dzen.ru (dzen.ru)|62.217.160.2|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 15406 (15K) [image/x-icon]
Saving to: 'favicon.ico'

     0K .......... .....                                      100% 3.90M=0.004s

2024-11-15 18:29:24 (3.90 MB/s) - 'favicon.ico' saved [15406/15406]
```