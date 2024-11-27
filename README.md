## PublicCloud 평가


## 3. 서버 프로그램을 DOCKER HUB, ECR에 배포해서 ECS서비스로 구동이 가능하도록 GIT ACTION 구현
**로드밸런서는 반드시 연결**
1. DockerHub에 배포하기 위한 Dockerfile생성
2. Git Action을 구현하기 위한 yaml파일 생성
   + ./github/workflows/gitaction.yaml
3. 로드밸런서를 연결하기 위해서 Task를 2개로 지정(최소 2개)


![image](https://github.com/user-attachments/assets/4dfa00fd-418e-4361-b788-de6af411e2bd)


![image](https://github.com/user-attachments/assets/57026ec8-55d2-45a8-88af-c0122525a6bd)


![image](https://github.com/user-attachments/assets/dec88fb1-3adf-43b4-9e31-f7f03ac83dbd)


배포에 성공했으므로 각 Task의 Public IP와 Service의 DNS 이름으로 접속할 수 있다 


![image](https://github.com/user-attachments/assets/fb240002-1619-4f5e-9f9d-c3f12cc9dc69)


+ Task 1


![image](https://github.com/user-attachments/assets/256d2bf2-7962-4d73-850b-ba6d02da4e23)


+ Task 2


![image](https://github.com/user-attachments/assets/0be3ab26-a4e0-49ff-9186-9fcc2a3b2ef3)


+ Service DNS 이름
  + http://userinfoloadbalnacer-135869067.ap-northeast-2.elb.amazonaws.com/
