---
title: GitHub Blog 한 번에 끝내기 (1) 프로그램 설치
date: 2023-10-14 09:00:00 +09:00
categories: [github]
tags: [github, blog, windows11, ruby, jekyll, bundler]
---

## 1. 시작

|:--------|:-----------------------------------------------:|
| Ruby | 동적 스크립트 언어로서 객체지향 프로그래밍 언어 |
| Jekyll | 정적 웹사이트 생성기(Static Site Generator, SSG) |
| Bundler | Ruby 프로젝트에서 종속성 관리를 도와주는 도구 |

## 2. Ruby

### Ruby 설치

|:--------|:-----------------------------------------------:|
| 다운로드 경로 | <https://rubyinstaller.org/downloads/> |
| 설치 버전 | Ruby+Devkit 3.2.2-1 (x86) |
| 설치 파일 | `rubyinstaller-devkit-3.2.2-1-x86.exe` |

![Ruby 설치1](/assets/posts/2023-10-14/스크린샷 2023-10-14 080808.png){: width="972" height="589" }
_https://rubyinstaller.org/downloads/_

![Ruby 설치2](/assets/posts/2023-10-14/스크린샷 2023-10-14 080941.png){: width="972" height="589" .w-75 .center }
_Setup - Ruby 3.2.2-1-x86_

![Ruby설치3](/assets/posts/2023-10-14/스크린샷 2023-10-14 080947.png){: width="972" height="589" .w-75 .center }
_Setup - Ruby 3.2.2-1-x86_

![Ruby설치4](/assets/posts/2023-10-14/스크린샷 2023-10-14 081005.png){: width="972" height="589" .w-75 .center }
_Setup - Ruby 3.2.2-1-x86_

![Ruby설치5](/assets/posts/2023-10-14/스크린샷 2023-10-14 081151.png){: width="972" height="589" .w-75 .center }
_Setup - Ruby 3.2.2-1-x86_

![Ruby설치6](/assets/posts/2023-10-14/스크린샷 2023-10-14 081405.png){: width="972" height="589" .w-75 .center }
_Setup - Ruby 3.2.2-1-x86_

![Ruby설치7](/assets/posts/2023-10-14/스크린샷 2023-10-14 081441.png){: width="972" height="589" }
_Ruby Installer2 for Windows_

![Ruby설치8](/assets/posts/2023-10-14/스크린샷 2023-10-14 081600.png){: width="972" height="589" }
_Ruby Installer2 for Windows_

### Ruby 버전 확인

```shell
$ ruby -v
ruby 3.2.2 (2023-03-30 revision e51014f9c0) [i386-mingw32]
```

## 3. Jekyll

### Jekyll 설치

```shell
$ gem install jekyll
```

### Jekyll 버전 확인

```shell
$ jekyll -v
jekyll 4.3.2
```

## 4. Bundler

### Bundler 설치

```shell
$ gem install bundler
```

### Bundler 버전 확인

```shell
$ bundler -v
Bundler version 2.4.20
```

## 5. 출처

- [PRO님의 Github 블로그 만들기 (1)](<https://devpro.kr/posts/Github-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0-(1)/>)
