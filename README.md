## ํ๋ก์ ํธ

### ๐ ๊ธฐ์ 

| name | version |
|:--:|:--:|
| `Java` | 1.8 |
| `Spring boot` | 2.7.8 |
| `Dockder` | 20.10.22 |
| `Gradle` | 7.4.2 |
| `JQuery` | 3.6.3 |
| `CentOS` | 8.4.2105 |

### ๋น๋ ํ๊ฒฝ
- application-local.yml : ๋ก์ปฌ ํ๊ฒฝ 
  - ๋ก์ปฌ์์ ํ๊ฒฝ์ ๋ง๊ฒ ๊ฒฝ๋ก ์์  ํ์!
- application-dev.yml : docker ๋ฐฐํฌ ํ๊ฒฝ
### ์์ค ๋น๋
1. gradle ๊ฒฝ๋ก ์ด๋
```
... shoplive-task/task
```
2. ์์ค ๋น๋
```
$ ./gradlew clean bootjar
```
###  Docker ์คํ
1. docker-compose.yml ๊ฒฝ๋ก๋ก ์ด๋
```
... shoplive-task/task
```
2. ๋น๋ํ๊ธฐ
```
$ docker-compose build
```
3. ์คํํ๊ธฐ
```
$ docker-compose up
```

[//]: # (1. Docker CentOS Image ๋ฐ๊ธฐ)

[//]: # (``` )

[//]: # ($ docker pull redis   )

[//]: # (```)

[//]: # ()
[//]: # (2. Docker CentOS ์คํ )

[//]: # (```)

[//]: # ($ docker run -i -t --name mycentos centos /bin/bash)

[//]: # (```)

[//]: # ()
[//]: # (3. Docker Redis ์คํ)

[//]: # (```)

[//]: # ($ docker run --name myredis -d -p 6379:6379 redis)

[//]: # ()
[//]: # ([redis-cli๋ก ์ ์ 1])

[//]: # ($ docker run -it --link myredis:redis --rm redis redis-cli -h redis -p 6379)

[//]: # ()
[//]: # ([redis-cli๋ก ์ ์ 2])

[//]: # ($ redis-cli -p 6379)

[//]: # (```)

[//]: # (  )
[//]: # (4. CentOS์ Java 1.8 ์ค์น)

[//]: # (```)

[//]: # (# java)

[//]: # ($ yum install java-1.8.0-openjdk)

[//]: # ()
[//]: # (# javac)

[//]: # ($ yum install java-1.8.0-openjdk-devel)

[//]: # (```)
