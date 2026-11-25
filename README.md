# 🌙 심심 연구소 — 크리스마스 운명 & 2026 신년 타로

**이름만 넣으면 올해 크리스마스와 내년 운세를 알려주는 웹 운세 사이트**

🔗 **[urimll.github.io/2026-christmas-fortune](https://urimll.github.io/2026-christmas-fortune/)**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-222222?style=flat-square&logo=githubpages&logoColor=white)

> 2025.11 · 개인 프로젝트 · 프레임워크 없이 HTML/CSS/JS로 만들고 GitHub Pages로 배포했어요.

## ✨ 페이지 구성

| 페이지 | 설명 |
|---|---|
| [`index.html`](index.html) | 메인 메뉴. 두 가지 운세로 들어가는 버튼 |
| [`christmas.html`](christmas.html) | 🎄 **2025 크리스마스 운명**: 이름을 넣으면 올해 크리스마스를 어떻게 보낼지 알려줘요 |
| [`tarot.html`](tarot.html) | 🔮 **2026 신년 타로**: 카드를 뒤집어 내년 운세 키워드와 풀이를 보여줘요 |

## 🎄 크리스마스 운명
- 웃긴 결과 **192개**를 7가지 테마로 나눠 넣었어요.
  - 🏠 솔로·집순이 / ❤️ 커플·썸 / 💸 알바·현생 / 🎉 파티 / 🌍 여행·황당 / 🍰 먹부림 / 🏥 건강·기타
  - 예) "🍊 전기장판과 한몸이 되어 귤 까먹다가 손 노래짐."
- 눈 내리는 애니메이션과 "분석 중…" 로딩 연출을 넣었어요.

## 🔮 2026 신년 타로
- **100가지** 운세를 키워드와 풀이로 나눠 넣었어요. 예) *대박의 기운*, *새로운 인연*, *도약의 시기*
- 카드를 클릭하면 뒤집히면서 결과가 나와요.

## ⚙️ 이렇게 동작해요

**같은 이름이면 항상 같은 결과가 나와요.** 이름 글자의 유니코드 값을 모두 더하고, 결과 개수로 나눈 나머지로 결과를 골라요.

```js
let sum = 0;
for (let i = 0; i < name.length; i++) sum += name.charCodeAt(i);
const idx = sum % fortunes.length;   // 이름 → 고정된 운세
```

**결과는 이렇게 공유해요**
- 📸 **이미지 저장:** [html2canvas](https://html2canvas.hertzen.com/)로 결과 카드를 PNG로 캡처해요. 화면용 카드와 따로 캡처용 카드를 만들어서 깔끔하게 저장돼요.
- 🔗 **공유:** 모바일에서는 `navigator.share`로 바로 공유하고, 안 되는 환경에서는 링크를 클립보드에 복사해요.

## 🚀 배포
- GitHub Pages로 호스팅해요. (예전에는 커스텀 도메인을 연결했었어요.)

## 🗂 파일 구조

```
├── index.html       # 메인 메뉴
├── christmas.html   # 크리스마스 운명
└── tarot.html       # 2026 신년 타로
```
