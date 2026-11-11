# 2-7번 「대결 — 꺾인 매출 기록 앞에서, 곧은 면 vs 읽는 기억」 이미지 제작 명세서

| 항목 | 내용 |
|---|---|
| 페이지 | 2_7_duel_summary.html |
| 모드 / 주 앵커 | 교과서 / D 생활: 반동이 심한 가게의 매출 기록을 읽는 두 방식 |
| 시즌 | 기본 |
| 대결 | 같은 7일 창으로 반동 매출 기록 E의 다음 날 맞히기 (검증 MAE) → 결과 R (주판봇 승), 초파리 2.89 vs 주판봇 0.82만 원, 차이 2.07 (상대 72%) — 초파리 결과 후 표정은 폭포 눈물(E21) |
| 새로 그릴 그림 | P1 0장 (챕터 공용 bg·hero 재사용) · P2 0장 · P3 0장 |
| 제작 경로 | 직접 2장 (페이지에 넣음) · 외부 의뢰 0장 (챕터 공용은 IMG_00_index에서 의뢰) |
| 의뢰 도구 | Genspark (기본) |
| 진행 | 받음 0 / 의뢰 0 · 마지막 반영 아직 |
| 캐릭터 팩 표정 | 32장 (팩 커밋 86d04ac) |
| 재사용 | 2장 (bg_c2, sc_c2_hero) |
| 그림이 없을 때 | 페이지는 캐릭터 팩 표정과 CSS 배경·픽셀아트로 이미 완성 상태 |

## 1. 그림체와 고정 외형
- 스타일: SKILL 18-3 (16비트 SNES 시대 픽셀 아트, 굵은 외곽선, 디더링 음영)
- 캐릭터 고정 외형: SKILL 18-4 표 그대로 (공식 저장소 `CHARACTER_CORE_EN`)
- 이 페이지 장소: 밤의 연구실 한쪽 독서 구석 — 책장, 펼친 이야기책(빈 줄무늬 쪽), 스탠드, 한쪽에서 새어 드는 보라 연구실 불빛
- 장소 영어 묘사: *a quiet reading corner rendered as part of the same night lab world, a tall bookshelf, an open storybook with blank striped pages, a desk lamp, purple lab light spilling in from one side*

## 2. 필요한 그림 전체

| # | 키 | 판 | 크기 | 상태 | 제작 | 우선 | 들어가는 곳 | 대신 쓰는 그림 |
|---|---|---|---|---|---|---|---|---|
| 1 | bg_c2 | F | 1920×720 | 재사용 (챕터 공용, IMG_00_index 3절) | 외부 | P1 | 히어로 배경 | CSS 그라데이션 + 벌집 무늬 + 픽셀아트 |
| 2 | sc_c2_hero | E | 1200×800 | 재사용 (챕터 공용) | 외부 | P1 | 히어로 무대 | 팩 표정 대화창 + 픽셀아트 무대 |
| 3 | asst_e01 | B | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 4 | asst_e07 | B | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 5 | asst_e12 | B | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 6 | asst_e13 | B | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 7 | asst_e24 | B | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 8 | doc_e08 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 9 | doc_e09 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 10 | doc_e10 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 11 | doc_e13 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 12 | doc_e16 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 13 | fly_e08 | C | 팩 192 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 14 | fly_e10 | C | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 15 | fly_e13 | C | 팩 192 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 16 | fly_e14 | C | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 17 | fly_e16 | C | 팩 192 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 18 | fly_e21 | C | 팩 192 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 19 | moa_e01 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 20 | moa_e12 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 21 | moa_e13 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 22 | robo_e12 | D | 팩 192 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 23 | robo_e13 | D | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 24 | robo_e14 | D | 팩 192 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 25 | robo_e16 | D | 팩 192 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 26 | robo_e18 | D | 팩 192 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 27 | robo_e20 | D | 팩 192 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 28 | sia_e06 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 29 | sia_e10 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 30 | sia_e13 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 31 | sia_e16 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 32 | x1_e13 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 33 | x2_e13 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 34 | x3_e13 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 · 대결 | — |
| 35 | thumb_2_7 | I | 600×400 | 넣음 | 직접 (목차 카드: CSS 배경 + 팩 표정 합성) | P2 | 00_index 카드 | 색 카드 |
| 36 | sc_c2_outro | E | 1200×800 | 넣음 (합성본) | 직접 → 외부 선택 | P2 | 아웃트로 | 팩 표정 말풍선 4개 |
| — | 행동으로 보기, 히어로 픽셀아트 | — | — | 코드 | 직접 | — | 부록 A 픽셀 지도 | — |

