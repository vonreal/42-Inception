# 42-Inception
Docker-compose를 사용하여 특정한 규칙에 따라 서로 다른 서비스로 구성된 소규모 인프라를 설정하는 프로젝트입니다.

### 현재 상태
진행중
✅ ~ 2021.08.21
<ul>
  <li> DB 컨테이너, WordPress + Php-fpm 컨테이너, NGINX 컨테이너 생성 완료</li>
  <li> 443 포트로 웹 서버 접근 가능</li>
  <li> WordPress volume 설정</li>
  <li> 웹 서버(Nginx)에서 애플리케이션 서버(WordPress + Php-fpm) 9000포트로 연결 완료</li>
  <li> 현재 수준까지 Docker-compose.yml 작성 완료</li>
</ul>
