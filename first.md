# Docker

## 리눅스 docker 설치 
```
# curl -fsSL https://get.docker.com/ | sudo sh
# systemctl start docker 
# docker stats
# docker login
> Username:
> Password
```



## docker 실습 시작

* 옵션

|옵션|설명|
|:--|:--
|-d|Detached mode(백그라운드 모드)|
|-p|호스트와 컨테이너의 포트를 연결(포워딩)|
|-v|호스트와 컨테이너의 디렉토리를 연결(마운트)|
|-e|컨테이너 내에서 사용할 환경변수 설정|
|-name|컨테이너 이름 설정|
|-rm|프로세스 종료시 컨테이너 자동 제거|
|-it|-i, -t 터미널 입력 옵션|
|-link|컨테이너 연결|


* ubuntu:16.04 이미지 실행
```
# docker run ubuntu:16.04        // 최초 실행 시, docker hub에서 해당 이미지 pull 
# docker run --rm -it ubuntu:16.04 /bin/bash           // ubuntu
```





