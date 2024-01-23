---
title: GitHub Blog 한 번에 끝내기 (4) 나의 favicon으로 수정
date: 2023-10-24 10:00:00 +09:00
categories: [github]
tags: [github, blog, favicon]
---

## 1.favicon 관련 파일들 생성

- 512x512 이상 정사각형 이미지 준비

![나의 favicon](/assets/img/favicons/android-chrome-512x512.png){: width="192" height="192" }
_512x512 이상 정사각형 이미지 준비_

- <https://realfavicongenerator.net/>

![나의 favicon](/assets/posts/2023-10-24/스크린샷 2023-10-24 172128.png)
_Select your Favicon image 버튼 클릭 ➡️ 이미지 파일 선택_

![나의 favicon](/assets/posts/2023-10-24/스크린샷 2023-10-24 172353.png)
_Generate your Favivons and HTML code 버튼 클릭_

![나의 favicon](/assets/posts/2023-10-24/스크린샷 2023-10-24 172422.png)
_Favicon package 버튼 클릭 ➡️ 다운로드_

## 2.파일 덮어쓰기

- favicon_package_v0.16 파일 압축 풀기
- /assets/img/favicons 폴더에 모든 파일 덮어쓰기

## 3. \_config.yml 수정

```yml
img_cdn: "https://chirpy-img.netlify.app" // 삭제
avatar: "/assets/img/favicons/android-chrome-192x192.png" // 수정
```

## 4. 완료

![나의 favicon](/assets/posts/2023-10-24/스크린샷 2023-10-24 175949.png)
_http://127.0.0.1:4000/_
