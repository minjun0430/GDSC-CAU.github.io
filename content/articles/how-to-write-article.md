---

title: "[공지] 아티클 작성 방법"
description: 아티클 작성 시 지켜야 할 규칙들에 대해 안내 드립니다.
slug: how-to-write-article
img: writing.png
category: General
author: Peniel Cho
featured: Featured

---

>  아티클 작성 방법과 작성 시 지켜야할 규칙에 대해 안내 드립니다.


## 1. 확장명은 md이며, ~/content/articles 디렉토리 내에 위치합니다.

- 아티클의 확장명은 md(마크다운)입니다. 

- 파일명은 아티클 slug 속성값과 동일해야 합니다. 관련 내용은 3번에서 설명 드립니다. 

- 파일은 ~/content/articles 디렉토리 내에 위치해야 합니다. 아래는 GDSC-CAU.github.io 레포지토리의 구조입니다. 이 중 content 폴더로 이동 후, 그 안의 articles 폴더 안에 들어가 md 파일을 생성하시면 됩니다.

  ![레포지토리 구조](/how-to-write-article/01.png)

## 2. YAML Front Matter 작성은 필수입니다.

YAML Front Matter란 마크다운 등의 파일 내에 환경설정 및 정보값 표기를 위한 YAML 구역입니다. 아래는 YAML Front Matter 작성하실 때의 규칙입니다.

### 파일 최상위에 위치해야 합니다.

아티클 md 파일 최상위에 위치하지 않을 경우 YAML 구역으로 인식되지 않습니다.

### 세개의 대시(-)로 감싸져야 합니다.

구역 자체는 세개의 대시로 위 아래를 감싸주어야 합니다. 아래 예시를 참고해주세요.

### 각 속성 및 값에 있어 오타가 없어야 합니다.

모든 아티클마다 기본적으로 5가지의 속성을 작성해주셔야 합니다.

- **title**: 말 그대로 아티클의 제목입니다. 내용을 잘 드러낼 수 있도록 적어주세요.
- **description**: 아티클에 대한 짧은 설명을 적어주시면 됩니다.
- **slug**: url의 일부로 사용될 중요한 부분입니다. 아래 원칙에 지켜 작성해주세요.
  - 영문 소문자로 작성되어야 합니다.
  - 띄어쓰기는 불가능합니다. 띄어쓰기가 필요한 경우 대시(-)로 대체해주세요.
  - md 파일명과 반드시 동일해야 합니다. 이는 3번에서 추가적으로 설명드리겠습니다.
- **category**: 카테고리는 총 6가지가 있습니다. 해당 카테고리 중에서 아티클에 가장 적절한 카테고리를 골라서 작성해주시면 됩니다. 대문자, 대시(-) 모두 확실히 지켜 작성해주세요. 6가지 카테고리 종류는 아래와 같습니다.
  - Front-End: 웹 개발에 관련된 글들입니다.
  - Back-End: 서버, 데이터베이스에 관련된 글들입니다.
  - Data-Science: DS부터 ML, DL까지 데이터에 관련된 글들입니다.
  - Application: 모바일 어플리케이션 개발에 관한 글들입니다.
  - DevOps: 개발부터 배포까지의 프로세스 개선을 위한 글들입니다.
  - General: 카테고리화하기 애매한 개발 관련 글들입니다. 행사 및 활동 글 역시 포함됩니다.
- **author**: 본인의 이름을 작성해주시면 됩니다. 다만 프로필의 name 속성에 대응하는 값과 완전히 동일해야 합니다.

Featured 아티클로 선정될 경우 두가지의 속성이 더 필요합니다.

- **featured**: 본 속성에 Featured라는 값을 부여하면 사이트 메인 페이지의 Featured 아티클에 포함됩니다. 다만 Featured 아티클의 경우, 리드 및 코어멤버가 따로 선정하여 직접 해당 파일의 featured 속성을 수정할 예정으로 직접 작성하실 필요는 없습니다.
- **img**: Featured 아티클로 선정된 글의 경우 썸네일이 필요합니다. 이 경우 따로 이미지를 요청드릴 수도, 리드 및 코어멤버가 직접 적절한 이미지를 찾아 썸네일로 지정할 수도 있습니다.

### 예시

```yaml
---
title: 프로젝트에 Tailwind CSS 적용하기
description: 프로젝트에 Tailwind CSS를 적용하는 방법을 Nuxt 프레임워크를 중심으로 알아봐요.
slug: tailwind-on-nuxt
category: Front-End
author: Peniel Cho
---
```

## 3. md 파일명은 YAML Front Matter에서 작성한 slug와 동일해야 합니다.

즉 slug가 tailwind-on-nuxt였다면 마크다운 파일의 이름 역시 tailwind-on-nuxt.md여야 합니다. 오타 등으로 인해 slug와 파일명이 불일치할 경우 사이트 빌드 자체에 에러가 발생할 수 있습니다. 꼭 확인 부탁드립니다. 또한 앞서 말씀드렸듯 스페이스는 사용 불가하며, 소문자로 작성해주셔야 합니다.

## 4. 기본적인 Markdown 문법들을 지원합니다.

#을 통해 헤딩을 만들거나, 백틱(```)으로 감싸 코드블럭을 만들거나, >를 통해 인용문을 만드는 등 기본적인 마크다운 문법들을 지원합니다. 혹시 마크다운 사용법을 모르시는 분들이 있으시다면 [관련 블로그 포스팅](https://heropy.blog/2017/09/30/markdown/)을 참고하시는 것을 추천 드립니다.

### Heading은 H2부터 사용하시고, H5, H6는 사용하지 않으시길 추천 드립니다.

H1 사용시 제목보다 폰트 크기가 커지게 됩니다. 혹시 해당 크기의 글자가 필요할지 몰라 따로 config 수정 없이 두었으나, 일반적으로 H1을 사용하실 경우엔 H2부터 사용해주시면 됩니다. 또한  md styling 모듈로 사용 중인 Tailwind Typography에서 아직 H5, H6를 공식지원하지 않습니다. 사용을 추천드리지 않습니다.

### LaTeX는 지원하지 않습니다.

먼저 데이터 공부하시는 분들께 죄송합니다... 모듈, 패키지 설치할 때마다 버그가 생기네요. 최대한 빠르게 지원가능 하도록 힘써 보겠습니다. 그래도 수식 자체를 LaTeX로 써주시는 건 좋으리라 생각합니다. 통계, DS 공부하다 보면 raw LaTeX식도 자연스레 읽을 수 있어야 하니까요... 하하.

## 5. 이미지 저장 경로 및 삽입 경로가 특이합니다.

일반적으로 상대 경로를 통해 이미지 파일을 불러올 경우 ~/를 통해 최상위 폴더에서 파일 루트를 작성하거나 현재 디렉토리부터 시작해 파일 루트를 작성합니다. 그러나 Nuxt의 경우 md 파일에서 이미지를 불러오는 방식이 조금 특이합니다. static 폴더에서 기본 루트가 시작되기 때문입니다.

![static 폴더 내 이미지 삽입](/how-to-write-article/02.png)

따라서 md 파일 내에 이미지가 필요한 경우 위 이미지와 같이 ~/static 디렉토리에 slug와 동일한 이름의 폴더를 만들어 필요한 이미지들을 넣으신 후, 해당 폴더명부터 시작하는 상대경로로 이미지를 불러오시면 됩니다. 마크다운 문법에 따른 예시는 아래와 같습니다.

```markdown
![Tailwind Breakpoint Prefix 이미지](/why-tailwind-css/05.png)
```