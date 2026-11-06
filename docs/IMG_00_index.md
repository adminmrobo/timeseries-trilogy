# 시리즈 공용 이미지 명세서

| 항목 | 내용 |
|---|---|
| 시리즈 | 시계열 3부작 — ARIMA와 LSTM, 페이지 21개 + 목차 |
| 시즌 | 기본 |
| 공용 표정 | 캐릭터 팩 96장 (커밋 107ce63) · 그림 없음 역할 키 3개 (doc_scale, asst_ledger, asst_board) |
| 의뢰 도구 | Genspark (기본) |
| 새로 그릴 그림 | 챕터 공용 P1 6장 (bg_c1~3, sc_c1~3_hero) · 목차 P1 3장 (cover_series, bg_index, lineup) |

## 1. 공용 표정 현황

| 키 | 팩 키 | 상태 | 쓰는 페이지 |
|---|---|---|---|
| doc_scale | (doc_e13로 대신) | 그림 없음 → P2 후보 | 대결 쪽 (무승부일 때만) |
| asst_ledger | (asst_e07로 대신) | 그림 없음 → P2 후보 | 모든 쪽 꾸러미 섹션 말풍선 (asst_e07 사용) |
| asst_board | (asst_e16로 대신) | 그림 없음 | 쓰지 않음 |

그 밖의 표정은 모두 팩에 있다. 쪽마다의 사용 목록은 각 `IMG_{쪽}_{이름}.md` 2절.

## 2. 목차·표지 그림

### 2-1. `cover_series` — 시리즈 표지 (J판 1600×900, 외부, P1)

**프롬프트 (복사해서 사용)**
```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 16:9 series cover, all four characters together, wide night laboratory; the Professor, a chibi male scientist with a big head, dark charcoal spiky hair with a white streak at the front, a small low ponytail at the back, very thick bold black eyebrows, teal-framed rectangular glasses, light peach skin, white lab coat over a black vest, black tie and black slacks, standing at the center pointing at a large blank wall map made only of circles and lines; the Fruit Fly, a tiny expressive cartoon fruit fly researcher with a dark charcoal-black segmented insect body, large glossy red compound eyes, a retro dark blue helmet with a yellow-white center stripe and small round side bolts, colorful dangling cables in magenta, purple and blue curving from the back of the helmet, a tiny white lab coat over a black vest, translucent veined wings, six thin black legs with the front pair used like hands, on the left looking up at the map; JUPANBOT (the abacus robot), a small chibi boxy beige retro CRT-monitor robot with thick dark outlines, a dark green screen face with mint pixel eyes and mouth, a short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, holding a wooden abacus, on the right looking up at the map beside a small wooden abacus; Haru, a cute anime girl lab assistant, long straight pink hair with navy blue streaks including a thick navy streak down the center of the bangs, two round messy hair buns on top of the head, a small ahoge, big bright blue eyes, light peach skin, wearing a lavender hoodie with white drawstrings over a white t-shirt, under an open white knee-length lab coat, at the side holding a blank scoreboard with three empty columns, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```
- 참고 이미지: `refs/original/jupanbot_ref_genspark_v0.png`, 네 캐릭터의 `E08_guiding.png`
- 대체 글: 밤의 연구실 벽 개념 지도 앞에 모인 네 캐릭터

### 2-2. `bg_index` — 목차 배경 (F판 1920×720, 외부, P1)

```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, wide 8:3 background, left side simple and calm for title text, details on the right, a long laboratory corridor with many doors in a row, each door leaking a different colored light (amber, cyan, purple), no characters, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```
- 대체 글: 연구실 복도, 문마다 다른 색 빛

### 2-3. `lineup` — 넷이 선 소개 컷 (G판 960×540, 직접)

- 직접 합성: 목차의 등장인물 섹션에 팩 표정 4장을 나란히 배치해 대신함 (넣음)

