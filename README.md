
### Linux(18.04 LTS)에 설치하는 방법

1. 환경 구성

    `$ sudo apt-get update && sudo apt-get install -y vim python-pip curl git`
    
    `$ pip install docker-compose`
     
---
     
2. Docker 설치(설치되어 있으면 패쓰~)

    (1) 아래의 명령문을 순서대로 실행

      `$ sudo curl -sSL get.docker.com | sh`

      `$ sudo apt-get update`
    
      `$ sudo apt-get install docker-ce`
    
    
    (2) 특정 버전의 도커를 설치하려면, 사용 가능한 버전을 조회한 후에 선택하여 설치해야 함
    
      -아래의 명령문은 사용 가능한 버전을 조회하기 위함
    
      `$ apt-cache madison docker-ce`
    
      (조회 결과 예시) 
    
      `docker-ce | 5:18.09.0~3-0~ubuntu-bionic | https://download.docker.com/linux/ubuntu bionic/edge amd64 Packages`
    
      -위의 예시에서 사용가능한 버전의 이름은 `5:18.09.0~3-0~ubuntu-bionic` 이다.
    
    (3) 버전의 이름을 아래 명령문의 `<VERSION>`에 입력
    
      `$ sudo apt-get install docker-ce=<VERSION>`
    
     (입력 예시)
      `$ sudo apt-get install docker-ce=5:18.09.0~3-0~ubuntu-bionic`
    
    (4) 이제 도커 설치 완료, 정상적으로 설치가 되었는지 확인
    
      `$ sudo docker run hello-world`
    
      -만약, 아래와 같은 메시지가 나타나면 정상적으로 설치가 된 것임
    
       Hello from Docker!
    
       This message shows that your installation appears to be working correctly.
       
     
    도커 사이트 참조 ： [https://docs.docker.com/install/](https://docs.docker.com/install/)

---

3. 온라인저지 설치

    (1) 아래의 명령문을 순서대로 실행

    `$ git clone -b 2.0 https://github.com/QingdaoU/OnlineJudgeDeploy.git && cd OnlineJudgeDeploy`

    `$ sudo -E docker-compose up -d`



## 尽情享用吧

通过浏览器访问服务器的 HTTP 80 端口或者 HTTPS 443 端口，就可以开始使用了。后台管理路径为`/admin`, 安装过程中自动添加的超级管理员用户名为 `root`，密码为 `rootroot`， **请务必及时修改密码**。

不要忘记阅读文档 http://docs.onlinejudge.me/

## 定制

2.0 版将一些常用设置放到了后台管理中，您可以直接登录管理后台对系统进行配置，而无需进行代码改动。

若需要对系统进行修改或二次开发，请参照各模块的**README**，修改完成后需自行构建Docker镜像并修改`docker-compose.yml`

## 遇到了问题？

请参照: [http://docs.onlinejudge.me/](http://docs.onlinejudge.me/#/onlinejudge/faq) ，如有其他问题请入群讨论或提issue。
