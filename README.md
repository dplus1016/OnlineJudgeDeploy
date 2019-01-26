
### Linux(18.04 LTS)에 설치하는 방법

1. 환경 구성
 
    `$ sudo apt-get update`
    
    `$ sudo apt-get install -y vim python-pip curl git`
---
     
2. Docker 설치

- 아래의 명령문을 순서대로 실행
    
      `$ sudo pip install docker-compose`
      
      `$ sudo apt-get update`
      
      `$ sudo curl -sSL get.docker.com | sh`
    
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
