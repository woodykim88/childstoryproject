# 세담이의 동화 극장

부모가 잠자리에서 한 손으로 큐레이션된 동화를 틀어주는 모바일 웹 앱.

- **사용자**: 부모 (조작) / 4세 아이 (청취)
- **핵심**: 잠자리 타이머 · 자동 연속 재생 · 볼륨 페이드아웃 · 한 손 UX

## Stack

- 단일 HTML 파일 (인라인 CSS/JS)
- 외부 의존성: YouTube IFrame Player API
- Vercel 정적 호스팅 (zero-config)

## 개발

브라우저에서 `index.html`을 직접 열거나 로컬 서버로 띄우세요.

```bash
python3 -m http.server 8000
# → http://localhost:8000
```

> Wake Lock API는 HTTPS 환경에서만 동작합니다. 로컬에서는 화면 꺼짐 방지가 비활성화될 수 있어요.

## 배포

`main` 브랜치 푸시 시 Vercel이 자동 배포합니다.

## 플레이리스트 수정

`index.html` 상단의 `PLAYLIST` 배열을 직접 편집하면 됩니다.

```js
const PLAYLIST = [
  { id: "유튜브_영상_ID", title: "동화 제목" },
  // ...
];
```

영상 ID는 `https://youtube.com/watch?v=XXXX`의 `XXXX` 부분.