## 3. 새로 그릴 그림 상세

이 페이지 전용으로 새로 그릴 그림은 없다. 챕터 공용 배경 `bg_c2`와 히어로 장면 `sc_c2_hero`의 상세·프롬프트는 `IMG_00_index.md` 3절에 있다.

## 4. 일관성 지침
- SKILL 18-9 그대로. 참고 이미지: `refs/original/jupanbot_ref_genspark_v0.png` + 장면에 나오는 캐릭터의 팩 표정 원본

## 5. 넘겨받은 뒤 처리
SKILL 18-15 절차 그대로.

## 6. 체크리스트
- [x] HTML의 모든 표정 `data-img` 키가 2절 표에 있음
- [x] 결과 전 그림에 승패 암시 없음
- [x] 팩에 있는 표정을 "새로 그림"에 넣지 않음
- [x] 장소가 주 앵커와 일치

## 7. 매니페스트
```json
{
  "page": "2_7_duel_summary",
  "anchor": "D:반동이 심한 가게의 매출 기록을 읽는 두 방식",
  "season": "default",
  "duel": {
    "result": "R",
    "gap": 2.07,
    "metric": "검증 MAE (만 원, 작을수록 좋음)",
    "fly": 2.89,
    "robo": 0.82
  },
  "images": [
    {
      "key": "bg_c2",
      "plate": "F",
      "size": [
        1920,
        720
      ],
      "maker": "external",
      "tool": "genspark",
      "status": "requested",
      "priority": "P1",
      "slot": "hero-bg",
      "fallback": "css",
      "alt": "밤의 연구실 한쪽 독서 구석에 책장과 펼친 이야기책이 놓인 장면"
    },
    {
      "key": "sc_c2_hero",
      "plate": "E",
      "size": [
        1200,
        800
      ],
      "maker": "external",
      "tool": "genspark",
      "status": "requested",
      "priority": "P1",
      "slot": "hero-stage",
      "fallback": "composite"
    },
    {
      "key": "asst_e01",
      "pack": "asst_e01",
      "plate": "B",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "asst_e07",
      "pack": "asst_e07",
      "plate": "B",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "asst_e12",
      "pack": "asst_e12",
      "plate": "B",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "asst_e13",
      "pack": "asst_e13",
      "plate": "B",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "asst_e24",
      "pack": "asst_e24",
      "plate": "B",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "doc_e08",
      "pack": "doc_e08",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "doc_e09",
      "pack": "doc_e09",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "doc_e10",
      "pack": "doc_e10",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "doc_e13",
      "pack": "doc_e13",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "doc_e16",
      "pack": "doc_e16",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "fly_e08",
      "pack": "fly_e08",
      "plate": "C",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "fly_e10",
      "pack": "fly_e10",
      "plate": "C",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "fly_e13",
      "pack": "fly_e13",
      "plate": "C",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "fly_e14",
      "pack": "fly_e14",
      "plate": "C",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "fly_e16",
      "pack": "fly_e16",
      "plate": "C",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "fly_e21",
      "pack": "fly_e21",
      "plate": "C",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "moa_e01",
      "pack": "moa_e01",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "moa_e12",
      "pack": "moa_e12",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "moa_e13",
      "pack": "moa_e13",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "robo_e12",
      "pack": "robo_e12",
      "plate": "D",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "robo_e13",
      "pack": "robo_e13",
      "plate": "D",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "robo_e14",
      "pack": "robo_e14",
      "plate": "D",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "robo_e16",
      "pack": "robo_e16",
      "plate": "D",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "robo_e18",
      "pack": "robo_e18",
      "plate": "D",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "robo_e20",
      "pack": "robo_e20",
      "plate": "D",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "sia_e06",
      "pack": "sia_e06",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "sia_e10",
      "pack": "sia_e10",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "sia_e13",
      "pack": "sia_e13",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "sia_e16",
      "pack": "sia_e16",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "x1_e13",
      "pack": "x1_e13",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "x2_e13",
      "pack": "x2_e13",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "x3_e13",
      "pack": "x3_e13",
      "plate": "A",
      "status": "pack",
      "alt": ""
    },
    {
      "key": "thumb_2_7",
      "plate": "I",
      "size": [
        600,
        400
      ],
      "maker": "claude",
      "status": "placed",
      "priority": "P2",
      "slot": "index-card"
    }
  ],
  "character_pack": {
    "repo": "adminmrobo/fruitfly-lab-expressions",
    "commit": "86d04ac"
  },
  "status_values": "pack | placed(직접, 넣음) | requested(의뢰) | received(받음) | applied(반영) | rejected(다시 의뢰)"
}
```
