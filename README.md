# kubernetes-deploy
django project를 kubernetes로 배포하기

[kubectl로 배포하기]
- kubectl은 kubernetes와 통신할 수 있도록 지원해주는 CLI


kubectl apply -f deployment.yml (kubernetes에 해당 yml 파일을 적용)

kubectl get pods (pods 정보를 가져온다.)

외부 서비스와 연동하려면 kubectl expose명령어로 deploy 해주면서 동시에 type설정이 필요!

kubectl expose deploy kubernetes-django-deployment --type=NodePort

kubectl get service
