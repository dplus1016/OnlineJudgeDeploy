
### Linux(18.04 LTS)에 설치하는 방법

1. 환경 구성

    `$ sudo apt-get update && sudo apt-get install -y vim python-pip curl git`
    
    `$ pip install docker-compose` -- 만약, Command 'pip' not found 에러가 나온다면, `$ sudo apt install python-pip` 를 실행한 후에 다시 
    
    
     
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

3. 온라인저지 사이트 설치

    (1) 아래의 명령문을 순서대로 실행

    `$ git clone -b 2.0 https://github.com/QingdaoU/OnlineJudgeDeploy.git && cd OnlineJudgeDeploy`
    
    `$ sudo apt install docker-compose`

    `$ sudo -E docker-compose up -d`
    
    사이트 설치 완료 --> 웹 브라우저로 접속... 주소는 127.0.0.1 혹은 0.0.0.0
    
---

4. 사이트 확인

    (1) 관리자 초기 ID: `root` / PW: `rootroot`
    
    (2) 관리자 계정으로 접속 한 후에 비밀번호 다시 설정
    
    (3) 사이트 이용에 관한 설명(반드시 참고) : http://docs.onlinejudge.me/

---

5. 사이트 한글화 작업(Frontend 수정)

    https://github.com/dplus1016/OnlineJudgeFE
