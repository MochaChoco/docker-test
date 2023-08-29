# docker-test
Next.js 프로젝트에 docker를 적용한 예제입니다.

# 명령어
1. 빌드
  - 개발환경: docker build -t {{ 빌드할 Image 파일명 }} -f ./Dockerfile . --build-arg ENV_MODE=development
  - 운영환경: docker build -t {{ 빌드할 Image 파일명 }} -f ./Dockerfile . --build-arg ENV_MODE=production
  - 예시) docker build -t docker-test -f ./Dockerfile . --build-arg ARG_MODE=development
2. 실행
  - docker run -it --rm -p 3000:3000 {{ 빌드한 Image 파일명 }}
  - 예시) docker run -it --rm -p 3000:3000 docker-test
