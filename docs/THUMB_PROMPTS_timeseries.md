# 목차 헤드 · 썸네일 지시문 — 시계열 3부작

SKILL 18-2(판 체계)·18-11(목차 명세)·18-6 R12(목차 카드)로 쓴 그림 지시문이다. 표지 4장(`cover_index`, `cover_ch1~3`)은 [`COVER_PROMPTS_timeseries.md`](COVER_PROMPTS_timeseries.md)에 있다. 이 파일은 그 나머지 — **목차 헤드 배경 1장, 공유 미리보기 1장, 페이지 카드 썸네일 21장**이다.

| 묶음 | 키 | 판 · 크기 | 쓰는 곳 | 그리기 |
|---|---|---|---|---|
| 목차 헤드 | `cover_index` | L · 1920×1080 | 목차 맨 위 표지 | 표지 지시문 1번 |
| 목차 헤드 | `bg_index` | F · 1920×720 (8:3) | 목차 표지 아래 히어로 배경 (제목이 왼쪽에 얹힘) | **새로** (아래 A-1) |
| 목차 헤드 | `og_index` | K · 1200×630 | 링크 공유 미리보기 | `cover_index`를 잘라 만든다 (새로 그리지 않음) |
| 썸네일 | `thumb_1_1` ~ `thumb_3_7` | I · 1200×800 (3:2) 생성 → 600×400 빌드 | 목차의 쪽 카드 21개 | **새로** (아래 B) |

**참고 이미지 (함께 올리기):** GitHub `adminmrobo/fruitfly-lab-expressions`의 `images/doctor/E13_neutral.png`, `images/haru/E13_neutral.png`, `images/fruitfly/E13_neutral.png`, `images/jupanbot/E13_neutral.png` 가운데 그 그림에 나오는 캐릭터만. 표지(`cover_index`)를 먼저 받았다면 그것도 함께 올려 화풍을 맞춘다.

**공통 규칙:** 그림 안에 글자·숫자·로고 금지 · 초파리는 왼쪽에서 오른쪽, 주판봇은 오른쪽에서 왼쪽을 본다 · 썸네일은 결과를 암시하지 않는다 · 키 비율 박사 1.00 · 조수 0.90 · 주판봇 0.72 · 초파리 0.41 (캐릭터 팩 C3) · 생물 앵커(3-6)가 아닌 그림에는 현미경·해부 소품을 넣지 않는다.

**받은 뒤:** 파일 이름을 키 그대로(`bg_index.png`, `thumb_1_1.png` …) 붙여 돌려주면 WebP로 바꿔(썸네일 600×400 · 40 KB 이하, 헤드 1280×480) 목차 카드와 헤드에 넣고 `cover_manifest.json`의 상태를 `ok`로 고친다.

---

## A. 목차 헤드

### A-1. `bg_index` — 목차 히어로 배경 (F판)

| 항목 | 내용 |
|---|---|
| 키 · 판 | bg_index · F (8:3, 1920×720) |
| 장소 (앵커) | 연구실 복도 (B) — 18-11 표 그대로: 문이 줄지어 있고 문마다 다른 색 빛이 샌다(각 쪽 = 방) |
| 시리즈 표식 | 복도 끝 벽에 오르내리는 선 그래프 종이 띠(숫자 없음) |
| 캐릭터 | 없음 (또는 복도 끝에 아주 작은 실루엣 넷) |
| 구도 | 왼쪽 45%는 단순하게(제목 글자 자리), 문과 빛은 오른쪽에 |
| 대체 글 (alt) | 문마다 다른 색 빛이 새어 나오는 밤의 연구실 복도, 끝 벽에 긴 선 그래프 띠가 걸려 있다 |

