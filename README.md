# ☕ STARBUCKS

## 문자 인코딩(Character Encoding) 설정

문자가 인코딩되는 방식을 설정합니다.

```html
<meta charset="UTF-8"/>
```

- `UTF-8`: 초성, 중성, 종성으로 구분하여 문자를 작성(권장)
- `EUC-KR`: 하나의 완성된 글자를 인식

## 뷰포트(Viewport) 렌더링 방식 설정

웹페이지가 화면(Viewport)에 표현되는 방식을 설정합니다.<br>
모바일 환경에서 적용됩니다.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

- `width=device-width`: 화면의 가로 너비를 각 디바이스(Device)의 가로 너비와 동일하게 적용
- `initial-scale=1.0`: 화면의 초기 화면 배율(확대 정도)을 설정
- `user-scalable=no`: 사용자가 디바이스 화면을 확대(`yes`)/축소(`no`)할 수 있는지 설정
- `maximum-scale=1`: 사용자가 화면을 확대할 수 있는 최댓값
- `minimum-scale=1`: 사용자가 화면을 축소할 수 있는 최솟값
## 오픈 그래프(The Open Graph protocol)

웹페이지가 소셜 미디어(페이스북 등)로 공유될 때 우선적으로 활용되는 정보를 지정합니다.

Slack -