## 3. 챕터 공용 그림 (모든 쪽이 재사용)

### 3-1. `bg_c1` — 챕터 1 대표 배경 (F판 1920×720, 외부, P1)

| 항목 | 내용 |
|---|---|
| 앵커 | C 장부 앵커 |
| 구도 | 왼쪽 45%는 단순하게(제목이 얹힘), 오른쪽에 장소 소품 |
| 대체 글 | 연구실 옆 회계실, 펼친 장부 위에 14쪽·30쪽 창 틀이 빛나는 장면 |
| 대신 쓰는 그림 | CSS 그라데이션 + 벌집 무늬 + 픽셀아트 |

```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, wide 8:3 background, left side simple and calm for title text, details on the right, cozy accounting room beside the lab, a large wooden abacus, leather ledgers with blank striped pages, a round vault door, a brass scale, a long open ledger with blank striped pages lies on a desk; a glowing amber window frame highlights a band of 14 pages, a longer faint frame covers 30 pages, no characters, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-1-2. `sc_c1_hero` — 챕터 1 히어로 장면 (E판 1200×800, 외부, P1)

```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 3:2 landscape scene, medium brightness, cozy accounting room beside the lab, a large wooden abacus, leather ledgers with blank striped pages, a round vault door, a brass scale, the Professor, a chibi male scientist with a big head, dark charcoal spiky hair with a white streak at the front, a small low ponytail at the back, very thick bold black eyebrows, teal-framed rectangular glasses, light peach skin, white lab coat over a black vest, black tie and black slacks, standing at the back center with a hand on his chin; the Fruit Fly, a tiny expressive cartoon fruit fly researcher with a dark charcoal-black segmented insect body, large glossy red compound eyes, a retro dark blue helmet with a yellow-white center stripe and small round side bolts, colorful dangling cables in magenta, purple and blue curving from the back of the helmet, a tiny white lab coat over a black vest, translucent veined wings, six thin black legs with the front pair used like hands, on the left looking right with a suspicious look; JUPANBOT (the abacus robot), a small chibi boxy beige retro CRT-monitor robot with thick dark outlines, a dark green screen face with mint pixel eyes and mouth, a short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, holding a wooden abacus, on the right looking left holding up a shiny abacus bead; Haru, a cute anime girl lab assistant, long straight pink hair with navy blue streaks including a thick navy streak down the center of the bangs, two round messy hair buns on top of the head, a small ahoge, big bright blue eyes, light peach skin, wearing a lavender hoodie with white drawstrings over a white t-shirt, under an open white knee-length lab coat, at the side holding a blank striped ledger, a long open ledger with blank striped pages lies on a desk; a glowing amber window frame highlights a band of 14 pages, a longer faint frame covers 30 pages, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```
- 참고 이미지: `refs/original/jupanbot_ref_genspark_v0.png`, `images/fruitfly/E08_guiding.png`, `images/jupanbot/E16_proud.png`
- 확인할 것: 박사 안경이 둥글게 나오면 다시, 결과 전 장면이므로 승패 암시 금지

### 3-2. `bg_c2` — 챕터 2 대표 배경 (F판 1920×720, 외부, P1)

| 항목 | 내용 |
|---|---|
| 앵커 | D 생활 앵커 |
| 구도 | 왼쪽 45%는 단순하게(제목이 얹힘), 오른쪽에 장소 소품 |
| 대체 글 | 밤의 연구실 독서 구석, 계산기 책상과 책 읽는 책상이 나란한 장면 |
| 대신 쓰는 그림 | CSS 그라데이션 + 벌집 무늬 + 픽셀아트 |

```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, wide 8:3 background, left side simple and calm for title text, details on the right, a quiet reading corner inside the same night lab world, bookshelves, a reading lamp, a desk with an open book of blank striped pages, purple lab light spilling in from one side, two reading desks side by side: on the left a calculator with seven glowing beads in a row, on the right an open book whose pages glow one after another like a moving bookmark, no characters, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-2-2. `sc_c2_hero` — 챕터 2 히어로 장면 (E판 1200×800, 외부, P1)

