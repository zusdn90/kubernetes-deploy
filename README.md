# kubernetes-deploy
django project를 kubernetes로 배포하기

### [kubectl로 배포하기]
##### kubectl은 kubernetes와 통신할 수 있도록 지원해주는 CLI



> kubectl apply -f deployment.yml (kubernetes에 해당 yml 파일을 적용 -> 배포 명령어)

> kubectl get pods (pods 정보를 가져온다.)


</br></br>

##### 외부 서비스와 연동하려면 kubectl expose명령어로 deploy 해주면서 동시에 type설정이 필요!
- type은 NodePort와 LoadBalancer가 있는데 LoadBalancer로 배포하는것이 일반적이다.
- LoadBalancer로 배포하면 virtual ip(대표ip)가 생성되는데 해당 ip로 외부에서 접근할 수 있다.

> kubectl expose deploy kubernetes-django-deployment --type=NodePort

> kubectl get service

> kubectl get pod -o wide (pod ip 확인 명령어)

> kubectl create deployment deploy-nginx --image=nginx(deployment 배포 명령어)
