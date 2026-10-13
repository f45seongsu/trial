# f45seongsu/trial — F45 성수 체험(트라이얼) 랜딩 페이지

- GitHub Pages: https://f45seongsu.github.io/trial/ (광고 유입용 랜딩)
- `index.html` 현행 페이지. `f45-seongsu-v4.html`, `v5.html`, `index (5).html`은 이전/시안 버전
- `meta.html` — 개인정보처리방침 (Meta 광고 심사용 URL이므로 경로 유지)
- 이미지: `why-0*.jpg`, `routine-*.jpg`, `og-image.jpg`(링크 미리보기), `f45-seongsu-video.mp4`
- 수정 후 commit + push까지 할 것
- 체험 신청 = 페이지 안 폼(이름·번호 + 연락 방법 문자/전화/카톡 + 편한 시간대) → Supabase Edge Function `landing-lead-edge-function`(소스는 app 레포 `supabase/functions/landing-lead/index.ts`) → `people`(source=웹랜딩, trial_memo) + 스튜디오 번호로 알림 문자(신규·재신청·기존 등록자 모두). 완료 화면에서 카톡 채널·문자·전화로 바로 연락 가능
- 폼 시간대 칩은 시간표(`tt-section`)와 맞춰둘 것
- 첫 화면(`.hero2`) = 수업 영상(`f45-seongsu-video.mp4`, 첫 장면 `hero-poster.jpg`) + 광고와 이어지는 한 줄(`heroTitle`/`heroSub`, utm_content·utm_campaign에 '내향'·'공감'·'45분'이 있으면 맞춤 문구 — 새 광고 문구 추가 시 index.html의 `V` 목록에 한 줄) + 가격 + 신청 / 카톡 먼저 물어보기
- 깔때기 기록 = Supabase `landing_events` (app 레포 `supabase/sql/23_landing_events.sql`, `LT()` 함수). 개인정보 넣지 말 것
