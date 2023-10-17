---
title: GitHub Blog 한 번에 끝내기 (2) jekyll 블로그 생성, 배포
date: 2023-10-15 12:30:00 +09:00
categories: [github]
tags: [github, blog, windows11, jekyll, bundler]
---

## 1. Github Repository 생성

|| _블로그 주소 형식_ | _블로그 주소_ |
||------|-----|-------|
| Repository name | {나의 깃허브계정}.github.io | ihongjinlee.github.io |

![GitHub](/assets/posts/2023-10-15/스크린샷 2023-10-14 081805.png){: width="972" height="589" }
_Github Repository 생성_

## 2. Jekyll 블로그 생성

### Git Clone

```shell
$ git clone https://github.com/ihongjinlee/ihongjinlee.github.io
$ cd ihongjinlee
```

### 기본 블로그 생성

```shell
$ jekyll new ./
```

### bundle 설치 ➡️ 업데이트 ➡️ 설치

```shell
$ bundle install
$ bundle update
$ bundle install
```

### 로컬 서버 띄우기

```shell
$ bundle exec jekyll s
```

![GitHub](/assets/posts/2023-10-15/스크린샷 2023-10-14 082718.png){: width="972" height="589" }
_로컬 서버에서 확인_

## 3. 배포

```shell
$ git add .
$ git commit -m "first commit"
$ git push
```

![GitHub](/assets/posts/2023-10-15/스크린샷 2023-10-14 083236.png){: width="972" height="589" }
_GitHub Action에서 배포 단계 확인_

![GitHub](/assets/posts/2023-10-15/스크린샷 2023-10-14 083311.png){: width="972" height="589" }
_GitHub Action에서 배포 단계 확인_

![GitHub](/assets/posts/2023-10-15/스크린샷 2023-10-14 082718.png){: width="972" height="589" }
_https://{나의 깃허브계정}.github.io 확인_

## 4. 출처

- [PRO님의 Github 블로그 만들기 (2)](<https://devpro.kr/posts/Github-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0-(2)/>)
