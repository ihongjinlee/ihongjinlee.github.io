---
title: GitHub Blog 한 번에 끝내기 (3) Jekyll Chirpy 테마 적용
date: 2023-10-17 21:00:00 +09:00
categories: [github]
tags: [github, blog, windows11, jekyll, chirpy, theme]
---

## 1. Chirpy 테마 다운로드

- http://jekyllthemes.org/themes/jekyll-theme-chirpy/
- Download 버튼 클릭

![Chirpy 테마](/assets/posts/2023-10-17/스크린샷 2023-10-14 083512.png){: width="972" height="589" }
_Chirpy 테마_

## 2. jekyll-theme-chirpy-master.zip

- jekyll-theme-chirpy-master 파일 압축 풀기
- 파일 탐색기에서 jekyll-theme-chirpy-master 폴더로 들어가 모두 선택 후 복사(Ctrl+C)
- 테마 적용할 폴더에 모두 덮어쓰기(Ctrl+V)

![Chirpy 테마](/assets/posts/2023-10-17/스크린샷 2023-10-14 083658.png)
_덮어쓰기_

## 3. 테마 설치

### 파일 및 폴더 삭제

|:----------------------|
| Gemfile.lock 파일 삭제 |
| docs 폴더 삭제 |

### GitHub Action (.github/workflow)

|:-------------|:-------------:|
| pages-deploy.yml.hook | 이 파일을 제외한 폴더 안의 모든 파일 삭제 |
| pages-deploy.yml.hook -> pages-deploy.yml | 파일명 변경 |

### 번들 인스톨

```console
$ bundle install
```

### GitHub Actions를 사용하여 배포하기 위한 처리

- Gemfile.lock을 저장소에 커밋했고 로컬 컴퓨터에서 Linux를 실행하지 않는 경우 사이트의 루트로 이동하여 잠금 파일의 플랫폼 목록을 업데이트.

```console
$ bundle lock --add-platform x86_64-linux
```

### node 패키지 설치와 빌드

```console
$ npm install
$ npm run build
```

### 빌드 에러 발생

- NODE_ENV은(는) 내부 또는 외부 명령, 실행할 수 있는 프로그램, 또는 배치 파일이 아닙니다.

```console
$ npm install -g win-node-env
```

### 다시 빌드

```console
$ npm run build
```

### `.gitignore`

```shell
...
# Misc
# assets/js/dist 주석처리
```

## 4. Github 빌드와 배포 설정

- Settings -> Pages -> Build and deployment -> source -> GitHub Actions 선택
  ![Chirpy 테마](/assets/posts/2023-10-17/스크린샷 2023-10-14 084603.png)
  _빌드와 배포 설정_

## 5. 배포

```console
$ git add .
$ git commit -m "Jekyll Chript 테마 적용"
$ git push
```

![Chirpy 테마](/assets/posts/2023-10-17/스크린샷 2023-10-14 090455.png)
_배포 완료_

## 6. 출처

- [달새님의 github pages 블로그 만들기 테마 적용하기(Chirpy)](https://ree31206.tistory.com/entry/github-pages-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0-%ED%85%8C%EB%A7%88-%EC%A0%81%EC%9A%A9%ED%95%98%EA%B8%B0Chirpy/)