```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 3:2 landscape scene, medium brightness, a quiet reading corner inside the same night lab world, bookshelves, a reading lamp, a desk with an open book of blank striped pages, purple lab light spilling in from one side, the Professor, a chibi male scientist with a big head, dark charcoal spiky hair with a white streak at the front, a small low ponytail at the back, very thick bold black eyebrows, teal-framed rectangular glasses, light peach skin, white lab coat over a black vest, black tie and black slacks, standing at the back center with a hand on his chin; the Fruit Fly, a tiny expressive cartoon fruit fly researcher with a dark charcoal-black segmented insect body, large glossy red compound eyes, a retro dark blue helmet with a yellow-white center stripe and small round side bolts, colorful dangling cables in magenta, purple and blue curving from the back of the helmet, a tiny white lab coat over a black vest, translucent veined wings, six thin black legs with the front pair used like hands, on the left looking right with a suspicious look; JUPANBOT (the abacus robot), a small chibi boxy beige retro CRT-monitor robot with thick dark outlines, a dark green screen face with mint pixel eyes and mouth, a short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, holding a wooden abacus, on the right looking left holding up a shiny abacus bead; Haru, a cute anime girl lab assistant, long straight pink hair with navy blue streaks including a thick navy streak down the center of the bangs, two round messy hair buns on top of the head, a small ahoge, big bright blue eyes, light peach skin, wearing a lavender hoodie with white drawstrings over a white t-shirt, under an open white knee-length lab coat, at the side holding a blank striped ledger, two reading desks side by side: on the left a calculator with seven glowing beads in a row, on the right an open book whose pages glow one after another like a moving bookmark, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```
- 참고 이미지: `refs/original/jupanbot_ref_genspark_v0.png`, `images/fruitfly/E08_guiding.png`, `images/jupanbot/E16_proud.png`
- 확인할 것: 박사 안경이 둥글게 나오면 다시, 결과 전 장면이므로 승패 암시 금지

### 3-3. `bg_c3` — 챕터 3 대표 배경 (F판 1920×720, 외부, P1)

| 항목 | 내용 |
|---|---|
| 앵커 | B 연구실 앵커 |
| 구도 | 왼쪽 45%는 단순하게(제목이 얹힘), 오른쪽에 장소 소품 |
| 대체 글 | 밤의 연구실 전경, 칠판의 평면에서 곡면으로 올라가는 도식과 신경망 모형 |
| 대신 쓰는 그림 | CSS 그라데이션 + 벌집 무늬 + 픽셀아트 |

