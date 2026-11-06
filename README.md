**[한국어](#ko) · [English](#en) · [中文](#zh) · [日本語](#ja) · [Oʻzbekcha](#uz) · [Русский](#ru) · [Tiếng Việt](#vi)**

---

<a id="ko"></a>

# 시계열 3부작 — ARIMA와 LSTM

lookback 14일과 window 14일은 같은 말일까? 같은 창을 보고도 ARIMA는 가중 평균을, LSTM은 조합을 찾는다. 며칠을 돌아볼지에서 시작해 숨은 상태와 고차원, "신경"이라는 이름의 아이러니까지, 3부 21쪽으로 따라가는 연구실 해설 대시보드입니다.

- 사이트: https://adminmrobo.github.io/timeseries-trilogy/
- 목차: [00_index.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.html) · 퀴즈 정답 모음: [00_answers.html](https://adminmrobo.github.io/timeseries-trilogy/00_answers.html)
- 글 · 안상선 ((주)M-Robo 대표) · AI 보조 제작

## 언어

한국어 원본과 외국어판 6개로 볼 수 있습니다.

- 고르는 방법: 화면 최상단 메뉴의 언어 선택 상자에서 고릅니다.
- 자동 전환: 한국어 페이지에 들어오면, 브라우저 언어가 지원 언어일 때 그 언어판으로 옮겨 갑니다. 번역판 주소로 들어오면 그대로 엽니다.
- 주소 끝에 `?lang=en`처럼 붙이면 그 언어로 바로 엽니다. `?lang=ko`는 한국어판에 머뭅니다.
- 언어판 파일은 `이름.언어코드.html` 꼴입니다.

<!-- i18n:langtable -->
| 언어 | 파일 이름 | 바로 보기 |
|---|---|---|
| 한국어 | `00_index.html` | [바로 보기](https://adminmrobo.github.io/timeseries-trilogy/00_index.html) |
| English | `00_index.en.html` | [바로 보기](https://adminmrobo.github.io/timeseries-trilogy/00_index.en.html) |
| 中文 | `00_index.zh.html` | [바로 보기](https://adminmrobo.github.io/timeseries-trilogy/00_index.zh.html) |
| 日本語 | `00_index.ja.html` | [바로 보기](https://adminmrobo.github.io/timeseries-trilogy/00_index.ja.html) |
| Oʻzbekcha | `00_index.uz.html` | [바로 보기](https://adminmrobo.github.io/timeseries-trilogy/00_index.uz.html) |
| Русский | `00_index.ru.html` | [바로 보기](https://adminmrobo.github.io/timeseries-trilogy/00_index.ru.html) |
| Tiếng Việt | `00_index.vi.html` | [바로 보기](https://adminmrobo.github.io/timeseries-trilogy/00_index.vi.html) |
<!-- /i18n:langtable -->

## 무엇을 배우나

| 부 | 주제 | 쪽 | 대결 결과 (검증 50일 MAE, 만 원) |
|---|---|---|---|
| 1부 | 며칠을 돌아볼 것인가 — lookback·window, 훈련·검증·시험 나누기, AR(14) 한 걸음씩, 한 번에 vs 굴려 가며, 세 선수 7·14·30, 학습 샘플 수 | 1-1 ~ 1-7 | AR(14) 3.16 vs AR(30) 2.74 → 주판봇 승 |
| 2부 | 같은 창, 다른 생각 — 계산기형 vs 독서형, LSTM 게이트, 가중합 vs 비선형 조합, 평평한 면 vs 휜 면, 표현 학습, 특성공학 | 2-1 ~ 2-7 | AR 2.89 vs LSTM 0.82 → 주판봇 승 |
| 3부 | 숨은 상태, 고차원, 그리고 신경의 아이러니 — HMM과 LSTM, 커널 트릭, 기준선 먼저, 표현력과 탐색, 과적합과 절제, 커넥톰 | 3-1 ~ 3-7 | AR 3.08 vs LSTM 2.97 → 무승부 (차이 5% 이내) |

3부 끝에서 봉인했던 시험 50일을 한 번만 엽니다(LSTM 2.06, AR(30) 2.37). 판정은 미리 정한 규칙(검증 기준)대로 바꾸지 않습니다.

## 페이지에 들어 있는 것

- 쪽마다: 원래 대화를 살린 대화 노트, 페이지 안에서 직접 돌려 보는 계산(AR 적합, 롤링 예측, 작은 LSTM·MLP), 대결, 용어 말풍선, 확인 퀴즈(전체 178문항)
- 지식 색인: 개념 799개, 관계 1,126개 (21쪽 합계)
- 온톨로지·서지 꾸러미: JSON-LD, Turtle, CSV, CSL-JSON, BibTeX, RIS
- 부마다 파이썬 코드(numpy·statsmodels·PyTorch) — 페이지의 숫자를 그대로 다시 만든다
- 장부 데이터는 설명용으로 만든 모형이며 실제 데이터가 아닙니다.

## 등장인물

| 이름 | 역할 |
|---|---|
| 박사 | 해설과 심판. 판정은 숫자대로 내린다 |
| 조수(하루) | 실험 진행과 숫자 발표. 판정은 하지 않는다 |
| 초파리 연구원 | 의심하는 쪽. 기준선과 검증부터 본다 |
| 주판봇 | 확신하는 쪽. 높은 숫자에 건다 |

## 파일 구성

| 파일 | 내용 |
|---|---|
| `index.html` | 첫 화면 (목차로 옮겨 감) |
| `00_index.html` | 목차, 장부 목록, 교사용 안내 |
| `00_answers.html` | 퀴즈 178문항 정답·풀이 (인쇄용) |
| `1_1_…html` ~ `3_7_…html` | 본문 21쪽 (그림이 모두 들어 있는 단일 파일) |
| `*.en.html` 등 | 외국어판 |
| `cover_manifest.json` | 표지·온톨로지·번역 현황 목록 |
| `docs/` | 쪽별 이미지 명세서, 표지 지시문(`COVER_PROMPTS_timeseries.md`), 지식 색인 등록분 |

로컬에서 볼 때는 HTML 파일을 브라우저로 바로 열면 됩니다.

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
- 캐릭터(박사 · 조수 하루 · 초파리 연구원 · 주판봇)의 이름·설정·그림은 저작권자 안상선에게 있으며 허락 없이 쓸 수 없습니다.

## 만든 도구

- 해설 대시보드: [ahnboat_lab_explainer](https://github.com/adminmrobo/ahnboat_lab_explainer) (ai-lab-explainer)
- 캐릭터 그림: [fruitfly-lab-expressions](https://github.com/adminmrobo/fruitfly-lab-expressions) (107ce63)
- 외국어판: 언어팩 VER1.1. 외국어판은 원어민 검수 전입니다.

---

<a id="en"></a>

# Time-Series Trilogy — ARIMA and LSTM

Is a 14-day lookback the same thing as a 14-day window? Looking through the same window, ARIMA searches for a weighted average while LSTM searches for combinations. Starting from how many days to look back and going all the way to hidden states, higher dimensions and the irony of the name "neural", this lab explainer dashboard follows the topic across 3 parts and 21 pages.

- Site: https://adminmrobo.github.io/timeseries-trilogy/index.en.html
- Contents: [00_index.en.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.en.html) · Quiz answers: [00_answers.en.html](https://adminmrobo.github.io/timeseries-trilogy/00_answers.en.html)
- Written by Ahn Sangsun (CEO, M-Robo Inc.) · Produced with AI assistance

## Language

Available as the Korean original and 6 translated editions.

- How to choose: use the language selector in the top menu.
- Automatic switching: when you open a Korean page and your browser language is supported, you are taken to that edition. Translated addresses open as they are.
- Add `?lang=en` (or another code) to an address to open that language directly. `?lang=ko` stays on the Korean edition.
- Translated files are named `name.langcode.html`. The language table is in the Korean section above.

## What you will learn

| Part | Topic | Pages | Duel result (validation 50-day MAE, ×10k won) |
|---|---|---|---|
| Part 1 | How many days to look back — lookback and window, splitting into training/validation/test, AR(14) step by step, all at once vs rolling, three runners 7·14·30, number of training samples | 1-1 – 1-7 | AR(14) 3.16 vs AR(30) 2.74 → AbaBot wins |
| Part 2 | Same window, different thinking — calculator vs reader, LSTM gates, weighted sum vs nonlinear combination, flat vs curved surface, representation learning, feature engineering | 2-1 – 2-7 | AR 2.89 vs LSTM 0.82 → AbaBot wins |
| Part 3 | Hidden states, higher dimensions and the irony of "neural" — HMM and LSTM, the kernel trick, baselines first, capacity and search, overfitting and restraint, the connectome | 3-1 – 3-7 | AR 3.08 vs LSTM 2.97 → draw (within 5%) |

At the end of Part 3 the sealed 50-day test set is opened once (LSTM 2.06, AR(30) 2.37). The verdict follows the rule fixed in advance (validation) and is not changed.

## What the pages contain

- On every page: dialogue notes that keep the original conversation, calculations you run in the page (AR fitting, rolling forecasts, a small LSTM and MLP), a duel, term tooltips, and check quizzes (178 questions in total)
- Knowledge index: 799 concepts, 1,126 relations (across 21 pages)
- Ontology and bibliography package: JSON-LD, Turtle, CSV, CSL-JSON, BibTeX, RIS
- Python code for each part (numpy, statsmodels, PyTorch) that reproduces the numbers on the pages
- The ledger data is an illustrative model, not real data.

## Characters

| Name | Role |
|---|---|
| Professor | Explains and judges. Verdicts follow the numbers |
| Assistant (Haru) | Runs the experiments and announces the numbers. Does not judge |
| Fruit Fly Researcher | The skeptic. Checks baselines and validation first |
| AbaBot | The confident one. Bets on bigger numbers |

## Files

| File | Contents |
|---|---|
| `index.html` | Entry page (redirects to the contents) |
| `00_index.html` | Contents, ledger catalog, teacher notes |
| `00_answers.html` | Answers and explanations for all 178 quiz questions (printable) |
| `1_1_…html` – `3_7_…html` | 21 main pages (single files with all images embedded) |
| `*.en.html` etc. | Translated editions |
| `cover_manifest.json` | Status list of covers, ontology and translations |
| `docs/` | Image specs per page, cover prompts (`COVER_PROMPTS_timeseries.md`), knowledge index registry |

To view locally, open the HTML files directly in a browser. References are listed in the Korean section above.

## License

- Text: [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)
- The names, settings and artwork of the characters (Professor · Assistant Haru · Fruit Fly Researcher · AbaBot) belong to the copyright holder, Ahn Sangsun, and may not be used without permission.

## Tools

- Explainer dashboard: [ahnboat_lab_explainer](https://github.com/adminmrobo/ahnboat_lab_explainer) (ai-lab-explainer)
- Character art: [fruitfly-lab-expressions](https://github.com/adminmrobo/fruitfly-lab-expressions) (107ce63)
- Translations: language pack VER1.1. The translated editions have not yet been reviewed by native speakers.

---

<a id="zh"></a>

# 时间序列三部曲 — ARIMA 与 LSTM

回看 14 天的 lookback 和 14 天的 window 是一回事吗？看着同一个窗口，ARIMA 寻找的是加权平均，LSTM 寻找的是组合。从"该回看几天"出发，一直讲到隐藏状态、高维，以及"神经"这个名字的反讽——这是一套分 3 部、共 21 页的研究室讲解仪表板。

- 网站：https://adminmrobo.github.io/timeseries-trilogy/index.zh.html
- 目录：[00_index.zh.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.zh.html) · 小测验答案：[00_answers.zh.html](https://adminmrobo.github.io/timeseries-trilogy/00_answers.zh.html)
- 文 · Ahn Sangsun（M-Robo 公司 代表）· AI 辅助制作

## 语言

提供韩语原版和 6 种外语版。

- 选择方法：使用页面顶部菜单中的语言选择框。
- 自动切换：打开韩语页面时，如果浏览器语言是支持的语言，会自动转到该语言版。直接打开译本地址时按原样显示。
- 在地址末尾加上 `?lang=zh` 等，即可直接打开该语言。`?lang=ko` 会停留在韩语版。
- 外语版文件名为 `名称.语言代码.html`。语言表见上方韩语部分。

## 学什么

| 部 | 主题 | 页 | 对决结果（验证 50 天 MAE，万韩元） |
|---|---|---|---|
| 第 1 部 | 该回看几天 — lookback 与 window、训练·验证·测试划分、AR(14) 一步步来、一次性 vs 滚动、三位选手 7·14·30、训练样本数 | 1-1 ~ 1-7 | AR(14) 3.16 vs AR(30) 2.74 → 算盘宝胜 |
| 第 2 部 | 同一个窗口，不同的思考 — 计算器型 vs 阅读型、LSTM 的门、加权和 vs 非线性组合、平面 vs 弯曲的面、表示学习、特征工程 | 2-1 ~ 2-7 | AR 2.89 vs LSTM 0.82 → 算盘宝胜 |
| 第 3 部 | 隐藏状态、高维，以及"神经"的反讽 — HMM 与 LSTM、核技巧、先立基线、模型容量与搜索、过拟合与克制、连接组 | 3-1 ~ 3-7 | AR 3.08 vs LSTM 2.97 → 平局（差距 5% 以内） |

第 3 部最后只打开一次封存的 50 天测试集（LSTM 2.06，AR(30) 2.37）。判定按事先定好的规则（以验证集为准），不做更改。

## 页面内容

- 每页都有：保留原对话的对话笔记、在页面里直接运行的计算（AR 拟合、滚动预测、小型 LSTM 与 MLP）、对决、术语提示、小测验（共 178 题）
- 知识索引：概念 799 个、关系 1,126 个（21 页合计）
- 本体与文献资料包：JSON-LD、Turtle、CSV、CSL-JSON、BibTeX、RIS
- 每部附有 Python 代码（numpy、statsmodels、PyTorch），可重现页面上的数字
- 账本数据是为讲解而做的示意模型，不是真实数据。

## 登场人物

| 名字 | 角色 |
|---|---|
| 博士 | 讲解与裁判。按数字判定 |
| 助手（Haru） | 推进实验、公布数字。不做判定 |
| 果蝇研究员 | 怀疑的一方。先看基线和验证 |
| 算盘宝 | 自信的一方。押注更高的数字 |

## 文件结构

| 文件 | 内容 |
|---|---|
| `index.html` | 首页（跳转到目录） |
| `00_index.html` | 目录、账本列表、教师指南 |
| `00_answers.html` | 178 道小测验的答案与解析（可打印） |
| `1_1_…html` ~ `3_7_…html` | 正文 21 页（图片全部内嵌的单文件） |
| `*.zh.html` 等 | 外语版 |
| `cover_manifest.json` | 封面·本体·翻译现状清单 |
| `docs/` | 各页图像规格书、封面提示词（`COVER_PROMPTS_timeseries.md`）、知识索引登记 |

本地查看时，直接用浏览器打开 HTML 文件即可。参考文献见上方韩语部分。

## 许可

- 文字：[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)
- 角色（博士 · 助手 Haru · 果蝇研究员 · 算盘宝）的名称、设定和图画的著作权属于 Ahn Sangsun，未经许可不得使用。

## 制作工具

- 讲解仪表板：[ahnboat_lab_explainer](https://github.com/adminmrobo/ahnboat_lab_explainer)（ai-lab-explainer）
- 角色图：[fruitfly-lab-expressions](https://github.com/adminmrobo/fruitfly-lab-expressions)（107ce63）
- 外语版：语言包 VER1.1。外语版尚未经过母语者审校。

---

<a id="ja"></a>

# 時系列三部作 — ARIMA と LSTM

14日の lookback と 14日の window は同じものでしょうか。同じ窓を見ていても、ARIMA は加重平均を、LSTM は組み合わせを探します。何日さかのぼるかから始めて、隠れ状態、高次元、そして「ニューラル」という名前の皮肉まで、3部21ページでたどる研究室の解説ダッシュボードです。

- サイト：https://adminmrobo.github.io/timeseries-trilogy/index.ja.html
- 目次：[00_index.ja.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.ja.html) · クイズ解答集：[00_answers.ja.html](https://adminmrobo.github.io/timeseries-trilogy/00_answers.ja.html)
- 文 · Ahn Sangsun（M-Robo Inc. 代表）· AI 支援制作

## 言語

韓国語の原本と 6 つの外国語版で読めます。

- 選び方：画面最上部のメニューにある言語選択ボックスから選びます。
- 自動切り替え：韓国語のページを開いたとき、ブラウザの言語が対応言語ならその言語版に移ります。翻訳版のアドレスから開いた場合はそのまま表示します。
- アドレスの末尾に `?lang=ja` のように付けると、その言語で直接開きます。`?lang=ko` は韓国語版のままです。
- 外国語版のファイル名は `名前.言語コード.html` です。言語の表は上の韓国語セクションにあります。

## 学ぶこと

| 部 | テーマ | ページ | 対決の結果（検証 50日 MAE、万ウォン） |
|---|---|---|---|
| 第1部 | 何日さかのぼるか — lookback と window、訓練・検証・テストの分け方、AR(14) を一歩ずつ、一度に vs 転がしながら、三人のランナー 7・14・30、学習サンプルの数 | 1-1 〜 1-7 | AR(14) 3.16 vs AR(30) 2.74 → アバボットの勝ち |
| 第2部 | 同じ窓、違う考え方 — 計算機型 対 読書型、LSTM のゲート、加重和 対 非線形の組み合わせ、平らな面 対 曲がった面、表現学習、特徴量エンジニアリング | 2-1 〜 2-7 | AR 2.89 vs LSTM 0.82 → アバボットの勝ち |
| 第3部 | 隠れ状態、高次元、そして「ニューラル」の皮肉 — HMM と LSTM、カーネルトリック、まずベースライン、表現力と探索、過学習と節制、コネクトーム | 3-1 〜 3-7 | AR 3.08 vs LSTM 2.97 → 引き分け（差は 5% 以内） |

第3部の最後に、封印しておいたテスト 50日を一度だけ開けます（LSTM 2.06、AR(30) 2.37）。判定は前もって決めたルール（検証基準）のとおりで、変えません。

## ページに入っているもの

- 各ページに：元の対話を生かした対話ノート、ページの中で実際に動かす計算（AR の当てはめ、ローリング予測、小さな LSTM・MLP）、対決、用語の吹き出し、確認クイズ（全 178 問）
- 知識インデックス：概念 799 個、関係 1,126 個（21 ページの合計）
- オントロジー・書誌パッケージ：JSON-LD、Turtle、CSV、CSL-JSON、BibTeX、RIS
- 部ごとの Python コード（numpy・statsmodels・PyTorch）— ページの数字をそのまま再現します
- 帳簿のデータは説明用に作ったモデルで、実データではありません。

## 登場人物

| 名前 | 役割 |
|---|---|
| 博士 | 解説と審判。判定は数字どおりに下します |
| 助手（Haru） | 実験の進行と数字の発表。判定はしません |
| ショウジョウバエ研究員 | 疑う側。まずベースラインと検証を見ます |
| アバボット | 自信満々の側。大きな数字に賭けます |

## ファイル構成

| ファイル | 内容 |
|---|---|
| `index.html` | 最初の画面（目次へ移ります） |
| `00_index.html` | 目次、帳簿一覧、教員向け案内 |
| `00_answers.html` | クイズ 178 問の解答と解説（印刷用） |
| `1_1_…html` 〜 `3_7_…html` | 本文 21 ページ（画像をすべて含む単一ファイル） |
| `*.ja.html` など | 外国語版 |
| `cover_manifest.json` | 表紙・オントロジー・翻訳の状況一覧 |
| `docs/` | ページごとの画像仕様書、表紙の指示文（`COVER_PROMPTS_timeseries.md`）、知識インデックスの登録分 |

ローカルで見るときは、HTML ファイルをブラウザでそのまま開いてください。参考文献は上の韓国語セクションにあります。

## ライセンス

- 文章：[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)
- キャラクター（博士 · 助手 Haru · ショウジョウバエ研究員 · アバボット）の名前・設定・絵の著作権は Ahn Sangsun にあり、許可なく使うことはできません。

## 制作ツール

- 解説ダッシュボード：[ahnboat_lab_explainer](https://github.com/adminmrobo/ahnboat_lab_explainer)（ai-lab-explainer）
- キャラクターの絵：[fruitfly-lab-expressions](https://github.com/adminmrobo/fruitfly-lab-expressions)（107ce63）
- 外国語版：言語パック VER1.1。外国語版はネイティブによる校閲前です。

---

<a id="uz"></a>

# Vaqt qatorlari trilogiyasi — ARIMA va LSTM

14 kunlik lookback bilan 14 kunlik window bir narsami? Bir xil oynaga qarab, ARIMA vaznli oʻrtachani, LSTM esa kombinatsiyalarni izlaydi. Necha kun orqaga qarash kerakligidan boshlab, yashirin holatlar, yuqori oʻlchamlar va „neyron“ nomining kinoyasigacha — 3 qism, 21 sahifadan iborat laboratoriya tushuntirish paneli.

- Sayt: https://adminmrobo.github.io/timeseries-trilogy/index.uz.html
- Mundarija: [00_index.uz.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.uz.html) · Test javoblari: [00_answers.uz.html](https://adminmrobo.github.io/timeseries-trilogy/00_answers.uz.html)
- Muallif · Ahn Sangsun (M-Robo Inc. bosh direktori) · SI yordamida tayyorlangan

## Til

Koreyscha asl nusxa va 6 ta tarjima mavjud.

- Tanlash: ekranning eng yuqorisidagi menyuda til tanlash qutisidan foydalaning.
- Avtomatik oʻtish: koreyscha sahifani ochganingizda brauzer tili qoʻllab-quvvatlansa, oʻsha til nusxasiga oʻtadi. Tarjima manzili orqali ochilsa, oʻzgarishsiz ochiladi.
- Manzil oxiriga `?lang=uz` kabi qoʻshsangiz, oʻsha til bevosita ochiladi. `?lang=ko` koreyscha nusxada qoladi.
- Tarjima fayllari `nom.tilkodi.html` koʻrinishida. Tillar jadvali yuqoridagi koreyscha boʻlimda.

## Nimani oʻrganasiz

| Qism | Mavzu | Sahifalar | Bellashuv natijasi (validatsiya 50 kun MAE, ×10 ming von) |
|---|---|---|---|
| 1-qism | Necha kun orqaga qarash kerak — lookback va window, oʻqitish·validatsiya·test boʻlish, AR(14) qadamma-qadam, bir yoʻla yoki sirpantirib, uch yuguruvchi 7·14·30, oʻquv namunalari soni | 1-1 – 1-7 | AR(14) 3.16 va AR(30) 2.74 → AbaBot yutdi |
| 2-qism | Bir oyna, turli fikrlash — kalkulyator turi va oʻquvchi turi, LSTM darvozalari, vaznli yigʻindi va nochiziqli kombinatsiya, tekis va egri sirt, tasvirlarni oʻrganish, belgilar muhandisligi | 2-1 – 2-7 | AR 2.89 va LSTM 0.82 → AbaBot yutdi |
| 3-qism | Yashirin holatlar, yuqori oʻlchamlar va „neyron“ kinoyasi — HMM va LSTM, yadro hiylasi, avval bazaviy model, model sigʻimi va qidiruv, ortiqcha moslashish va cheklash, konnektom | 3-1 – 3-7 | AR 3.08 va LSTM 2.97 → durang (farq 5% ichida) |

3-qism oxirida muhrlangan 50 kunlik test toʻplami faqat bir marta ochiladi (LSTM 2.06, AR(30) 2.37). Hukm oldindan belgilangan qoidaga (validatsiya boʻyicha) koʻra chiqariladi va oʻzgartirilmaydi.

## Sahifalarda nima bor

- Har bir sahifada: asl suhbatni saqlagan suhbat qaydlari, sahifaning oʻzida bajariladigan hisob-kitoblar (AR moslash, sirpanuvchi prognoz, kichik LSTM va MLP), bellashuv, atama izohlari, tekshiruv testlari (jami 178 savol)
- Bilimlar indeksi: 799 tushuncha, 1 126 bogʻlanish (21 sahifa boʻyicha)
- Ontologiya va bibliografiya toʻplami: JSON-LD, Turtle, CSV, CSL-JSON, BibTeX, RIS
- Har bir qism uchun Python kodi (numpy, statsmodels, PyTorch) — sahifadagi raqamlarni aynan qayta hosil qiladi
- Daftar maʼlumotlari tushuntirish uchun tuzilgan model, haqiqiy maʼlumot emas.

## Qahramonlar

| Ism | Vazifa |
|---|---|
| Professor | Tushuntiradi va hakamlik qiladi. Hukm raqamlarga qarab chiqariladi |
| Yordamchi (Haru) | Tajribani olib boradi va raqamlarni eʼlon qiladi. Hukm chiqarmaydi |
| Meva pashshasi tadqiqotchi | Shubhalanuvchi tomon. Avval bazaviy model va validatsiyani tekshiradi |
| AbaBot | Ishonchli tomon. Kattaroq raqamga tikadi |

## Fayllar

| Fayl | Mazmuni |
|---|---|
| `index.html` | Bosh sahifa (mundarijaga oʻtadi) |
| `00_index.html` | Mundarija, daftarlar roʻyxati, oʻqituvchi uchun yoʻriqnoma |
| `00_answers.html` | 178 ta test savolining javoblari va tahlili (chop etish uchun) |
| `1_1_…html` – `3_7_…html` | Asosiy 21 sahifa (barcha rasmlar ichida boʻlgan yagona fayllar) |
| `*.uz.html` va boshqalar | Tarjima nusxalari |
| `cover_manifest.json` | Muqova, ontologiya va tarjima holati roʻyxati |
| `docs/` | Sahifalar boʻyicha rasm spetsifikatsiyalari, muqova koʻrsatmalari (`COVER_PROMPTS_timeseries.md`), bilimlar indeksi roʻyxati |

Kompyuterda koʻrish uchun HTML faylni brauzerda toʻgʻridan-toʻgʻri oching. Adabiyotlar roʻyxati yuqoridagi koreyscha boʻlimda.

## Litsenziya

- Matn: [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)
- Qahramonlar (Professor · Yordamchi Haru · Meva pashshasi tadqiqotchi · AbaBot) nomlari, tavsiflari va rasmlariga mualliflik huquqi Ahn Sangsunga tegishli; ruxsatsiz foydalanish mumkin emas.

## Vositalar

- Tushuntirish paneli: [ahnboat_lab_explainer](https://github.com/adminmrobo/ahnboat_lab_explainer) (ai-lab-explainer)
- Qahramon rasmlari: [fruitfly-lab-expressions](https://github.com/adminmrobo/fruitfly-lab-expressions) (107ce63)
- Tarjimalar: til paketi VER1.1. Tarjimalar hali ona tilida soʻzlashuvchilar tomonidan tekshirilmagan.

---

<a id="ru"></a>

# Трилогия о временных рядах — ARIMA и LSTM

Ретроспектива (lookback) в 14 дней и окно (window) в 14 дней — это одно и то же? Глядя в одно и то же окно, ARIMA ищет взвешенное среднее, а LSTM — комбинации. От вопроса «на сколько дней оглядываться» до скрытых состояний, высоких размерностей и иронии названия «нейронный» — учебная панель лаборатории из 3 частей и 21 страницы.

- Сайт: https://adminmrobo.github.io/timeseries-trilogy/index.ru.html
- Оглавление: [00_index.ru.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.ru.html) · Ответы к тестам: [00_answers.ru.html](https://adminmrobo.github.io/timeseries-trilogy/00_answers.ru.html)
- Автор · Ahn Sangsun (генеральный директор M-Robo Inc.) · Подготовлено с помощью ИИ

## Язык

Доступны корейский оригинал и 6 переводов.

- Как выбрать: в списке выбора языка в верхнем меню страницы.
- Автоматическое переключение: если вы открываете корейскую страницу и язык браузера поддерживается, откроется версия на этом языке. Адреса переводов открываются как есть.
- Добавьте к адресу `?lang=ru` (или другой код), чтобы сразу открыть нужный язык. `?lang=ko` оставляет корейскую версию.
- Файлы переводов называются `имя.кодязыка.html`. Таблица языков — в корейском разделе выше.

## Чему вы научитесь

| Часть | Тема | Страницы | Итог поединка (MAE на валидации 50 дней, ×10 тыс. вон) |
|---|---|---|---|
| Часть 1 | На сколько дней оглядываться — lookback и window, деление на обучение/валидацию/тест, AR(14) шаг за шагом, сразу или по шагам, три бегуна 7·14·30, число обучающих примеров | 1-1 – 1-7 | AR(14) 3.16 vs AR(30) 2.74 → победа АбаБот |
| Часть 2 | Одно окно, разное мышление — калькулятор vs читатель, вентили LSTM, взвешенная сумма vs нелинейная комбинация, плоская vs изогнутая поверхность, обучение представлений, конструирование признаков | 2-1 – 2-7 | AR 2.89 vs LSTM 0.82 → победа АбаБот |
| Часть 3 | Скрытые состояния, высокие размерности и ирония «нейронного» — HMM и LSTM, ядерный трюк, сначала базовая модель, ёмкость модели и поиск, переобучение и сдержанность, коннектом | 3-1 – 3-7 | AR 3.08 vs LSTM 2.97 → ничья (разница в пределах 5%) |

В конце части 3 запечатанная тестовая выборка из 50 дней открывается один раз (LSTM 2.06, AR(30) 2.37). Вердикт выносится по заранее заданному правилу (по валидации) и не меняется.

## Что есть на страницах

- На каждой странице: заметки к диалогу, сохраняющие исходный разговор, вычисления прямо на странице (подгонка AR, скользящий прогноз, небольшие LSTM и MLP), поединок, подсказки к терминам, проверочные тесты (всего 178 вопросов)
- Указатель знаний: 799 понятий, 1 126 связей (по 21 странице)
- Пакет онтологии и библиографии: JSON-LD, Turtle, CSV, CSL-JSON, BibTeX, RIS
- Код на Python для каждой части (numpy, statsmodels, PyTorch), воспроизводящий числа со страниц
- Данные журнала продаж — учебная модель, а не реальные данные.

## Персонажи

| Имя | Роль |
|---|---|
| Профессор | Объясняет и судит. Вердикт — по числам |
| Ассистент (Хару) | Ведёт эксперименты и объявляет числа. Не судит |
| Исследователь Дрозофила | Скептик. Сначала проверяет базовую модель и валидацию |
| АбаБот | Уверенный. Ставит на большие числа |

## Файлы

| Файл | Содержание |
|---|---|
| `index.html` | Стартовая страница (переход к оглавлению) |
| `00_index.html` | Оглавление, список журналов, памятка для преподавателя |
| `00_answers.html` | Ответы и разбор всех 178 вопросов (для печати) |
| `1_1_…html` – `3_7_…html` | 21 основная страница (единые файлы со всеми рисунками внутри) |
| `*.ru.html` и др. | Переводы |
| `cover_manifest.json` | Список состояния обложек, онтологии и переводов |
| `docs/` | Спецификации изображений по страницам, указания для обложек (`COVER_PROMPTS_timeseries.md`), реестр указателя знаний |

Чтобы смотреть локально, откройте HTML-файлы прямо в браузере. Список литературы — в корейском разделе выше.

## Лицензия

- Текст: [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)
- Имена, описания и рисунки персонажей (Профессор · Ассистент Хару · Исследователь Дрозофила · АбаБот) принадлежат правообладателю Ahn Sangsun; использование без разрешения запрещено.

## Инструменты

- Учебная панель: [ahnboat_lab_explainer](https://github.com/adminmrobo/ahnboat_lab_explainer) (ai-lab-explainer)
- Рисунки персонажей: [fruitfly-lab-expressions](https://github.com/adminmrobo/fruitfly-lab-expressions) (107ce63)
- Переводы: языковой пакет VER1.1. Переводы ещё не проверены носителями языка.

---

<a id="vi"></a>

# Bộ ba chuỗi thời gian — ARIMA và LSTM

Lookback 14 ngày và window 14 ngày có phải là một? Cùng nhìn qua một cửa sổ, ARIMA tìm trung bình có trọng số, còn LSTM tìm các tổ hợp. Bắt đầu từ câu hỏi nên nhìn lại bao nhiêu ngày, đi đến trạng thái ẩn, nhiều chiều và nghịch lý của cái tên “nơ-ron” — bảng điều khiển giải thích của phòng thí nghiệm gồm 3 phần, 21 trang.

- Trang web: https://adminmrobo.github.io/timeseries-trilogy/index.vi.html
- Mục lục: [00_index.vi.html](https://adminmrobo.github.io/timeseries-trilogy/00_index.vi.html) · Đáp án câu đố: [00_answers.vi.html](https://adminmrobo.github.io/timeseries-trilogy/00_answers.vi.html)
- Tác giả · Ahn Sangsun (CEO, M-Robo Inc.) · Thực hiện với sự hỗ trợ của AI

## Ngôn ngữ

Có bản gốc tiếng Hàn và 6 bản dịch.

- Cách chọn: dùng hộp chọn ngôn ngữ ở menu trên cùng của trang.
- Tự động chuyển: khi bạn mở trang tiếng Hàn và ngôn ngữ trình duyệt được hỗ trợ, trang sẽ chuyển sang bản ngôn ngữ đó. Mở bằng địa chỉ bản dịch thì giữ nguyên.
- Thêm `?lang=vi` (hoặc mã khác) vào cuối địa chỉ để mở thẳng ngôn ngữ đó. `?lang=ko` giữ ở bản tiếng Hàn.
- Tệp bản dịch có dạng `tên.mãngônngữ.html`. Bảng ngôn ngữ nằm ở phần tiếng Hàn phía trên.

## Bạn sẽ học gì

| Phần | Chủ đề | Trang | Kết quả cuộc đấu (MAE kiểm định 50 ngày, ×10 nghìn won) |
|---|---|---|---|
| Phần 1 | Nhìn lại bao nhiêu ngày — lookback và window, chia huấn luyện·kiểm định·kiểm tra, AR(14) từng bước một, một lần vs cuốn chiếu, ba vận động viên 7·14·30, số mẫu huấn luyện | 1-1 – 1-7 | AR(14) 3.16 vs AR(30) 2.74 → AbaBot thắng |
| Phần 2 | Cùng một cửa sổ, cách nghĩ khác nhau — kiểu máy tính vs kiểu đọc sách, các cổng LSTM, tổng có trọng số vs tổ hợp phi tuyến, mặt phẳng vs mặt cong, học biểu diễn, kỹ thuật đặc trưng | 2-1 – 2-7 | AR 2.89 vs LSTM 0.82 → AbaBot thắng |
| Phần 3 | Trạng thái ẩn, nhiều chiều và nghịch lý của “nơ-ron” — HMM và LSTM, thủ thuật hạt nhân, mô hình cơ sở trước tiên, năng lực mô hình và tìm kiếm, quá khớp và sự tiết chế, connectome | 3-1 – 3-7 | AR 3.08 vs LSTM 2.97 → hòa (chênh lệch trong 5%) |

Cuối phần 3, tập kiểm tra 50 ngày được niêm phong sẽ được mở đúng một lần (LSTM 2.06, AR(30) 2.37). Phán quyết theo quy tắc đã định trước (dựa trên kiểm định) và không thay đổi.

## Trang có gì

- Mỗi trang có: ghi chú hội thoại giữ nguyên cuộc trò chuyện gốc, các phép tính chạy ngay trong trang (khớp AR, dự báo cuốn chiếu, LSTM và MLP nhỏ), cuộc đấu, chú thích thuật ngữ, câu đố kiểm tra (tổng cộng 178 câu)
- Chỉ mục kiến thức: 799 khái niệm, 1.126 quan hệ (trên 21 trang)
- Gói bản thể học & thư mục: JSON-LD, Turtle, CSV, CSL-JSON, BibTeX, RIS
- Mã Python cho từng phần (numpy, statsmodels, PyTorch) tái tạo đúng các con số trên trang
- Dữ liệu sổ sách là mô hình minh họa, không phải dữ liệu thật.

## Nhân vật

| Tên | Vai trò |
|---|---|
| Giáo sư | Giải thích và làm trọng tài. Phán quyết theo con số |
| Trợ lý (Haru) | Tiến hành thí nghiệm và công bố con số. Không phán quyết |
| Nhà nghiên cứu Ruồi giấm | Bên hoài nghi. Xem mô hình cơ sở và kiểm định trước |
| AbaBot | Bên tự tin. Đặt cược vào con số lớn hơn |

## Cấu trúc tệp

| Tệp | Nội dung |
|---|---|
| `index.html` | Trang đầu (chuyển đến mục lục) |
| `00_index.html` | Mục lục, danh sách sổ sách, hướng dẫn cho giáo viên |
| `00_answers.html` | Đáp án và lời giải cho 178 câu đố (để in) |
| `1_1_…html` – `3_7_…html` | 21 trang nội dung (tệp đơn chứa toàn bộ hình ảnh) |
| `*.vi.html` v.v. | Các bản dịch |
| `cover_manifest.json` | Danh sách tình trạng ảnh bìa, bản thể học và bản dịch |
| `docs/` | Bản đặc tả hình ảnh từng trang, chỉ dẫn ảnh bìa (`COVER_PROMPTS_timeseries.md`), bản đăng ký chỉ mục kiến thức |

Để xem trên máy, chỉ cần mở tệp HTML bằng trình duyệt. Tài liệu tham khảo nằm ở phần tiếng Hàn phía trên.

## Giấy phép

- Văn bản: [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)
- Tên, thiết lập và hình vẽ các nhân vật (Giáo sư · Trợ lý Haru · Nhà nghiên cứu Ruồi giấm · AbaBot) thuộc quyền tác giả của Ahn Sangsun; không được sử dụng khi chưa được phép.

## Công cụ

- Bảng giải thích: [ahnboat_lab_explainer](https://github.com/adminmrobo/ahnboat_lab_explainer) (ai-lab-explainer)
- Hình nhân vật: [fruitfly-lab-expressions](https://github.com/adminmrobo/fruitfly-lab-expressions) (107ce63)
- Bản dịch: gói ngôn ngữ VER1.1. Các bản dịch chưa được người bản ngữ hiệu đính.
