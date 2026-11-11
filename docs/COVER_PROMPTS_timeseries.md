# 표지 지시문 — 시계열 3부작 (목차 + 챕터 3)

SKILL 18-14 규칙으로 쓴 글 표지 4장의 지시문이다. 표지마다 **Genspark에 붙여 넣기** 블록을 그대로 복사해 쓰면 된다.

| 키 | 붙는 페이지 | 장소 (앵커) | 주제 은유 | 상태 |
|---|---|---|---|---|
| `cover_index` | `00_index.html` (목차) — 목차 헤드 배경·썸네일은 [`THUMB_PROMPTS_timeseries.md`](THUMB_PROMPTS_timeseries.md) | 밤의 연구실 전경 (B) | 벽을 가로지르는 긴 선 그래프 띠와 길이가 다른 창틀 셋 | 그릴 것 |
| `cover_ch1` | `1_1_lookback_window.html` (1부 첫 쪽), 1-2~1-7은 띠로 재사용 | 회계실 (C 장부) | 장부 쪽 띠 위를 미끄러지는 짧은 창틀과 긴 창틀 | 그릴 것 |
| `cover_ch2` | `2_1_calculator_vs_reader.html` (2부 첫 쪽), 2-2~2-7은 띠로 재사용 | 연구실 옆 독서실 (D 생활) | 같은 창틀 하나 — 한쪽은 곧은 자와 계산기, 다른 쪽은 빛나는 실이 엮여 휜 천 | 그릴 것 |
| `cover_ch3` | `3_1_hidden_state.html` (3부 첫 쪽), 3-2~3-7은 띠로 재사용 | 연구실 한구석의 어두운 무대 (D 생활) | 평평한 점 판이 떠올라 빛나는 유리 정육면체 안에서 색별로 갈라짐 | 그릴 것 |

**공통 참고 이미지 (함께 올리기):** 네 캐릭터 기본 그림 4장 — GitHub `adminmrobo/fruitfly-lab-expressions`의 `images/doctor/E13_neutral.png`, `images/haru/E13_neutral.png`, `images/fruitfly/E13_neutral.png`, `images/jupanbot/E13_neutral.png` (주판봇은 v2 기준 그림이 확정되면 그것으로 바꾼다). 첫 표지를 받은 뒤에는 그 표지도 함께 올려 화풍을 맞춘다.

**키 비율 (캐릭터 팩 C3, 2026-11 갱신):** 박사 1.00 · 조수 0.90 · 주판봇 0.72 · 초파리 0.41.

**규격 (네 장 공통):** 16:9, 가로 1920 이상 · 그림 안에 글자·숫자·로고 금지 · 얼굴·손·핵심 소품은 좌우 12%, 위 10%, 아래 18% 안쪽 · 왼쪽 아래 30% × 20%는 어둡고 단순하게(시리즈 이름 칩이 얹힘) · 결과를 암시하지 않는 **대결 전 장면**.

**받은 뒤:** 파일 이름을 `cover_index.png`, `cover_ch1.png`, `cover_ch2.png`, `cover_ch3.png`로 붙여 돌려주면 SKILL 18-15 절차로 WebP(1600×900, 960×540)로 바꿔 페이지 맨 위 표지 자리에 넣고 `cover_manifest.json`의 상태를 고친다.

---

## 1. `cover_index` — 목차

| 항목 | 내용 |
|---|---|
| 키 · 판 | cover_index (= cover_series) · L (16:9, 1920 이상) |
| 장소 (앵커) | 밤의 연구실 전경 (B) |
| 주제 은유 | 연구실 벽을 끝에서 끝까지 가로지르는 긴 종이 띠에 그려진 오르내리는 선 그래프(눈금·숫자 없음), 그 위에 길이가 다른 투명 창틀 셋(짧음·중간·긺)이 걸려 있다 |
| 네 캐릭터 포즈 | 박사: 가운데 뒤에서 그래프 띠를 따라 손을 길게 뻗어 가리킨다 / 조수: 오른쪽 앞 옆에서 빈 체크리스트가 끼워진 클립보드를 들고 띠를 올려다본다 / 초파리: 왼쪽에서 오른쪽을 보며 가장 짧은 창틀을 두 손으로 들어 띠에 대 본다 / 주판봇: 오른쪽에서 왼쪽을 보며 가장 긴 창틀을 회색 팔로 받쳐 들고, 안테나 끝 주판알이 빛난다 |
| 대체 글 (alt) | 밤의 연구실 벽을 가로지르는 긴 선 그래프 띠 앞에서, 초파리 연구원은 짧은 창틀을, 주판봇은 긴 창틀을 들어 보이고 박사와 조수가 함께 지켜보는 장면 |
| 앞 표지와 다른 점 | 시리즈 첫 표지. 이후 표지는 이 장소·소품(긴 그래프 띠, 세 창틀)을 다시 쓰지 않는다 |