```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, wide 8:3 background, left side simple and calm for title text, details on the right, wide night laboratory with test tube racks, a box of sealed envelopes, stacks of lab notebooks, a blank chalkboard, a small server rack, a blank chalkboard with an abstract diagram of circles and arrows rising from a flat plane into a curved surface, a small glowing neuron-like network model on a stand, no characters, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-3-2. `sc_c3_hero` — 챕터 3 히어로 장면 (E판 1200×800, 외부, P1)

```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 3:2 landscape scene, medium brightness, wide night laboratory with test tube racks, a box of sealed envelopes, stacks of lab notebooks, a blank chalkboard, a small server rack, the Professor, a chibi male scientist with a big head, dark charcoal spiky hair with a white streak at the front, a small low ponytail at the back, very thick bold black eyebrows, teal-framed rectangular glasses, light peach skin, white lab coat over a black vest, black tie and black slacks, standing at the back center with a hand on his chin; the Fruit Fly, a tiny expressive cartoon fruit fly researcher with a dark charcoal-black segmented insect body, large glossy red compound eyes, a retro dark blue helmet with a yellow-white center stripe and small round side bolts, colorful dangling cables in magenta, purple and blue curving from the back of the helmet, a tiny white lab coat over a black vest, translucent veined wings, six thin black legs with the front pair used like hands, on the left looking right with a suspicious look; JUPANBOT (the abacus robot), a small chibi boxy beige retro CRT-monitor robot with thick dark outlines, a dark green screen face with mint pixel eyes and mouth, a short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, holding a wooden abacus, on the right looking left holding up a shiny abacus bead; Haru, a cute anime girl lab assistant, long straight pink hair with navy blue streaks including a thick navy streak down the center of the bangs, two round messy hair buns on top of the head, a small ahoge, big bright blue eyes, light peach skin, wearing a lavender hoodie with white drawstrings over a white t-shirt, under an open white knee-length lab coat, at the side holding a blank striped ledger, a blank chalkboard with an abstract diagram of circles and arrows rising from a flat plane into a curved surface, a small glowing neuron-like network model on a stand, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```
- 참고 이미지: `refs/original/jupanbot_ref_genspark_v0.png`, `images/fruitfly/E08_guiding.png`, `images/jupanbot/E16_proud.png`
- 확인할 것: 박사 안경이 둥글게 나오면 다시, 결과 전 장면이므로 승패 암시 금지

## 4. 페이지별 대표 그림 모음

| 페이지 | 앵커 | bg | hero | thumb | 상태 |
|---|---|---|---|---|---|
| 1-1 lookback과 window | C | bg_c1 (재사용) | sc_c1_hero (재사용) | thumb_1_1 = doc_e08 + robo_e16 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 1-2 훈련·검증·시험 나누기 | C | bg_c1 (재사용) | sc_c1_hero (재사용) | thumb_1_2 = asst_e07 + fly_e07 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 1-3 ARIMA(14) 한 걸음씩 | C | bg_c1 (재사용) | sc_c1_hero (재사용) | thumb_1_3 = robo_e09 + doc_e07 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 1-4 한 번에 vs 굴려 가며 | C | bg_c1 (재사용) | sc_c1_hero (재사용) | thumb_1_4 = fly_e10 + asst_e04 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 1-5 세 선수 7·14·30 | C | bg_c1 (재사용) | sc_c1_hero (재사용) | thumb_1_5 = asst_e12 + robo_e12 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 1-6 학습 샘플 193·186·170 | C | bg_c1 (재사용) | sc_c1_hero (재사용) | thumb_1_6 = doc_e09 + fly_e09 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 1-7 대결·정리 | C | bg_c1 (재사용) | sc_c1_hero (재사용) | thumb_1_7 = doc_e18 + robo_e04 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 2-1 계산기형 vs 독서형 | D | bg_c2 (재사용) | sc_c2_hero (재사용) | thumb_2_1 = doc_e16 + robo_e08 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 2-2 LSTM 게이트 열어 보기 | D | bg_c2 (재사용) | sc_c2_hero (재사용) | thumb_2_2 = asst_e09 + fly_e04 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 2-3 가중합 vs 비선형 조합 | D | bg_c2 (재사용) | sc_c2_hero (재사용) | thumb_2_3 = robo_e10 + asst_e08 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 2-4 평평한 면 vs 휜 면 | D | bg_c2 (재사용) | sc_c2_hero (재사용) | thumb_2_4 = doc_e19 + fly_e16 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 2-5 새 좌표계 — 표현 학습 | D | bg_c2 (재사용) | sc_c2_hero (재사용) | thumb_2_5 = asst_e01 + doc_e04 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 2-6 특성공학 vs 특성 학습 | C | bg_c2 (재사용) | sc_c2_hero (재사용) | thumb_2_6 = robo_e07 + asst_e10 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 2-7 대결 · 2부 정리 | D | bg_c2 (재사용) | sc_c2_hero (재사용) | thumb_2_7 = doc_e10 + asst_e16 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 3-1 HMM과 LSTM의 숨은 상태 | D | bg_c3 (재사용) | sc_c3_hero (재사용) | thumb_3_1 = fly_e13 + doc_e12 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 3-2 고차원으로 가는 오래된 꿈 | D | bg_c3 (재사용) | sc_c3_hero (재사용) | thumb_3_2 = doc_e01 + robo_e13 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 3-3 “상대가 안 된다?” — 기준선 | B | bg_c3 (재사용) | sc_c3_hero (재사용) | thumb_3_3 = fly_e12 + robo_e20 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 3-4 복잡하게 + 효율적으로 | C | bg_c3 (재사용) | sc_c3_hero (재사용) | thumb_3_4 = asst_e19 + robo_e01 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 3-5 세 번째 축 — 과적합과 절제 | B | bg_c3 (재사용) | sc_c3_hero (재사용) | thumb_3_5 = asst_e24 + robo_e15 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 3-6 신경이라는 이름의 아이러니 | A | bg_c3 (재사용) | sc_c3_hero (재사용) | thumb_3_6 = fly_e19 + doc_e14 합성 | 썸네일 넣음(직접), 나머지 의뢰 |
| 3-7 대결 · 3부작 정리 | C | bg_c3 (재사용) | sc_c3_hero (재사용) | thumb_3_7 = asst_e14 + fly_e01 합성 | 썸네일 넣음(직접), 나머지 의뢰 |

## 5. 아이콘
- `icon_fly`, `icon_robo`, `icon_draw`, `icon_dq`: 직접 (팩 표정 머리 잘라 32·16px) — 아직 쓰는 자리 없음, 필요할 때 만듦

## 6. 매니페스트
```json
{
  "series": "시계열 3부작 — ARIMA와 LSTM",
  "shared": [
    {
      "key": "cover_series",
      "plate": "J",
      "maker": "external",
      "status": "requested",
      "priority": "P1"
    },
    {
      "key": "bg_index",
      "plate": "F",
      "maker": "external",
      "status": "requested",
      "priority": "P1"
    },
    {
      "key": "lineup",
      "plate": "G",
      "maker": "claude",
      "status": "placed",
      "priority": "P1"
    },
    {
      "key": "bg_c1",
      "plate": "F",
      "maker": "external",
      "status": "requested",
      "priority": "P1"
    },
    {
      "key": "bg_c2",
      "plate": "F",
      "maker": "external",
      "status": "requested",
      "priority": "P1"
    },
    {
      "key": "bg_c3",
      "plate": "F",
      "maker": "external",
      "status": "requested",
      "priority": "P1"
    },
    {
      "key": "sc_c1_hero",
      "plate": "E",
      "maker": "external",
      "status": "requested",
      "priority": "P1"
    },
    {
      "key": "sc_c2_hero",
      "plate": "E",
      "maker": "external",
      "status": "requested",
      "priority": "P1"
    },
    {
      "key": "sc_c3_hero",
      "plate": "E",
      "maker": "external",
      "status": "requested",
      "priority": "P1"
    }
  ],
  "pages": [
    "1_1_lookback_window",
    "1_2_split",
    "1_3_arima14",
    "1_4_multi_vs_rolling",
    "1_5_three_runners",
    "1_6_samples",
    "1_7_duel_summary",
    "2_1_calculator_vs_reader",
    "2_2_lstm_gates",
    "2_3_weighted_sum_vs_combination",
    "2_4_flat_vs_curved",
    "2_5_new_coordinates",
    "2_6_feature_engineering",
    "2_7_duel_summary",
    "3_1_hidden_state",
    "3_2_lifting_dimensions",
    "3_3_baseline_first",
    "3_4_capacity_and_search",
    "3_5_overfitting_restraint",
    "3_6_neural_irony",
    "3_7_duel_and_wrapup"
  ],
  "character_pack": {
    "repo": "adminmrobo/fruitfly-lab-expressions",
    "commit": "107ce63"
  }
}
```
