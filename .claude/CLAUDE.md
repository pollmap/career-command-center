# 취업 대시보드 — Claude Project Config

## Project Overview
이찬희(충북대 경영 24학번) 취업 인텔리전스 대시보드. 188개 금융·공공기관을 5등급+마이너스 체계로 평가.

## Tech Stack
- Vanilla HTML/CSS/JS (단일 파일: index.html)
- Vercel 배포
- Google Fonts: Bebas Neue, Sora, Noto Sans KR, JetBrains Mono

## Design Reference
- **Primary**: cufa-web.vercel.app (Dark terminal + editorial finance aesthetic)
- **Tone**: Bloomberg meets developer tooling — serious, institutional, technically sharp
- **Colors**: Deep navy-black backgrounds (#06080e), blue/steel accents, gold for finance, green for growth
- **ZERO gradients** — flat solid colors only
- **ZERO purple** — use steel blue (#6080a0) instead

## Active Skills
1. **ui-ux-pro-max** — Design intelligence with 67 styles, 96 palettes, 57 font pairings
2. **frontend-design** — Distinctive UI creation, anti-"AI slop" guidelines
3. **web-design-guidelines** — Accessibility/UX audit against 100+ rules

## Scoring System (V1)
- DNA 적합도 (30pt) + 금융 시너지 (25pt) + 창업/빌더 시너지 (20pt) + 진입 적합도 (25pt) = 100점
- 현실 보정: 삭제
- 채용 규모, 경쟁률 보정: 삭제
- 금융/창업은 보너스가 아닌 정식 평가 카테고리

## Tier System (5등급 + 마이너스)
| 등급 | 이름 | 색상 | 점수 범위 |
|------|------|------|-----------|
| 1 | 최우선 | #e03050 | 80~100 |
| 2 | 핵심공략 | #e08020 | 65~79 |
| 3 | 전략도전 | #c0a030 | 50~64 |
| 4 | 관심유지 | #607890 | 35~49 |
| 5 | 비권장 | #404050 | 20~34 |
| M | 마이너스 | #1a1a24 | 0~19 |

## Design Rules
- ZERO gradients — flat solid colors only, no linear-gradient anywhere
- ZERO purple — use steel blue (#6080a0) instead of #9066f0
- NO generic fonts — use Sora/Bebas Neue for display, Noto Sans KR for body, JetBrains Mono for data
- Numbered sections (01, 02, 03) with editorial layout
- Terminal-style blocks for data summaries
- Gold (#e8a020) for finance indicators, Green (#20c860) for startup/growth
- 3-stage responsive: 480px / 768px / 1024px
- Mobile card view for table at <480px
- Touch targets minimum 44x44px
