# docker : 기본 명령어

## component
 
- image : 실행 가능한 애플리케이션 또는 환경을 포함하는 템플릿
- container : 이미지로부터 생성된 인스턴스
- Dockerfile : 이미지 생성을 위한 설정 파일
- registry : 이미지를 관리하는 공간

## command

- docker pull : 이미지 다운로드
- docker run : 컨테이너 생성 및 실행
- docker ps : 실행 중인 컨테이너 확인
- docker ps -a : 모든 컨테이너 확인
- docker exec : 실행 중인 컨테이너에 명령 실행
- docker stop : 컨테이너 중지
- docker rm : 컨테이너 삭제
- docker rmi : 이미지 삭제
- docker logs : 컨테이너 로그 확인
- docker build : Dockerfile 기반 이미지 빌드
- docker volume : 볼륨 관리
- docker network : 네트워크 관리