**Genspark에 붙여 넣기 ↓**
```
웹페이지 맨 위에 거는 표지 그림 1장을 만들어 줘.
- 비율 16:9, 가로 1920px 이상
- 첨부한 참고 이미지의 네 캐릭터(박사, 조수, 초파리 연구원, 주판봇)를 같은 그림체·같은 외형으로, 넷 모두 등장
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 얼굴과 손은 가장자리에서 떨어진 가운데 영역에, 왼쪽 아래 구석은 어둡고 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Website top cover illustration, wide 16:9.
Match the art style, proportions and colors of the attached reference images exactly
(if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: wide night laboratory with test tube racks, stacks of lab notebooks, a blank chalkboard and a small server rack; a long paper ribbon stretches across the whole back wall from end to end, showing one hand-drawn line chart that rises and falls like daily sales, with no grid labels and no numbers; three empty transparent picture frames of different widths (short, medium, long) hang on the ribbon like sliding windows.
All four characters together:
chibi scientist, thin teal rectangular glasses, spiky black hair with one white streak, small ponytail at the back, white lab coat over black vest and tie, standing in the center back and stretching one arm along the ribbon to point at it;
girl researcher, long pink hair with two round buns and a navy streak, blue eyes, white lab coat over lavender hoodie, jeans, standing at the front right side holding a clipboard with a blank checklist and looking up at the ribbon;
anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, holding up the shortest frame with both hands against the ribbon;
boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, lifting the longest frame with its gray arms, the abacus bead on its antenna glowing softly.
Height ratio: scientist 1.00, girl 0.90, robot 0.72 including treads and antenna, fruit fly 0.41.
Visual metaphor of the topic: one long time-series line seen through windows of different lengths, without any text.
Composition: keep every face and hand inside the central safe area (12% margin left and right, 10% top, 18% bottom); keep the bottom-left corner dark and simple; the light falls on the long chart ribbon and the three frames.
Mood: curious, friendly rivalry, the moment before the result.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

**고칠 때 (같은 대화에서):** `Same four characters, same art style and composition. Change only: {고칠 점}. Still no text.`

---

## 2. `cover_ch1` — 1부 「며칠을 돌아볼 것인가」 (1-1 ~ 1-7)

| 항목 | 내용 |
|---|---|
| 키 · 판 | cover_ch1 · L (16:9, 1920 이상) |
| 장소 (앵커) | 연구실 옆 회계실 (C 장부) |
| 주제 은유 | 책상 위로 길게 펼쳐진 장부 쪽 띠(하루 한 칸씩, 빈 줄무늬 칸) 위를 짧은 창틀과 긴 창틀이 레일을 따라 미끄러진다. 짧은 창틀은 띠의 앞쪽부터, 긴 창틀은 한참 뒤쪽부터 놓여 있다 (긴 창은 늦게 시작한다) |
| 네 캐릭터 포즈 | 박사: 가운데 뒤에서 놋쇠 저울을 한 손에 들고 두 창틀을 번갈아 본다 / 조수: 왼쪽 뒤 옆에서 두꺼운 가죽 장부를 펼쳐 쪽을 넘긴다 / 초파리: 왼쪽 앞에서 오른쪽을 보며 짧은 창틀을 레일 위로 한 칸 밀고 있다 / 주판봇: 오른쪽 앞에서 왼쪽을 보며 긴 창틀 옆에 서서 한 팔로 큰 나무 주판알을 튕긴다 |
| 대체 글 (alt) | 따뜻한 램프가 켜진 회계실에서 길게 펼친 장부 띠 위로 초파리 연구원은 짧은 창틀을, 주판봇은 긴 창틀을 밀고, 박사가 저울을 들고 조수가 장부를 넘기는 장면 |
| 앞 표지와 다른 점 | 목차의 벽 그래프 대신 책상 위 장부 띠, 창틀 둘(짧음·긺)만. 박사는 가리키는 대신 저울, 조수는 클립보드 대신 장부. 장소가 연구실 전경에서 회계실로 |

**Genspark에 붙여 넣기 ↓**
```
웹페이지 맨 위에 거는 표지 그림 1장을 만들어 줘.
- 비율 16:9, 가로 1920px 이상
- 첨부한 참고 이미지의 네 캐릭터(박사, 조수, 초파리 연구원, 주판봇)를 같은 그림체·같은 외형으로, 넷 모두 등장
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 얼굴과 손은 가장자리에서 떨어진 가운데 영역에, 왼쪽 아래 구석은 어둡고 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Website top cover illustration, wide 16:9.
Match the art style, proportions and colors of the attached reference images exactly
(if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, with warm golden lamp light in this room.
Scene: cozy accounting room beside the lab, a giant wooden abacus on the back wall, leather ledgers with blank striped pages, a round vault door, a brass scale; on a long wooden desk a very long strip of ledger pages is unrolled from left to right, one blank striped cell per day, and two empty wooden picture frames ride on a thin brass rail above it — a short frame placed near the start of the strip and a long frame placed much further along.
All four characters together:
chibi scientist, thin teal rectangular glasses, spiky black hair with one white streak, small ponytail at the back, white lab coat over black vest and tie, standing in the center back holding a small brass scale in one hand and glancing from one frame to the other;
girl researcher, long pink hair with two round buns and a navy streak, blue eyes, white lab coat over lavender hoodie, jeans, standing at the back left side opening a thick leather ledger and turning a page;
anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, pushing the short frame one step along the rail;
boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, standing beside the long frame and flicking a bead on a wooden abacus with one arm.
Height ratio: scientist 1.00, girl 0.90, robot 0.72 including treads and antenna, fruit fly 0.41.
Visual metaphor of the topic: a short window and a long window looking back over the same daily ledger, the long one starting later, without any text.
Composition: keep every face and hand inside the central safe area (12% margin left and right, 10% top, 18% bottom); keep the bottom-left corner dark and simple; the light falls on the ledger strip and the two frames.
Mood: curious, friendly rivalry, the moment before the result.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

**고칠 때 (같은 대화에서):** `Same four characters, same art style and composition. Change only: {고칠 점}. Still no text.`

---

## 3. `cover_ch2` — 2부 「같은 창, 다른 생각」 (2-1 ~ 2-7)

| 항목 | 내용 |
|---|---|
| 키 · 판 | cover_ch2 · L (16:9, 1920 이상) |
| 장소 (앵커) | 연구실 옆 작은 독서실 (D 생활) — 한쪽에서 연구실 보라 조명이 새어 든다 |
| 주제 은유 | 커다란 책상 가운데 **같은 창틀 하나**가 세워져 있다. 창틀 왼쪽 책상에는 곧은 나무 자와 놋쇠 계산기, 평평한 유리판(가중합·평평한 면). 오른쪽에는 펼친 책들에서 빛나는 실이 뻗어 나와 서로 엮이며 부드럽게 휜 천이 되고, 그 사이에 작은 문 세 개(열림·반쯤·닫힘)가 떠 있다(LSTM 게이트·휜 면) |
| 네 캐릭터 포즈 | 박사: 가운데 뒤에서 창틀 위로 몸을 숙여 양손을 펼쳐 왼쪽과 오른쪽을 동시에 가리킨다 / 조수: 오른쪽 뒤 옆 책장 사다리에 올라 책 한 권을 꺼내며 내려다본다 / 초파리: 왼쪽에서 오른쪽을 보며 놋쇠 계산기 버튼에 한 손을 얹고 다른 손으로 자를 잡는다 / 주판봇: 오른쪽에서 왼쪽을 보며 회색 팔로 빛나는 실 몇 가닥을 감아 들고, 작은 문 하나를 살짝 연다 |
| 대체 글 (alt) | 독서실 책상 가운데 같은 창틀을 두고, 초파리 연구원 쪽에는 자와 계산기가, 주판봇 쪽에는 책에서 뻗은 빛나는 실과 작은 문들이 있고, 박사가 양쪽을 가리키며 조수가 사다리에서 책을 꺼내는 장면 |
| 앞 표지와 다른 점 | 장소가 독서실로 바뀌고, 창틀이 하나뿐(앞 표지는 길이가 다른 창틀 여럿). 박사는 저울 대신 양손 비교, 조수는 사다리 위. 초파리·주판봇은 창틀을 들지 않고 각자의 도구(계산기·실)를 만진다 |

**Genspark에 붙여 넣기 ↓**
```
웹페이지 맨 위에 거는 표지 그림 1장을 만들어 줘.
- 비율 16:9, 가로 1920px 이상
- 첨부한 참고 이미지의 네 캐릭터(박사, 조수, 초파리 연구원, 주판봇)를 같은 그림체·같은 외형으로, 넷 모두 등장
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 얼굴과 손은 가장자리에서 떨어진 가운데 영역에, 왼쪽 아래 구석은 어둡고 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Website top cover illustration, wide 16:9.
Match the art style, proportions and colors of the attached reference images exactly
(if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: a small reading room with tall bookshelves and a rolling ladder, rendered as part of the same night lab world, purple lab light spilling in from one side; in the middle of a large desk stands one single empty wooden window frame. On the left half of the desk: a straight wooden ruler, a brass mechanical calculator and a flat clear glass plate. On the right half: open books from which glowing threads rise, weave together and form a softly curved shimmering cloth, with three tiny floating doors among the threads — one open, one half open, one closed.
All four characters together:
chibi scientist, thin teal rectangular glasses, spiky black hair with one white streak, small ponytail at the back, white lab coat over black vest and tie, standing in the center back and leaning over the window frame, both arms spread to point at the left side and the right side at the same time;
girl researcher, long pink hair with two round buns and a navy streak, blue eyes, white lab coat over lavender hoodie, jeans, standing on the rolling ladder at the back right, pulling a book from the shelf and looking down at the desk;
anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, one hand resting on the brass calculator keys and the other holding the straight ruler;
boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, winding a few glowing threads around its gray arm and gently opening one of the tiny doors.
Height ratio: scientist 1.00, girl 0.90, robot 0.72 including treads and antenna, fruit fly 0.41.
Visual metaphor of the topic: the same window read in two ways — a straight weighted sum on a flat plate versus woven threads forming a curved surface with small gates, without any text.
Composition: keep every face and hand inside the central safe area (12% margin left and right, 10% top, 18% bottom); keep the bottom-left corner dark and simple; the light falls on the single window frame in the middle of the desk.
Mood: curious, friendly rivalry, the moment before the result.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

**고칠 때 (같은 대화에서):** `Same four characters, same art style and composition. Change only: {고칠 점}. Still no text.`

---

## 4. `cover_ch3` — 3부 「숨은 상태, 고차원, 그리고 신경의 아이러니」 (3-1 ~ 3-7)

| 항목 | 내용 |
|---|---|
| 키 · 판 | cover_ch3 · L (16:9, 1920 이상) |
| 장소 (앵커) | 연구실 한구석의 작은 어두운 무대 (D 생활) — 커튼 뒤에서 연구실 보라 조명이 새어 든다. 생물 앵커가 아니므로 현미경·해부 소품은 넣지 않는다 |
| 주제 은유 | 바닥의 평평한 판 위에 분홍·초록 두 색 점이 뒤섞여 있다. 그 판에서 점들이 위로 떠올라 공중의 빛나는 유리 정육면체 안으로 들어가고, 정육면체 안에서는 얇은 빛의 막 하나가 두 색을 깨끗이 가른다(고차원으로 올리면 갈라진다). 무대 뒤 반투명 커튼 너머에는 흐릿한 그림자 모양들이 보인다(숨은 상태) |
| 네 캐릭터 포즈 | 박사: 가운데 뒤에서 두 손을 아래에서 위로 들어 올리는 몸짓으로 점들을 정육면체로 띄운다 / 조수: 왼쪽 뒤 옆에서 밀랍으로 봉한 봉투가 든 작은 상자를 두 손으로 소중히 안고 있다 (봉인된 시험) / 초파리: 왼쪽 앞에서 오른쪽을 보며 바닥 판 가까이 쭈그려 앉아 돋보기로 점들을 살핀다 / 주판봇: 오른쪽 앞에서 왼쪽을 보며 정육면체를 올려다보고, 화면 얼굴에 별 모양 눈이 반짝인다 |
| 대체 글 (alt) | 어두운 무대에서 바닥 판의 점들이 빛나는 유리 정육면체로 떠오르고, 박사가 두 손으로 띄워 올리는 동안 초파리 연구원은 돋보기로 점을 살피고 주판봇은 정육면체를 올려다보며 조수는 봉인된 봉투 상자를 안고 있는 장면 |
| 앞 표지와 다른 점 | 창틀이 처음으로 없다. 장소는 어두운 무대, 빛은 정육면체에 모인다. 조수는 처음으로 봉인 상자를 들고, 초파리는 서 있지 않고 쭈그려 앉는다. 주판봇은 아무것도 들지 않고 올려다본다 |

**Genspark에 붙여 넣기 ↓**
```
웹페이지 맨 위에 거는 표지 그림 1장을 만들어 줘.
- 비율 16:9, 가로 1920px 이상
- 첨부한 참고 이미지의 네 캐릭터(박사, 조수, 초파리 연구원, 주판봇)를 같은 그림체·같은 외형으로, 넷 모두 등장
- 그림 안에 글자·숫자·로고를 넣지 말 것
- 얼굴과 손은 가장자리에서 떨어진 가운데 영역에, 왼쪽 아래 구석은 어둡고 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Website top cover illustration, wide 16:9.
Match the art style, proportions and colors of the attached reference images exactly
(if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: a small dark stage in a corner of the night lab, rendered as part of the same night lab world, purple lab light spilling in from behind a translucent curtain at the back, vague soft shadow shapes visible behind the curtain; on the floor lies a flat board scattered with mixed magenta and green dots; the dots float upward from the board into a glowing transparent glass cube hovering in the air, and inside the cube one thin sheet of light cleanly separates the magenta dots from the green dots. No microscope, no dissection tools.
All four characters together:
chibi scientist, thin teal rectangular glasses, spiky black hair with one white streak, small ponytail at the back, white lab coat over black vest and tie, standing in the center back raising both hands from low to high as if lifting the dots up into the cube;
girl researcher, long pink hair with two round buns and a navy streak, blue eyes, white lab coat over lavender hoodie, jeans, standing at the back left side carefully holding a small box of wax-sealed envelopes in both arms;
anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, on the left facing right, crouching close to the flat board and inspecting the dots with a magnifying glass;
boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, on the right facing left, looking up at the glowing cube with sparkling star-shaped pixel eyes on its screen.
Height ratio: scientist 1.00, girl 0.90, robot 0.72 including treads and antenna, fruit fly 0.41.
Visual metaphor of the topic: mixed points that cannot be split on a flat board become separable once lifted into a higher-dimensional cube, with hidden states as shadows behind a curtain, without any text.
Composition: keep every face and hand inside the central safe area (12% margin left and right, 10% top, 18% bottom); keep the bottom-left corner dark and simple; the light falls on the glowing glass cube.
Mood: curious, friendly rivalry, the moment before the result.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

**고칠 때 (같은 대화에서):** `Same four characters, same art style and composition. Change only: {고칠 점}. Still no text.`

---

## 표지 점검 (18-15-1)

- [x] 네 장 모두 네 캐릭터의 18-4 영어 묘사, 좌우 방향(초파리 왼쪽→오른쪽, 주판봇 오른쪽→왼쪽), 안전 영역, 금지 구절이 들어감
- [x] 결과 암시 없음 (네 장 모두 대결 전 장면, 승자 배치 없음)
- [x] 생물 앵커가 아닌 챕터에 현미경·해부 소품 없음 (3부는 명시적으로 뺌)
- [x] 표지끼리 장소(연구실 전경·회계실·독서실·무대)·소품(그래프 띠·장부 띠·창틀 하나·정육면체)·포즈가 겹치지 않음
- [ ] 받은 뒤 390·768·1280 폭에서 얼굴 잘림 확인 (반영할 때)
- [ ] 1600 WebP 220 KB 이하 (반영할 때)