![Slack Open Graph example](https://raw.githubusercontent.com/ParkYoungWoong/starbucks-vanilla-app/master/_assets/slack_message_og_example.jpg)

KakaoTalk -

![KakaoTalk Open Graph example](https://raw.githubusercontent.com/ParkYoungWoong/starbucks-vanilla-app/master/_assets/kakao_og_example.jpg)

[더 많은 오픈 그래프 속성 보기](https://ogp.me/)

```html
<meta property="og:type" content="website" />
<meta property="og:site_name" content="Starbucks" />
<meta property="og:title" content="Starbucks Coffee Korea" />
<meta property="og:description" content="스타벅스는 세계에서 가장 큰 다국적 커피 전문점으로, 64개국에서 총 23,187개의 매점을 운영하고 있습니다." />
<meta property="og:image" content="./images/starbucks_seo.jpg" />
<meta property="og:url" content="https://starbucks.co.kr" />
```

- `og:type`: 페이지의 유형(E.g, `website`, `video.movie`)
- `og:site_name`: 속한 사이트의 이름
- `og:title`: 페이지의 이름(제목)
- `og:description`: 페이지의 간단한 설명
- `og:image`: 페이지의 대표 이미지 주소(URL)
- `og:url`: 페이지 주소(URL)

## 트위터 카드(Twitter Cards)

웹페이지가 소셜 미디어(트위터)로 공유될 때 우선적으로 활용되는 정보를 지정합니다.

[더 많은 트위터 카드 보기](https://developer.twitter.com/en/docs/twitter-for-websites/cards/guides/getting-started)

```html
<meta property="twitter:card" content="summary" />
<meta property="twitter:site" content="Starbucks" />
<meta property="twitter:title" content="Starbucks Coffee Korea" />
<meta property="twitter:description" content="스타벅스는 세계에서 가장 큰 다국적 커피 전문점으로, 64개국에서 총 23,187개의 매점을 운영하고 있습니다." />
<meta property="twitter:image" content="./images/starbucks_seo.jpg" />
<meta property="twitter:url" content="https://starbucks.co.kr" />
```

- `twitter:card`: 페이지(카드)의 유형(E.g. `summary`, `player`)
- `twitter:site`: 속한 사이트의 이름
- `twitter:title`: 페이지의 이름(제목)
- `twitter:description`: 페이지의 간단한 설명
- `twitter:image`: 페이지의 대표 이미지 주소(URL)
- `twitter:url`: 페이지 주소(URL)

## Favicon(파비콘, favorites icon)

웹페이지를 나타내는 아이콘, 웹페이지의 로고를 설정합니다.<br>
대부분의 경우 루트 경로에 `favicon.ico` 파일을 위치하면 자동으로 로딩하기 때문에 `<link />` 를 작성할 필요가 없습니다.
`favicon.png` 파일을 사용하려면 다음과 같이 `<link />`를 작성하세요.

> 파비콘 이미지는 루트 경로에 있어야 합니다!

```html
<!--<link rel="shortcut icon" href="favicon.ico" />-->
<link rel="icon" href="./favicon.png" />
```

- `favicon.ico` 64 x 64 (px) 또는 32 x 32 또는 16 x 16
- `favicon.png` 500 x 500 (px)

<img src="https://raw.githubusercontent.com/ParkYoungWoong/starbucks-vanilla-app/master/favicon.png" alt="Starbucks" width="16" />
<img src="https://raw.githubusercontent.com/ParkYoungWoong/starbucks-vanilla-app/master/favicon.png" alt="Starbucks" width="200" />

### .ico 파일 제작

이미지를 업로드하면 손쉽게 `.ico` 파일을 제작할 수 있습니다.

[iconifier.net](https://iconifier.net/)

## CDN Reset.css

각 브라우저의 기본 스타일을 초기화합니다.
이외에 reset.css파일을 css 폴더에 직접 추가하는 방법이 있습니다.

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reset-css@5.0.1/reset.min.css" />
```

## Google Fonts

페이지에서 사용할 '나눔고딕' 폰트를 지정합니다.

> 폰트 라이선스를 꼭 확인해야 합니다!

[Google Fonts](https://fonts.google.com/)에서 고른 폰트 파일을 가져옵니다.

```html
<link rel="preconnect" href="https://fonts.gstatic.com" />
<link href="https://fonts.googleapis.com/css2?family=Nanum+Gothic:wght@400;700&display=swap" rel="stylesheet" />
```

페이지에 폰트를 적용(CSS 상속)합니다.

```css
body {
    font-family: 'Nanum Gothic', sans-serif;
}
```

## Google Material Icons

[구글에서 제공하는 머터리얼 아이콘](https://material.io/resources/icons/?style=baseline)을 무료로 사용할 수 있습니다.

[Getting started for web](https://material.io/develop/web/getting-started)

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons" />
```

다음과 같이 사용할 수 있습니다.

```html
<div class="material-icons">upload</div>
```

## Swiper

[Swiper](https://swiperjs.com/)는 하드웨어 가속 전환과 여러 기본 동작을 갖춘 현대적인 슬라이드 라이브러리입니다.

[Getting Started With Swiper](https://swiperjs.com/get-started)
> Swiper 6버전을 사용합니다.<br>
> 7/8버전의 사용법이 다르기 때문에 6버전을 유지합니다.

```html
<!-- in HEAD -->
<link rel="stylesheet" href="https://unpkg.com/swiper@6.8.4/swiper-bundle.min.css" />
<script src="https://unpkg.com/swiper@6.8.4/swiper-bundle.min.js"></script>

<!-- in BODY -->
<div class="swiper-container">
  <div class="swiper-wrapper">
    <div class="swiper-slide">1</div>
    <div class="swiper-slide">2</div>
    <div class="swiper-slide">3</div>
  </div>
</div>
```

[Swiper API](https://swiperjs.com/swiper-api)(옵션)을 확인하세요!

```js
new Swiper(요소, 옵션);
```

```js
new Swiper('.swiper-container', {
  direction: 'vertical', // 수직 슬라이드
  autoplay: true, // 자동 재생 여부
  loop: true // 반복 재생 여부
});
```

---





---
## 구성
### Header
#### logo
```paintext
상대적 배치를 이용해, 좌측 수직 중앙 배치
```
```css
header .logo {
  height: 75px;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  margin: auto;
}
```
#### sub-menu
```paintext
flex 정렬을  통해 li를 수평으로 정렬
```
```css
header .sub-menu {
  position: absolute;
  top: 10px;
  right: 0;
  display: flex;
}
header .sub-menu ul.menu {
  font-family: Arial, sans-serif;
  display: flex;
}
```
```paintext

// 검색창 요소 내부 실제 input 요소에 포커스 될때
// 검색창 요소 내부 실제 input 요소에서 포커스가 해제(블러)될때

각각 add()와 remove()를 통해 해당 .focused 클래스 선택자 선택 및 해제!
```
```js
// 검색창 요소를 클릭하면 실행.
searchEl.addEventListener('click', function () {
  searchInputEl.focus()
})
// 검색창 요소 내부 실제 input 요소에 포커스되면 실행.
searchInputEl.addEventListener('focus', function () {
  searchEl.classList.add('focused')
  searchInputEl.setAttribute('placeholder', '통합검색')
})
// 검색창 요소 내부 실제 input 요소에서 포커스가 해제(블러)되면 실행.
searchInputEl.addEventListener('blur', function () {
  searchEl.classList.remove('focused')
  searchInputEl.setAttribute('placeholder', '')
})

```

#### main menu
```paintext
drop-down menu로 hover로 구현
sub-menu와 동일하게 flex 정렬을  통해 li를 수평으로 정렬
```
```css
header .main-menu {
  position: absolute;
  bottom: 0;
  right: 0;
  z-index: 1;
  display: flex;
}

header .main-menu .item .item__contents .contents__menu > ul {
  padding: 20px 0;
  display: flex;
}
```
### section - notice
#### notice-line
```paintext
swiper-wrapper안에 swiper-slide들로 구성
```
```js
// swiperjs docs
const swiper = new Swiper('.swiper', {
  // Optional parameters
  direction: 'vertical',
  loop: true,

  // If we need pagination
  pagination: {
    el: '.swiper-pagination',
  },

  // Navigation arrows
  navigation: {
    nextEl: '.swiper-button-next',
    prevEl: '.swiper-button-prev',
  },

  // And if we need scrollbar
  scrollbar: {
    el: '.swiper-scrollbar',
  },
});
```

```html
<!-- in BODY -->
<div class="swiper-container">
  <div class="swiper-wrapper">
    <div class="swiper-slide">1</div>
    <div class="swiper-slide">2</div>
    <div class="swiper-slide">3</div>
  </div>
</div>
```
```css
  /*정렬 수행*/
.notice .notice-line .inner__left .swiper-slide {
  height: 62px;
  display: flex;
  align-items: center;
}
.notice .notice-line .inner__left .swiper-slide a {
  color: #fff;
}
.notice .notice-line .inner__left .notice-line__more {
  width: 62px;
  height: 62px;
  display: flex;
  justify-content: center;
  align-items: center;
}  
```
```js
new Swiper('.swiper-container', {
  direction: 'vertical', // 수직 슬라이드
  autoplay: true, // 자동 재생 여부
  loop: true // 반복 재생 여부
});
```
#### notice-promotion
```paintext
swiper-wrapper안에 swiper-slide들로 구성

버튼 배치 및 메인 slide 외 양쪽 나머지 슬라이드 opacity: 0.5로 조절
```
```js
// swiperjs docs
const swiper = new Swiper('.swiper', {
  // Optional parameters
  direction: 'vertical',
  loop: true,

  // If we need pagination
  pagination: {
    el: '.swiper-pagination',
  },

  // Navigation arrows
  navigation: {
    nextEl: '.swiper-button-next',
    prevEl: '.swiper-button-prev',
  },

  // And if we need scrollbar
  scrollbar: {
    el: '.swiper-scrollbar',
  },
});
```

```html
<!-- in BODY -->
<div class="swiper-container">
  <div class="swiper-wrapper">
    <div class="swiper-slide">1</div>
    <div class="swiper-slide">2</div>
    <div class="swiper-slide">3</div>
  </div>
</div>
```
```css
.notice .promotion {
  /*width: auto;*/
  height: 693px;
  background-color: #f6f5ef;
  position: relative;
  overflow: hidden;
  transition: height .4s;
}
.notice .promotion .swiper-container {
  /* 819px 슬라이드 3개와 그 사이 여백 10px씩 = 2477px */
  width: calc(819px * 3 + 20px);
  height: 553px;
  position: absolute;
  top: 40px;
  left: 50%;
  margin-left: calc((819px * 3 + 20px) / -2);
}
.notice .promotion .swiper-slide {
  position: relative;
  opacity: .5;
  transition: opacity 1s;
}
.notice .promotion .swiper-slide .btn {
  /*width: 130px;*/
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  margin: auto;
}
```
```js
new Swiper('.promotion .swiper-container', {
  // direction: 'horizontal', // 수평 슬라이드
  autoplay: { // 자동 재생 여부
    delay: 5000 // 5초마다 슬라이드 바뀜
  },
  loop: true, // 반복 재생 여부
  slidesPerView: 3, // 한 번에 보여줄 슬라이드 개수
  spaceBetween: 10, // 슬라이드 사이 여백
  centeredSlides: true, // 1번 슬라이드가 가운데 보이기
  pagination: { // 페이지 번호 사용 여부
    el: '.promotion .swiper-pagination', // 페이지 번호 요소 선택자
    clickable: true // 사용자의 페이지 번호 요소 제어 가능 여부
  },
  navigation: { // 슬라이드 이전/다음 버튼 사용 여부
    prevEl: '.promotion .swiper-prev', // 이전 버튼 선택자
    nextEl: '.promotion .swiper-next' // 다음 버튼 선택자
  }
});
```
### section - awards
```paintext
// 네비게이션 옵션 추가
// css로 네비게이션 배치
```
```js
new Swiper('.awards .swiper-container', {
    // direction: 'horizontal', // 수평 슬라이드
    autoplay: true, // 자동 재생 여부
    loop: true, // 반복 재생 여부
    spaceBetween: 30, // 슬라이드 사이 여백
    slidesPerView: 5, // 한 번에 보여줄 슬라이드 개수
    // slidesPerGroup: 5, // 한 번에 슬라이드 할 개수(전체 개수로 나뉘어야 함)
    navigation: { // 슬라이드 이전/다음 버튼 사용 여부
      prevEl: '.awards .swiper-prev', // 이전 버튼 선택자
      nextEl: '.awards .swiper-next' // 다음 버튼 선택자
    }
});
```

```html
 <!--promotion과 동일-->
```
```css
.awards .swiper-prev,
.awards .swiper-next {
  width: 42px;
  height: 42px;
  outline: none;
  border: 2px solid #fff;
  border-radius: 50%;
  color: #fff;
  position: absolute;
  top: 0;
  bottom: 0;
  margin: auto;
  opacity: .3;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: .4s;
}
.awards .swiper-prev {
  left: -100px;
}
.awards .swiper-next {
  right: -100px;
}
```

### footer
```paintext
// flex로 수평 정렬
// 이는 메뉴바 구성원리와도 동일

// btn-group과 menu가 핵심
```
```css
footer .menu {
  display: flex;
  justify-content: center;
}

footer .btn-group {
  margin-top: 20px;
  display: flex;
  justify-content: center;
}
```
