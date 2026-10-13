# f45seongsu/trial — F45 성수 체험(트라이얼) 랜딩 페이지

- GitHub Pages: https://f45seongsu.github.io/trial/ (광고 유입용 랜딩)
- `index.html` 현행 페이지. `f45-seongsu-v4.html`, `v5.html`, `index (5).html`은 이전/시안 버전
- `meta.html` — 개인정보처리방침 (Meta 광고 심사용 URL이므로 경로 유지)
- 이미지: `img/*` (현행), `og-image.jpg`(링크 미리보기), `map.png`. `why-0*.jpg`·`routine-*.jpg`·`f45-seongsu-video.mp4`·`hero-poster.jpg`는 예전 페이지용(지금은 안 씀)
- 수정 후 commit + push까지 할 것
- 체험 신청 = 페이지 안 폼(이름·번호 + 연락 방법 문자/전화/카톡 + 편한 시간대) → Supabase Edge Function `landing-lead-edge-function`(소스는 app 레포 `supabase/functions/landing-lead/index.ts`) → `people`(source=웹랜딩, trial_memo) + 스튜디오 번호로 알림 문자(신규·재신청·기존 등록자 모두). 완료 화면에서 카톡 채널·문자·전화로 바로 연락 가능
- 폼 시간대 칩은 시간표(`tt-section`)와 맞춰둘 것
- 2026-10 개편: 밝은 에디토리얼형. 사진은 본사 촬영본 `img/`(hero·hero-wide·coach·cardio·resistance·hybrid·team, 웹용으로 줄인 것), 로고 `img/logo-navy.png`·`img/logo-white.png`(신로고). 첫 화면 = 사진 + 짧은 문구 + 7일 40,000원 + 신청 / 카톡 문의. 영상(`f45-seongsu-video.mp4`)·글로벌 숫자·움직이는 띠는 뺌
- 깔때기 기록 = Supabase `landing_events` (app 레포 `supabase/sql/23_landing_events.sql`, `LT()` 함수). 개인정보 넣지 말 것
