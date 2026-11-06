# 1-4번 「50일을 한 번에? 하루씩 굴려 가며?」 이미지 제작 명세서

| 항목 | 내용 |
|---|---|
| 페이지 | 1_4_multi_vs_rolling.html |
| 모드 / 주 앵커 | 교과서 / C 장부: 한 번에 50쪽 미리 쓰기 vs 매일 장부 확인 후 한 쪽 |
| 시즌 | 기본 |
| 대결 | 이 페이지에는 대결 없음 (챕터 마지막 페이지에 있음) |
| 새로 그릴 그림 | P1 0장 (챕터 공용 bg·hero 재사용) · P2 0장 · P3 0장 |
| 제작 경로 | 직접 1장 (페이지에 넣음) · 외부 의뢰 0장 (챕터 공용은 IMG_00_index에서 의뢰) |
| 의뢰 도구 | Genspark (기본) |
| 진행 | 받음 0 / 의뢰 0 · 마지막 반영 아직 |
| 캐릭터 팩 표정 | 11장 (팩 커밋 107ce63) |
| 재사용 | 2장 (bg_c1, sc_c1_hero) |
| 그림이 없을 때 | 페이지는 캐릭터 팩 표정과 CSS 배경·픽셀아트로 이미 완성 상태 |

## 1. 그림체와 고정 외형
- 스타일: SKILL 18-3 (16비트 SNES 시대 픽셀 아트, 굵은 외곽선, 디더링 음영)
- 캐릭터 고정 외형: SKILL 18-4 표 그대로 (공식 저장소 `CHARACTER_CORE_EN`)
- 이 페이지 장소: 연구실 옆 회계실 — 큰 주판, 가죽 장부(빈 줄무늬 쪽), 원형 금고 문, 놋쇠 저울
- 장소 영어 묘사: *cozy accounting room beside the lab, a large wooden abacus, leather ledgers with blank striped pages, a round vault door, a brass scale*

## 2. 필요한 그림 전체

| # | 키 | 판 | 크기 | 상태 | 제작 | 우선 | 들어가는 곳 | 대신 쓰는 그림 |
|---|---|---|---|---|---|---|---|---|
| 1 | bg_c1 | F | 1920×720 | 재사용 (챕터 공용, IMG_00_index 3절) | 외부 | P1 | 히어로 배경 | CSS 그라데이션 + 벌집 무늬 + 픽셀아트 |
| 2 | sc_c1_hero | E | 1200×800 | 재사용 (챕터 공용) | 외부 | P1 | 히어로 무대 | 팩 표정 대화창 + 픽셀아트 무대 |
| 3 | asst_e07 | B | 팩 96 | 팩 | — | — | 말풍선·대화창 | — |
| 4 | asst_e13 | B | 팩 96 | 팩 | — | — | 말풍선·대화창 | — |
| 5 | doc_e08 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 | — |
| 6 | doc_e09 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 | — |
| 7 | doc_e13 | A | 팩 96 | 팩 | — | — | 말풍선·대화창 | — |
| 8 | fly_e08 | C | 팩 96 | 팩 | — | — | 말풍선·대화창 | — |
| 9 | fly_e09 | C | 팩 96 | 팩 | — | — | 말풍선·대화창 | — |
| 10 | fly_e10 | C | 팩 96 | 팩 | — | — | 말풍선·대화창 | — |
| 11 | fly_e13 | C | 팩 96 | 팩 | — | — | 말풍선·대화창 | — |
| 12 | robo_e13 | D | 팩 96 | 팩 | — | — | 말풍선·대화창 | — |
| 13 | robo_e16 | D | 팩 96 | 팩 | — | — | 말풍선·대화창 | — |
| 14 | thumb_1_4 | I | 600×400 | 넣음 | 직접 (목차 카드: CSS 배경 + 팩 표정 합성) | P2 | 00_index 카드 | 색 카드 |
| — | 행동으로 보기, 히어로 픽셀아트 | — | — | 코드 | 직접 | — | 부록 A 픽셀 지도 | — |

## 3. 새로 그릴 그림 상세

이 페이지 전용으로 새로 그릴 그림은 없다. 챕터 공용 배경 `bg_c1`와 히어로 장면 `sc_c1_hero`의 상세·프롬프트는 `IMG_00_index.md` 3절에 있다.

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
  "page": "1_4_multi_vs_rolling",
  "anchor": "C:한 번에 50쪽 미리 쓰기 vs 매일 장부 확인 후 한 쪽",
  "season": "default",
  "duel": null,
  "images": [
    {
      "key": "bg_c1",
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
      "alt": "연구실 옆 회계실에 큰 주판과 펼친 장부가 놓인 장면"
    },
    {
      "key": "sc_c1_hero",
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
      "key": "asst_e07",
      "pack": "asst_e07",
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
      "key": "doc_e13",
      "pack": "doc_e13",
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
      "key": "fly_e09",
      "pack": "fly_e09",
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
      "key": "robo_e13",
      "pack": "robo_e13",
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
      "key": "thumb_1_4",
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
    "commit": "107ce63"
  },
  "status_values": "pack | placed(직접, 넣음) | requested(의뢰) | received(받음) | applied(반영) | rejected(다시 의뢰)"
}
```
