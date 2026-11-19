# my-CALENDAR

노션 임베드용 구글 캘린더 위젯 (읽기 전용).

## 파일

- `index.html` — 실제로 쓰는 위젯. 구글 캘린더 기본 임베드를 그대로 띄웁니다. **API 키가 필요 없습니다.** (캘린더가 공개 상태여야 함)
- `calendar.html` — 같은 임베드를 감싼 예전 형식. 북마크용으로 남겨 둡니다.
- `fullcalendar.html` — FullCalendar UI + 한국 공휴일 표시 버전. 구글 API 키를 넣어야 동작합니다(아래 설명). 지금은 사용하지 않습니다.

## 공개(public) 캘린더 전제

`index.html`은 구글 캘린더의 공개 임베드를 쓰므로, 대상 캘린더가 공개로 설정되어 있어야 합니다.
공개 캘린더는 로그인 없이 읽히기 때문에 비밀 키가 필요 없습니다.

## fullcalendar.html 에 키를 넣을 때 (Google Cloud Console)

- 프로젝트: `notion-calendar-widget-490006`
- API 및 서비스 → 사용자 인증 정보 → API 키 만들기
- 애플리케이션 제한사항: 웹사이트 → `https://mtswork.github.io/*`
- API 제한사항: Google Calendar API
- 만든 키를 `fullcalendar.html`의 `API_KEY` 값에 넣습니다.

## 보안 메모

- 캘린더 ID는 소스에 평문 메일 주소가 남지 않도록 base64로 담아 두었습니다.
- 이 저장소는 공개입니다. 어떤 키도 커밋하지 마세요. (2026-11-19 과거 커밋에 남아 있던 노출 키·클라이언트 ID·이메일은 히스토리에서 제거했습니다.)