**Genspark에 붙여 넣기 ↓**
```
웹페이지 제목 뒤에 까는 넓은 배경 그림 1장을 만들어 줘.
- 비율 8:3, 1920×720px
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 왼쪽 45%는 어둡고 단순하게(제목 글자가 얹힘), 볼거리는 오른쪽에
아래 영어 프롬프트를 그대로 써 줘.

Wide page hero background, 8:3 landscape, 1920 x 720 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: a long night laboratory corridor seen in gentle one-point perspective, with a row of plain wooden doors on both sides; each door is slightly open and leaks a different colored light (warm gold, soft green, lavender, magenta, teal), as if every door is a different room of the same lab.
At the far end of the corridor a long paper ribbon with one rising and falling line chart, no numbers, hangs across the wall.
No characters, or at most four tiny distant silhouettes near the far end.
Composition: keep the left 45% simple and calm (dark floor and wall) because the title text sits there; put the doors and colored light mostly on the right side.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### A-2. `og_index` — 공유 미리보기 (K판)

새로 그리지 않는다. `cover_index`를 받으면 가운데 기준으로 1200×630으로 잘라 만든다(네 캐릭터 얼굴이 모두 들어가게, 위아래만 자름). 표지가 늦어지면 `bg_index` 오른쪽 부분을 잘라 임시로 쓴다.

---

## B. 쪽 카드 썸네일 21장 (I판, 3:2)

| 키 | 쪽 | 앵커 | 장면 (한 줄) | 캐릭터 |
|---|---|---|---|---|
| `thumb_1_1` | 1-1 lookback과 window | C 장부 (회계실) | 펼친 장부의 하루 칸 줄 위에 작은 나무 창틀이 마지막 며칠만 덮고, 그 다음 칸(내일)이 빈칸으로 빛난다 | 초파리 |
| `thumb_1_2` | 1-2 훈련·검증·시험 나누기 | C 장부 (회계실) | 긴 장부 띠를 날짜 순서대로 세 토막으로 자른다: 긴 훈련 토막, 중간 검증 토막, 맨 끝 토막은 밀랍 봉인 봉투 안으로 | 조수 |
| `thumb_1_3` | 1-3 ARIMA(14) 한 걸음씩 | C 장부 (회계실) | 주판봇이 주판알을 튕기면, 주판 막대마다 가는 빛줄이 지난 장부 칸으로 이어지고, 모두 모여 빈칸 하나로 흐른다 | 주판봇 |
| `thumb_1_4` | 1-4 한 번에 vs 굴려 가며 | C 장부 (회계실) | 왼쪽은 예측 카드가 앞으로 줄줄이 이어지며 점점 흐려지고 안개 부채꼴이 넓어진다. 오른쪽은 박사가 카드를 하루씩 진짜 장부 쪽으로 바꿔 끼운다 | 박사 |
| `thumb_1_5` | 1-5 세 선수 7·14·30 | C 장부 (회계실) | 폭이 다른 나무 창틀 셋(좁음·중간·넓음)에 작은 바퀴가 달려 바닥의 장부 띠 트랙 위를 나란히 달린다 | 초파리 · 주판봇 |
| `thumb_1_6` | 1-6 학습 샘플 193·186·170 | C 장부 (회계실) | 학습 카드 더미 셋의 높이가 조금씩 다르다(높음·조금 낮음·더 낮음). 조수가 자를 대어 높이를 잰다 | 조수 |
| `thumb_1_7` | 1-7 대결·정리 | C 장부 (회계실) | 놋쇠 저울 양쪽 접시에 짧은 창틀과 긴 창틀이 하나씩 놓여 수평을 이룬다(결과 암시 없음) | 초파리 · 박사 · 주판봇 |
| `thumb_2_1` | 2-1 계산기형 vs 독서형 | D 생활 | 천장에 매달린 창틀 하나 아래 책상 두 개: 왼쪽에서 초파리가 놋쇠 계산기를 두드리고, 오른쪽에서 주판봇이 두꺼운 책을 읽는다 | 초파리 · 주판봇 |
| `thumb_2_2` | 2-2 LSTM 게이트 열어 보기 | D 생활 | 구슬이 실린 컨베이어 벨트가 작은 문 셋을 지난다: 첫 문에서 구슬이 떨어져 나가고(잊기), 둘째 문에서 새 구슬이 들어오고(입력), 셋째 문에서 빛이 조금 새어 나온다(출력) | 주판봇 |
| `thumb_2_3` | 2-3 가중합 vs 비선형 조합 | D 생활 | 왼쪽 그릇은 계량스푼으로 두 색 물을 정해진 비율로 붓자 단정한 두 줄무늬가 된다. 오른쪽 그릇은 두 색이 소용돌이치며 새 셋째 색 무늬가 생긴다 | 조수 |
| `thumb_2_4` | 2-4 평평한 면 vs 휜 면 | D 생활 | 받침대 위의 평평한 유리판 옆에서, 박사가 두 손으로 다른 유리판을 부드럽게 휘어 올리고, 판 위의 점들이 휜 면을 따라 놓인다 | 박사 |
| `thumb_2_5` | 2-5 새 좌표계 — 표현 학습 | D 생활 | 엉켜 있던 분홍·초록 점 위에 투명한 격자판을 돌리고 늘여 얹자, 점들이 두 무리로 깔끔히 갈리고 곧은 자 하나로 나뉜다 | 초파리 |
| `thumb_2_6` | 2-6 특성공학 vs 특성 학습 | C 장부 (회계실) | 왼쪽 작업대에서 조수가 손으로 만든 도구(눈금 없는 띠자, 손으로 그린 물결 띠)를 다듬고, 오른쪽에서 주판봇의 화면에 이름 없는 빛 모양들이 저절로 생겨난다 | 조수 · 주판봇 |
| `thumb_2_7` | 2-7 대결 · 2부 정리 | D 생활 | 벽에 텐트(봉우리) 모양으로 오르내리는 막대 장부 그림(숫자 없음). 그 앞에서 초파리와 주판봇이 같은 작은 창틀을 하나씩 들고 마주 선다 | 초파리 · 주판봇 |
| `thumb_3_1` | 3-1 HMM과 LSTM의 숨은 상태 | D 생활 | 반투명 커튼 뒤에 보이지 않는 형체가 있고, 커튼 아래 틈으로 색 구슬(관측)만 하나씩 굴러 나온다. 초파리가 구슬을 보며 커튼 뒤를 짐작한다 | 초파리 |
| `thumb_3_2` | 3-2 고차원으로 가는 오래된 꿈 | D 생활 | 바닥 판에서 섞여 있던 점 가운데 한 색 점들만 용수철을 타고 위로 떠오르고, 그 사이를 얇은 빛 막 한 장이 가로지른다 | 박사 |
| `thumb_3_3` | 3-3 “상대가 안 된다?” — 기준선 | B 연구실 | 출발선에 소박한 나무 막대 다섯 개가 먼저 나란히 서 있고, 그 뒤로 거대한 반짝이는 기계가 대기한다 | 초파리 · 주판봇 |
| `thumb_3_4` | 3-4 복잡하게 + 효율적으로 | C 장부 (회계실) | 끝이 안 보이는 서랍장 통로(넓은 공간) 사이로 주판봇이 등불 빛줄기로 한 서랍을 곧장 비춘다 | 주판봇 |
| `thumb_3_5` | 3-5 세 번째 축 — 과적합과 절제 | B 연구실 | 코르크판에 핀이 흩어져 있고, 실 하나는 핀마다 걸려 지그재그로, 다른 실 하나는 부드러운 곡선으로 지난다. 조수가 지그재그 실의 핀을 뽑는다 | 조수 |
| `thumb_3_6` | 3-6 신경이라는 이름의 아이러니 | A 생물 | 형광 현미경 모니터의 뇌 점구름 옆, 빈 칠판에 동그라미와 곧은 선으로 된 단순한 망(인공 신경망)이 그려져 있다 | 초파리 · 박사 |
| `thumb_3_7` | 3-7 대결 · 3부작 정리 | C 장부 (회계실) | 금고실 책상 위 봉인 봉투 상자를 조수가 편지칼로 막 여는 순간. 양쪽에서 초파리와 주판봇이 숨죽여 기다린다 | 초파리 · 조수 · 주판봇 |

같은 부 안에서 장소·소품·캐릭터 조합이 겹치지 않게 골랐다. 1부는 회계실(C) 안에서 소품을 바꾸고, 2부는 독서실·작업실·부엌·유리 공방·지도실, 3부는 인형극 무대·관측실·출발선·서랍장 통로·코르크판·현미경 실험대·금고실이다.

**Genspark에 한 번에 맡길 때:** 아래 블록의 머리말을 한 번 붙이고, 영어 프롬프트를 한 장씩 차례로 넣는다. 같은 대화에서 이어 그리면 화풍이 맞는다.

**고칠 때 (같은 대화에서):** `Same characters, same art style and composition. Change only: {고칠 점}. Still no text.`

### `thumb_1_1` — 1-1 lookback과 window

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `1_1_lookback_window.html` |
| 장소 (앵커) | C 장부 (회계실) |
| 장면 | 펼친 장부의 하루 칸 줄 위에 작은 나무 창틀이 마지막 며칠만 덮고, 그 다음 칸(내일)이 빈칸으로 빛난다 |
| 캐릭터 | 초파리 |
| 대체 글 (alt) | 장부의 마지막 며칠을 덮은 작은 창틀과 빛나는 내일 칸을 초파리 연구원이 돋보기로 들여다보는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: cozy accounting room beside the lab, a giant wooden abacus, leather ledgers with blank striped pages, a round vault door, a brass scale, warm golden lamp light.
Main focus: an open ledger with a row of blank striped day cells; a small wooden window frame lies over the last few cells, and the next empty cell after them glows softly as tomorrow.
Character: anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, leaning over the frame with a magnifying glass.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_1_2` — 1-2 훈련·검증·시험 나누기

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `1_2_split.html` |
| 장소 (앵커) | C 장부 (회계실) |
| 장면 | 긴 장부 띠를 날짜 순서대로 세 토막으로 자른다: 긴 훈련 토막, 중간 검증 토막, 맨 끝 토막은 밀랍 봉인 봉투 안으로 |
| 캐릭터 | 조수 |
| 대체 글 (alt) | 조수가 긴 장부 띠를 시간 순서대로 세 토막으로 자르고 마지막 토막을 봉인 봉투에 넣는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: cozy accounting room beside the lab, a giant wooden abacus, leather ledgers with blank striped pages, a round vault door, a brass scale, warm golden lamp light.
Main focus: a long ledger ribbon cut in time order into three pieces on the desk: a long piece, a medium piece, and the last short piece being slipped into an envelope with a red wax seal.
Character: girl researcher, long pink hair with two round buns and a navy streak, blue eyes, white lab coat over lavender hoodie, jeans, standing at the desk holding large scissors in one hand and the sealed envelope in the other.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_1_3` — 1-3 ARIMA(14) 한 걸음씩

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `1_3_arima14.html` |
| 장소 (앵커) | C 장부 (회계실) |
| 장면 | 주판봇이 주판알을 튕기면, 주판 막대마다 가는 빛줄이 지난 장부 칸으로 이어지고, 모두 모여 빈칸 하나로 흐른다 |
| 캐릭터 | 주판봇 |
| 대체 글 (alt) | 주판봇이 주판알을 튕기자 지난 장부 칸들에서 뻗은 빛줄이 빈칸 하나로 모이는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: cozy accounting room beside the lab, a giant wooden abacus, leather ledgers with blank striped pages, a round vault door, a brass scale, warm golden lamp light.
Main focus: a wooden abacus whose rods are each linked by a thin glowing thread to one past ledger cell, and all the threads gather and flow into one single empty cell.
Character: boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, flicking an abacus bead with one gray arm.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_1_4` — 1-4 한 번에 vs 굴려 가며

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `1_4_multi_vs_rolling.html` |
| 장소 (앵커) | C 장부 (회계실) |
| 장면 | 왼쪽은 예측 카드가 앞으로 줄줄이 이어지며 점점 흐려지고 안개 부채꼴이 넓어진다. 오른쪽은 박사가 카드를 하루씩 진짜 장부 쪽으로 바꿔 끼운다 |
| 캐릭터 | 박사 |
| 대체 글 (alt) | 한쪽은 점점 흐려지는 예측 카드 줄, 다른 쪽은 박사가 하루씩 진짜 장부 쪽으로 바꿔 끼우는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: cozy accounting room beside the lab, a giant wooden abacus, leather ledgers with blank striped pages, a round vault door, a brass scale, warm golden lamp light.
Main focus: two paths across the desk: on the left a long chain of paper forecast cards stretching forward, each one fainter, inside a widening cone of mist; on the right the same chain where each card is being replaced, day by day, by a fresh real ledger page.
Character: chibi scientist, thin teal rectangular glasses, spiky black hair with one white streak, small ponytail at the back, white lab coat over black vest and tie, standing in the center behind the desk, swapping one forecast card for a real ledger page.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_1_5` — 1-5 세 선수 7·14·30

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `1_5_three_runners.html` |
| 장소 (앵커) | C 장부 (회계실) |
| 장면 | 폭이 다른 나무 창틀 셋(좁음·중간·넓음)에 작은 바퀴가 달려 바닥의 장부 띠 트랙 위를 나란히 달린다 |
| 캐릭터 | 초파리 · 주판봇 |
| 대체 글 (alt) | 폭이 다른 창틀 셋이 바퀴를 달고 장부 트랙을 달리고, 초파리 연구원과 주판봇이 양쪽에서 응원하는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: cozy accounting room beside the lab, a giant wooden abacus, leather ledgers with blank striped pages, a round vault door, a brass scale, warm golden lamp light.
Main focus: three wooden window frames of different widths — narrow, medium and wide — on tiny wheels, racing side by side along a ledger strip laid on the floor like a running track.
Characters: anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, cheering with both gloved hands raised; boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, cheering with its gray arms up, antenna bead glowing.
Height ratio when characters appear together: scientist 1.00, girl 0.90, robot 0.72 including treads and antenna, fruit fly 0.41.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_1_6` — 1-6 학습 샘플 193·186·170

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `1_6_samples.html` |
| 장소 (앵커) | C 장부 (회계실) |
| 장면 | 학습 카드 더미 셋의 높이가 조금씩 다르다(높음·조금 낮음·더 낮음). 조수가 자를 대어 높이를 잰다 |
| 캐릭터 | 조수 |
| 대체 글 (alt) | 높이가 조금씩 다른 학습 카드 더미 셋을 조수가 자로 재는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: cozy accounting room beside the lab, a giant wooden abacus, leather ledgers with blank striped pages, a round vault door, a brass scale, warm golden lamp light.
Main focus: three stacks of identical small training cards on the counting table, the first tall, the second a little shorter, the third shorter still.
Character: girl researcher, long pink hair with two round buns and a navy streak, blue eyes, white lab coat over lavender hoodie, jeans, kneeling beside the stacks and holding a ruler against them to compare their heights.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_1_7` — 1-7 대결·정리

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `1_7_duel_summary.html` |
| 장소 (앵커) | C 장부 (회계실) |
| 장면 | 놋쇠 저울 양쪽 접시에 짧은 창틀과 긴 창틀이 하나씩 놓여 수평을 이룬다(결과 암시 없음) |
| 캐릭터 | 초파리 · 박사 · 주판봇 |
| 대체 글 (alt) | 수평을 이룬 놋쇠 저울 양쪽에 짧은 창틀과 긴 창틀, 그 앞에서 초파리 연구원과 주판봇이 마주 서고 박사가 저울을 잡은 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: cozy accounting room beside the lab, a giant wooden abacus, leather ledgers with blank striped pages, a round vault door, a brass scale, warm golden lamp light.
Main focus: a brass balance scale on the desk with a short wooden window frame on one pan and a long one on the other, perfectly level.
Characters: anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, arms crossed, curious; chibi scientist, thin teal rectangular glasses, spiky black hair with one white streak, small ponytail at the back, white lab coat over black vest and tie, in the center back, holding the scale steady; boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, leaning forward eagerly.
Height ratio when characters appear together: scientist 1.00, girl 0.90, robot 0.72 including treads and antenna, fruit fly 0.41.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_2_1` — 2-1 계산기형 vs 독서형

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `2_1_calculator_vs_reader.html` |
| 장소 (앵커) | D 생활 — a reading room with tall bookshelves |
| 장면 | 천장에 매달린 창틀 하나 아래 책상 두 개: 왼쪽에서 초파리가 놋쇠 계산기를 두드리고, 오른쪽에서 주판봇이 두꺼운 책을 읽는다 |
| 캐릭터 | 초파리 · 주판봇 |
| 대체 글 (alt) | 같은 창틀 아래에서 초파리 연구원은 계산기를 두드리고 주판봇은 두꺼운 책을 읽는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: a reading room with tall bookshelves rendered as part of the same night lab world, purple lab light spilling in from one side.
Main focus: one small window frame hanging from the ceiling above two desks; under it, on the left desk, a brass mechanical calculator, and on the right desk, a thick open book.
Characters: anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, tapping the calculator keys; boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, reading the thick book held in its gray arms.
Height ratio when characters appear together: scientist 1.00, girl 0.90, robot 0.72 including treads and antenna, fruit fly 0.41.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_2_2` — 2-2 LSTM 게이트 열어 보기

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `2_2_lstm_gates.html` |
| 장소 (앵커) | D 생활 — a small workshop with brass pipes and levers |
| 장면 | 구슬이 실린 컨베이어 벨트가 작은 문 셋을 지난다: 첫 문에서 구슬이 떨어져 나가고(잊기), 둘째 문에서 새 구슬이 들어오고(입력), 셋째 문에서 빛이 조금 새어 나온다(출력) |
| 캐릭터 | 주판봇 |
| 대체 글 (alt) | 구슬이 실린 벨트가 작은 문 셋을 지나며 구슬이 빠지고 들어오고 빛이 새어 나오며, 주판봇이 레버를 당기는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: a small workshop with brass pipes and levers rendered as part of the same night lab world, purple lab light spilling in from one side.
Main focus: a conveyor belt carrying glowing beads passes through three small doors: at the first door some beads drop off, at the second door new beads are added, at the third door a little light leaks out.
Character: boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, pulling one of three levers.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_2_3` — 2-3 가중합 vs 비선형 조합

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `2_3_weighted_sum_vs_combination.html` |
| 장소 (앵커) | D 생활 — a kitchen corner of the lab |
| 장면 | 왼쪽 그릇은 계량스푼으로 두 색 물을 정해진 비율로 붓자 단정한 두 줄무늬가 된다. 오른쪽 그릇은 두 색이 소용돌이치며 새 셋째 색 무늬가 생긴다 |
| 캐릭터 | 조수 |
| 대체 글 (alt) | 계량스푼으로 정해진 비율로 섞은 그릇과 두 색이 소용돌이쳐 새 무늬를 만든 그릇 사이에서 조수가 놀라는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: a kitchen corner of the lab rendered as part of the same night lab world, purple lab light spilling in from one side.
Main focus: two glass bowls: in the left bowl two colored liquids poured with measuring spoons settle into neat fixed stripes; in the right bowl the same two colors swirl together and create a brand-new third color pattern.
Character: girl researcher, long pink hair with two round buns and a navy streak, blue eyes, white lab coat over lavender hoodie, jeans, standing between the bowls holding two measuring spoons, looking at the swirling bowl with surprise.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_2_4` — 2-4 평평한 면 vs 휜 면

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `2_4_flat_vs_curved.html` |
| 장소 (앵커) | D 생활 — a glass workshop |
| 장면 | 받침대 위의 평평한 유리판 옆에서, 박사가 두 손으로 다른 유리판을 부드럽게 휘어 올리고, 판 위의 점들이 휜 면을 따라 놓인다 |
| 캐릭터 | 박사 |
| 대체 글 (alt) | 평평한 유리판 옆에서 박사가 다른 유리판을 두 손으로 부드럽게 휘어 올리는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: a glass workshop rendered as part of the same night lab world, purple lab light spilling in from one side.
Main focus: a flat clear glass sheet on a stand, and next to it a second glass sheet being gently bent into a smooth curve, with small colored dots resting along the curved surface.
Character: chibi scientist, thin teal rectangular glasses, spiky black hair with one white streak, small ponytail at the back, white lab coat over black vest and tie, in the center, bending the second glass sheet with both hands, a small purple spark at his fingertips.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_2_5` — 2-5 새 좌표계 — 표현 학습

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `2_5_new_coordinates.html` |
| 장소 (앵커) | D 생활 — a map room with a large drafting table |
| 장면 | 엉켜 있던 분홍·초록 점 위에 투명한 격자판을 돌리고 늘여 얹자, 점들이 두 무리로 깔끔히 갈리고 곧은 자 하나로 나뉜다 |
| 캐릭터 | 초파리 |
| 대체 글 (alt) | 돌리고 늘인 투명 격자판 위에서 엉켰던 점들이 두 무리로 갈리고 초파리 연구원이 곧은 자로 나누는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: a map room with a large drafting table rendered as part of the same night lab world, purple lab light spilling in from one side.
Main focus: a tangled scatter of magenta and green dots on the drafting table; a transparent grid sheet laid on top has been rotated and stretched so the dots now fall into two neat groups, separated by one straight ruler.
Character: anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, placing the straight ruler between the two groups.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_2_6` — 2-6 특성공학 vs 특성 학습

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `2_6_feature_engineering.html` |
| 장소 (앵커) | C 장부 (회계실) |
| 장면 | 왼쪽 작업대에서 조수가 손으로 만든 도구(눈금 없는 띠자, 손으로 그린 물결 띠)를 다듬고, 오른쪽에서 주판봇의 화면에 이름 없는 빛 모양들이 저절로 생겨난다 |
| 캐릭터 | 조수 · 주판봇 |
| 대체 글 (alt) | 조수가 작업대에서 손으로 지표 도구를 다듬고, 주판봇 위로 이름 없는 빛 모양들이 저절로 생기는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: cozy accounting room beside the lab, a giant wooden abacus, leather ledgers with blank striped pages, a round vault door, a brass scale, warm golden lamp light.
Main focus: on the left a workbench with hand-made measuring tools — a plain sliding strip and a hand-drawn wavy band; on the right glowing unnamed shapes form by themselves in the air above a robot.
Characters: girl researcher, long pink hair with two round buns and a navy streak, blue eyes, white lab coat over lavender hoodie, jeans, at the left workbench, carefully shaping a hand-made strip; boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, watching glowing shapes appear above its screen.
Height ratio when characters appear together: scientist 1.00, girl 0.90, robot 0.72 including treads and antenna, fruit fly 0.41.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_2_7` — 2-7 대결 · 2부 정리

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `2_7_duel_summary.html` |
| 장소 (앵커) | D 생활 — a reading room with tall bookshelves |
| 장면 | 벽에 텐트(봉우리) 모양으로 오르내리는 막대 장부 그림(숫자 없음). 그 앞에서 초파리와 주판봇이 같은 작은 창틀을 하나씩 들고 마주 선다 |
| 캐릭터 | 초파리 · 주판봇 |
| 대체 글 (alt) | 봉우리 모양 막대 장부 앞에서 초파리 연구원과 주판봇이 같은 크기 창틀을 들고 마주 선 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: a reading room with tall bookshelves rendered as part of the same night lab world, purple lab light spilling in from one side.
Main focus: on the wall a ledger bar chart shaped like a tent — bars rising to a peak and falling again, with no numbers; in front of it two identical small window frames.
Characters: anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, holding one small window frame; boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, holding an identical small window frame.
Height ratio when characters appear together: scientist 1.00, girl 0.90, robot 0.72 including treads and antenna, fruit fly 0.41.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_3_1` — 3-1 HMM과 LSTM의 숨은 상태

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `3_1_hidden_state.html` |
| 장소 (앵커) | D 생활 — a small puppet theater in a corner of the lab |
| 장면 | 반투명 커튼 뒤에 보이지 않는 형체가 있고, 커튼 아래 틈으로 색 구슬(관측)만 하나씩 굴러 나온다. 초파리가 구슬을 보며 커튼 뒤를 짐작한다 |
| 캐릭터 | 초파리 |
| 대체 글 (alt) | 반투명 커튼 아래로 굴러 나오는 색 구슬만 보고 초파리 연구원이 커튼 뒤를 짐작하는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: a small puppet theater in a corner of the lab rendered as part of the same night lab world, purple lab light spilling in from one side.
Main focus: a translucent curtain hides a vague figure behind it; only colored marbles roll out one by one from the gap under the curtain.
Character: anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, crouching to examine the marbles with a magnifying glass.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_3_2` — 3-2 고차원으로 가는 오래된 꿈

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `3_2_lifting_dimensions.html` |
| 장소 (앵커) | D 생활 — a quiet observatory room with a domed ceiling |
| 장면 | 바닥 판에서 섞여 있던 점 가운데 한 색 점들만 용수철을 타고 위로 떠오르고, 그 사이를 얇은 빛 막 한 장이 가로지른다 |
| 캐릭터 | 박사 |
| 대체 글 (alt) | 섞인 점 가운데 한 색만 용수철로 떠오르고 그 사이를 빛 막이 가르는 것을 박사가 손을 들어 보여 주는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: a quiet observatory room with a domed ceiling rendered as part of the same night lab world, purple lab light spilling in from one side.
Main focus: a flat board of mixed magenta and green dots; the green dots rise on small springs to a higher level, and one thin sheet of light slides horizontally between the two heights.
Character: chibi scientist, thin teal rectangular glasses, spiky black hair with one white streak, small ponytail at the back, white lab coat over black vest and tie, in the center, raising one hand as the springs lift the dots.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_3_3` — 3-3 “상대가 안 된다?” — 기준선

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `3_3_baseline_first.html` |
| 장소 (앵커) | B 연구실 |
| 장면 | 출발선에 소박한 나무 막대 다섯 개가 먼저 나란히 서 있고, 그 뒤로 거대한 반짝이는 기계가 대기한다 |
| 캐릭터 | 초파리 · 주판봇 |
| 대체 글 (alt) | 출발선에 소박한 막대 다섯을 먼저 세우는 초파리 연구원과 뒤의 거대한 기계를 자랑하는 주판봇의 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: wide night laboratory with test tube racks, a box of sealed envelopes, stacks of lab notebooks, a blank chalkboard, a small server rack.
Main focus: five plain wooden measuring sticks standing in a neat row at a starting line on the floor, and behind them a huge shiny complicated machine waiting.
Characters: anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, placing the last plain stick in the row; boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, proudly patting the big shiny machine.
Height ratio when characters appear together: scientist 1.00, girl 0.90, robot 0.72 including treads and antenna, fruit fly 0.41.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_3_4` — 3-4 복잡하게 + 효율적으로

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `3_4_capacity_and_search.html` |
| 장소 (앵커) | C 장부 (회계실) |
| 장면 | 끝이 안 보이는 서랍장 통로(넓은 공간) 사이로 주판봇이 등불 빛줄기로 한 서랍을 곧장 비춘다 |
| 캐릭터 | 주판봇 |
| 대체 글 (alt) | 끝없는 서랍장 통로에서 주판봇이 등불 빛으로 서랍 하나를 곧장 비추는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: cozy accounting room beside the lab, a giant wooden abacus, leather ledgers with blank striped pages, a round vault door, a brass scale, warm golden lamp light.
Main focus: endless rows of tall wooden drawer cabinets stretching far into the distance; a single lantern beam cuts straight down one aisle and lights up one drawer.
Character: boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, rolling down the aisle holding the lantern high.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_3_5` — 3-5 세 번째 축 — 과적합과 절제

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `3_5_overfitting_restraint.html` |
| 장소 (앵커) | B 연구실 |
| 장면 | 코르크판에 핀이 흩어져 있고, 실 하나는 핀마다 걸려 지그재그로, 다른 실 하나는 부드러운 곡선으로 지난다. 조수가 지그재그 실의 핀을 뽑는다 |
| 캐릭터 | 조수 |
| 대체 글 (alt) | 핀마다 걸린 지그재그 실과 부드러운 곡선 실이 있는 코르크판에서 조수가 핀을 뽑는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: wide night laboratory with test tube racks, a box of sealed envelopes, stacks of lab notebooks, a blank chalkboard, a small server rack.
Main focus: a cork board with scattered pins: one string zigzags tightly through every single pin, another string passes smoothly in a gentle curve.
Character: girl researcher, long pink hair with two round buns and a navy streak, blue eyes, white lab coat over lavender hoodie, jeans, pulling out a pin from the zigzag string, thoughtful.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_3_6` — 3-6 신경이라는 이름의 아이러니

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `3_6_neural_irony.html` |
| 장소 (앵커) | A 생물 |
| 장면 | 형광 현미경 모니터의 뇌 점구름 옆, 빈 칠판에 동그라미와 곧은 선으로 된 단순한 망(인공 신경망)이 그려져 있다 |
| 캐릭터 | 초파리 · 박사 |
| 대체 글 (alt) | 형광 뇌 점구름과 칠판의 단순한 동그라미 망을 박사가 번갈아 가리키고 초파리 연구원이 현미경에서 고개를 드는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: night laboratory bench with a fluorescence microscope, petri dishes and fly vials, a monitor glowing with a magenta and green neuron point cloud.
Main focus: next to the glowing neuron point cloud on the monitor, a blank chalkboard shows a very simple network of round nodes joined by straight lines, the two side by side.
Characters: anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, looking up from the microscope; chibi scientist, thin teal rectangular glasses, spiky black hair with one white streak, small ponytail at the back, white lab coat over black vest and tie, in the center back, gesturing from the neuron cloud to the simple network.
Height ratio when characters appear together: scientist 1.00, girl 0.90, robot 0.72 including treads and antenna, fruit fly 0.41.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

