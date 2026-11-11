**[한국어](#ko) · [English](#en) · [中文](#zh) · [日本語](#ja) · [Oʻzbekcha](#uz) · [Русский](#ru) · [Tiếng Việt](#vi)**

---

<a id="ko"></a>

# 시계열 3부작 — ARIMA와 LSTM

lookback 14일과 window 14일은 같은 말일까? 같은 창을 보고도 ARIMA는 가중 평균을, LSTM은 조합을 찾는다. 며칠을 돌아볼지에서 시작해 숨은 상태와 고차원, "신경"이라는 이름의 아이러니까지, 3부 21쪽으로 따라가는 연구실 해설 대시보드입니다.

- 사이트: https://adminmrobo.github.io/timeseries-trilogy/
- 목차: [00_index.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.html) · 퀴즈 정답 모음: [00_answers.html](https://adminmrobo.github.io/timeseries-trilogy/00_answers.html)
- 글 · 안상선 ((주)M-Robo 대표) · AI 보조 제작

## 언어

지금은 **한국어판만** 있습니다. 2026-11-11 최신 연구실 스킬로 전면 다시 쓰면서 이전 외국어판(영어·중국어·일본어·우즈베크어·러시아어·베트남어)은 내렸고, 한국어판 검토가 끝나면 다시 만듭니다.

<!-- i18n:langtable -->
| 언어 | 파일 이름 | 바로 보기 |
|---|---|---|
| 한국어 | `00_index.html` | [바로 보기](https://adminmrobo.github.io/timeseries-trilogy/00_index.html) |
<!-- /i18n:langtable -->

## 무엇을 배우나

| 부 | 주제 | 쪽 | 대결 결과 (검증 MAE, 만 원) |
|---|---|---|---|
| 1부 | 며칠을 돌아볼 것인가 — lookback·window, 훈련·검증·시험 나누기, AR(14) 한 걸음씩, 한 번에 vs 굴려 가며, 세 선수 7·14·30, 학습 샘플 수 | 1-1 ~ 1-7 | AR(14) 3.16 vs AR(30) 2.74 → 주판봇 승 |
| 2부 | 같은 창, 다른 생각 — 계산기형 vs 독서형, LSTM 게이트, 가중합 vs 비선형 조합, 평평한 면 vs 휜 면, 표현 학습, 특성공학 | 2-1 ~ 2-7 | AR 2.89 vs LSTM 0.82 → 주판봇 승 |
| 3부 | 숨은 상태, 고차원, 그리고 신경의 아이러니 — HMM과 LSTM, 커널 트릭, 기준선 먼저, 표현력과 탐색, 과적합과 절제, 커넥톰 | 3-1 ~ 3-7 | AR 3.08 vs LSTM 2.97 → 무승부 (차이 5% 이내) |

3부 끝에서 봉인했던 시험 50일을 한 번만 엽니다(LSTM 2.06, AR(30) 2.37). 판정은 미리 정한 규칙(검증 기준)대로 바꾸지 않습니다.

## 페이지에 들어 있는 것

- 쪽마다: 원래 대화를 살린 대화 노트, 페이지 안에서 직접 돌려 보는 계산(AR 적합, 롤링 예측, 작은 LSTM·MLP), 용어 말풍선, 확인 퀴즈(전체 178문항)
- 부마다 마지막 쪽에 대결: 인턴 시아가 심판 깃발을 들고, 인턴 모아와 방청석의 누군가들이 지켜봅니다
- 지식 색인: 개념 799개, 관계 1,126개 (21쪽 합계) · 온톨로지·서지 꾸러미: JSON-LD, Turtle, CSV, CSL-JSON, BibTeX, RIS
- 부마다 파이썬 코드(numpy·statsmodels·PyTorch) — 페이지의 숫자를 그대로 다시 만든다
- 매출 기록 데이터는 설명용으로 만든 모형이며 실제 데이터가 아닙니다.

## 등장인물

| 이름 | 역할 |
|---|---|
| 박사 | 해설과 판정. 판정은 숫자대로 내린다 |
| 조수(하루) | 실험 진행과 숫자 발표. 판정은 하지 않는다 |
| 초파리 연구원 | 의심하는 쪽. 기준선과 검증부터 본다 |
| 주판봇 | 확신하는 쪽. 높은 숫자에 건다 |
| 인턴 시아 | 대결 심판. 시작 신호와 판정 확인 깃발 |
| 인턴 모아 | 방청석 응원과 안내. 대결이 끝나면 차를 권한다 |
| 미공개 X1·X2·X3 | 방청석의 누군가(실루엣). 목차의 "미공개 식구 보기" 버튼을 눌러야 보인다 |

## 파일 구성

| 파일 | 내용 |
|---|---|
| `index.html` | 첫 화면 (목차로 옮겨 감) |
| `00_index.html` | 목차, 매출 기록 목록, 대결 규칙, 강의자 키트, 등장인물 |
| `00_answers.html` | 퀴즈 178문항 정답·풀이 (인쇄용) |
| `1_1_…html` ~ `3_7_…html` | 본문 21쪽 (그림이 모두 들어 있는 단일 파일) |
| `cover_manifest.json` | 표지·온톨로지·번역 현황 목록 (현황판용) |
| `docs/` | 쪽별 이미지 명세서, 표지 지시문(`COVER_PROMPTS_timeseries.md`), 목차 헤드·썸네일 지시문(`THUMB_PROMPTS_timeseries.md`), 지식 색인 등록분 |

표지·썸네일 그림은 아직 없고, 받기 전까지는 캐릭터 넷이 선 대체 표지가 보입니다.

## 참고 문헌

1. Box & Jenkins (1970), Time Series Analysis: Forecasting and Control
2. Hyndman & Athanasopoulos (2021), Forecasting: Principles and Practice (3rd ed.)
3. Hochreiter & Schmidhuber (1997), Long Short-Term Memory, Neural Computation
4. Gers, Schmidhuber & Cummins (2000), Learning to Forget: Continual Prediction with LSTM, Neural Computation
5. Rabiner (1989), A Tutorial on Hidden Markov Models and Selected Applications in Speech Recognition, Proceedings of the IEEE
6. Cortes & Vapnik (1995), Support-Vector Networks, Machine Learning
7. Aizerman, Braverman & Rozonoer (1964), Theoretical Foundations of the Potential Function Method in Pattern Recognition Learning
8. Rumelhart, Hinton & Williams (1986), Learning Representations by Back-Propagating Errors, Nature
9. Makridakis, Spiliotis & Assimakopoulos (2018), The M4 Competition: Results, Findings, Conclusion and Way Forward, IJF
10. Makridakis, Spiliotis & Assimakopoulos (2020), The M4 Competition: 100,000 Time Series and 61 Forecasting Methods, IJF
11. Smyl 외 (2018), M4 Forecasting Competition: Introducing a New Hybrid ES-RNN Model, Uber Engineering Blog
12. Dorkenwald 외 (2024), Neuronal Wiring Diagram of an Adult Brain, Nature
13. Balasubramanian (2021), Brain Power, PNAS

## 라이선스

- 글: [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)
- 캐릭터(박사 · 조수 하루 · 초파리 연구원 · 주판봇 · 인턴 시아 · 인턴 모아 · 미공개 X1~X3)의 이름·설정·그림은 저작권자 안상선에게 있으며 허락 없이 쓸 수 없습니다.

## 만든 도구

- 해설 대시보드: [ahnboat_lab_explainer](https://github.com/adminmrobo/ahnboat_lab_explainer) (ai-lab-explainer, 캐릭터 팩 1.4)
- 캐릭터 그림: [fruitfly-lab-expressions](https://github.com/adminmrobo/fruitfly-lab-expressions) (86d04ac)

---

<a id="en"></a>

# Time-Series Trilogy — ARIMA and LSTM

Is a 14-day lookback the same thing as a 14-day window? A lab explainer dashboard in 3 parts and 21 pages, from how many days to look back to hidden states, higher dimensions and the irony of the name "neural".

Only the **Korean edition** is available right now. The series was fully rewritten on 2026-11-11 with the latest lab skill; the earlier translated editions were taken down and will be rebuilt after the Korean edition is reviewed. Start here: [00_index.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.html).

Characters: Professor, Assistant (Haru), Fruit Fly Researcher, AbaBot, intern Sia (duel referee), intern Moa (audience, guide) and three unrevealed silhouettes X1–X3 (audience). Text: CC BY-NC 4.0. Character names, settings and artwork © Ahn Sangsun; not to be used without permission.

---

<a id="zh"></a>

# 时间序列三部曲 — ARIMA 与 LSTM

回看 14 天的 lookback 和 14 天的 window 是一回事吗？这是一套分 3 部、共 21 页的研究室讲解仪表板。

目前只有**韩语版**。本系列已于 2026-11-11 用最新的研究室技能全面重写，原有外语版已下架，韩语版审阅完成后会重新制作。入口：[00_index.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.html)。

登场人物：博士、助手（Haru）、果蝇研究员、算盘宝、实习生 西娅（对决裁判）、实习生 茉雅（观众席·引导），以及未公开的剪影 X1~X3（观众）。文字：CC BY-NC 4.0。角色名称、设定和图画的著作权属于 Ahn Sangsun，未经许可不得使用。

---

<a id="ja"></a>

# 時系列三部作 — ARIMA と LSTM

14日の lookback と 14日の window は同じものでしょうか。3部21ページでたどる研究室の解説ダッシュボードです。

現在は**韓国語版のみ**です。2026-11-11 に最新の研究室スキルで全面的に書き直し、以前の外国語版は取り下げました。韓国語版の確認が終わってから作り直します。入口：[00_index.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.html)。

登場人物：博士、助手（Haru）、ショウジョウバエ研究員、アバボット、インターンのシア（対決の審判）、インターンのモア（観客席・案内）、未公開のシルエット X1〜X3（観客）。文章：CC BY-NC 4.0。キャラクターの名前・設定・絵の著作権は Ahn Sangsun にあり、許可なく使うことはできません。

---

<a id="uz"></a>

# Vaqt qatorlari trilogiyasi — ARIMA va LSTM

14 kunlik lookback bilan 14 kunlik window bir narsami? 3 qism, 21 sahifadan iborat laboratoriya tushuntirish paneli.

Hozircha faqat **koreyscha nusxa** mavjud. Seriya 2026-11-11 da eng yangi laboratoriya koʻnikmasi bilan toʻliq qayta yozildi; avvalgi tarjimalar olib tashlandi va koreyscha nusxa koʻrib chiqilgach qayta tayyorlanadi. Boshlash: [00_index.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.html).

Qahramonlar: Professor, Yordamchi (Haru), Meva pashshasi tadqiqotchi, AbaBot, stajyor Sia (bellashuv hakami), stajyor Moa (tomoshabinlar, yoʻl koʻrsatuvchi) va oshkor qilinmagan uchta siluet X1–X3 (tomoshabinlar). Matn: CC BY-NC 4.0. Qahramonlar nomlari, tavsiflari va rasmlariga mualliflik huquqi Ahn Sangsunga tegishli; ruxsatsiz foydalanish mumkin emas.

---

<a id="ru"></a>

# Трилогия о временных рядах — ARIMA и LSTM

Ретроспектива (lookback) в 14 дней и окно (window) в 14 дней — это одно и то же? Учебная панель лаборатории из 3 частей и 21 страницы.

Сейчас доступна только **корейская версия**. 2026-11-11 серия полностью переписана по новейшему навыку лаборатории; прежние переводы сняты и будут сделаны заново после проверки корейской версии. Начать: [00_index.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.html).

Персонажи: Профессор, Ассистент (Хару), Исследователь Дрозофила, АбаБот, стажёр Сия (судья поединка), стажёр Моа (зрители, гид) и три нераскрытых силуэта X1–X3 (зрители). Текст: CC BY-NC 4.0. Имена, описания и рисунки персонажей принадлежат правообладателю Ahn Sangsun; использование без разрешения запрещено.

---

<a id="vi"></a>

# Bộ ba chuỗi thời gian — ARIMA và LSTM

Lookback 14 ngày và window 14 ngày có phải là một? Bảng điều khiển giải thích của phòng thí nghiệm gồm 3 phần, 21 trang.

Hiện chỉ có **bản tiếng Hàn**. Ngày 2026-11-11 bộ bài đã được viết lại toàn bộ theo kỹ năng phòng thí nghiệm mới nhất; các bản dịch cũ đã được gỡ xuống và sẽ được làm lại sau khi bản tiếng Hàn được duyệt. Bắt đầu: [00_index.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.html).

Nhân vật: Giáo sư, Trợ lý (Haru), Nhà nghiên cứu Ruồi giấm, AbaBot, thực tập sinh Sia (trọng tài cuộc đấu), thực tập sinh Moa (khán đài, hướng dẫn) và ba bóng đen chưa công bố X1–X3 (khán giả). Văn bản: CC BY-NC 4.0. Tên, thiết lập và hình vẽ các nhân vật thuộc quyền tác giả của Ahn Sangsun; không được sử dụng khi chưa được phép.