### `thumb_3_7` — 3-7 대결 · 3부작 정리

| 항목 | 내용 |
|---|---|
| 들어가는 곳 | `00_index.html` 카드 → `3_7_duel_and_wrapup.html` |
| 장소 (앵커) | C 장부 (회계실) |
| 장면 | 금고실 책상 위 봉인 봉투 상자를 조수가 편지칼로 막 여는 순간. 양쪽에서 초파리와 주판봇이 숨죽여 기다린다 |
| 캐릭터 | 초파리 · 조수 · 주판봇 |
| 대체 글 (alt) | 금고실에서 조수가 봉인 봉투를 막 열고 초파리 연구원과 주판봇이 양쪽에서 기다리는 그림 |

**Genspark에 붙여 넣기 ↓**
```
썸네일 그림 1장을 만들어 줘.
- 비율 3:2, 1200×800px
- 첨부한 참고 이미지의 캐릭터를 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 작게(가로 400px) 보여도 알아볼 수 있게 소품 하나에 집중, 배경은 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Index card thumbnail illustration, 3:2 landscape, 1200 x 800 pixels.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: cozy accounting room beside the lab, a giant wooden abacus, leather ledgers with blank striped pages, a round vault door, a brass scale, warm golden lamp light.
Main focus: a box of wax-sealed envelopes on the desk in front of the round vault door, one envelope just about to be opened with a letter opener.
Characters: anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, holding its breath; girl researcher, long pink hair with two round buns and a navy streak, blue eyes, white lab coat over lavender hoodie, jeans, in the center, carefully cutting the seal with a letter opener; boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, waiting eagerly.
Height ratio when characters appear together: scientist 1.00, girl 0.90, robot 0.72 including treads and antenna, fruit fly 0.41.
Keep it simple and readable when shown 400 pixels wide: one clear focal prop in the middle, large shapes, an uncluttered background, every face at least 60 pixels from the edges.
Mood: curious and calm, no hint of who wins.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

---

## 점검

- [x] 21장 모두 3:2, 글자·숫자 금지, 결과 암시 없음, 캐릭터 고정 외형(18-4) 영어 묘사 포함
- [x] 초파리 왼쪽→오른쪽, 주판봇 오른쪽→왼쪽, 두 명 이상이면 키 비율 문장 포함
- [x] 현미경은 3-6(생물 앵커)에만
- [x] 같은 부 안에서 장소·소품·캐릭터 조합이 겹치지 않음
- [ ] 받은 뒤 400px 폭에서 소품이 알아보이는지 (반영할 때)
