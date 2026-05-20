# Google公式｜生成AI検索 最適化ガイド（ナレッジ版）

> **出典**: [Optimizing your website for generative AI features on Google Search](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide)
> 取得日: 2026-05-20 / 原文最終更新: 2026-05-15 UTC
> 関連公式: Search Essentials / Helpful Content / Spam Policies / AI Features / Using Gen AI Content / Technical Requirements

---

## TL;DR（30秒で押さえる結論）

1. **AI検索向けの「特別な最適化」は存在しない**。AI Overviews / AI Mode はGoogle検索のコアランキング・品質システムを土台にしているため、**従来のSEOベストプラクティスがそのままAI最適化になる**。
2. **llms.txt・AI専用マークアップ・Markdown化・コンテンツの細切れ化（チャンキング）は不要**。GoogleはそれらをAI用に特別扱いしない。
3. **やるべきは「独自の経験・専門知識を持った非汎用コンテンツ」と「クローラブルで素直なHTML」**。E-E-A-T と Who/How/Why を満たすこと。
4. **AI機能に出るための前提**は「インデックスされている」「スニペット表示の対象である」「Search技術要件を満たしている」の3つ。
5. **構造化データはAI機能の必須要件ではない**。ただしリッチリザルト等のためには引き続き有効。
6. **「ウェブ上での不自然なメンション獲得」は効果がないどころかスパム判定リスク**。
7. **AI生成コンテンツは禁止ではないが、ユーザー価値ゼロの量産はスパム**（Scaled Content Abuse）。生成過程の開示が推奨。

---

## 1. 結論：AI検索向けのSEOは「依然としてSEO」

Google公式の見解：

> "Yes! The best practices for SEO continue to be relevant because our generative AI features on Google Search are rooted in our core Search ranking and quality systems."

- AEO（Answer Engine Optimization）/ GEO（Generative Engine Optimization）という別概念で語られがちだが、**Googleの立場では「AI検索向け最適化＝検索体験への最適化＝SEO」と同じ**。
- 表示順位を決めているのは依然としてコアランキングシステム＋スパムフィルタ。

### AI検索の裏側の仕組み

| 仕組み | 役割 |
|---|---|
| **RAG (Retrieval-Augmented Generation / Grounding)** | 検索インデックスから関連性の高い最新ページを取得し、AI応答の品質・正確性・鮮度を担保。応答には目立つクリック可能リンクを表示。 |
| **Query fan-out** | ユーザーのクエリから関連クエリを並列生成し、追加情報を取得（例：「芝生の除草」→「除草剤」「化学薬品なし除草」「予防」など）。**個別ロングテール対策よりも、トピックを総合的にカバーするコンテンツ**が有利。 |

---

## 2. やるべきこと（Do）

### 2-1. 価値ある「非汎用（non-commodity）」コンテンツを作る

#### 非汎用コンテンツとは
- **悪い例（汎用）**: 「初めてのホームバイヤーのための7つのヒント」
- **良い例（非汎用）**: 「検査を免除して費用削減：下水管路を詳しく見る」
- 一般常識を超え、**専門家ないし実体験者ならではの独自視点**を提供しているか。

#### 必須要素
- ✅ 第一人称・実体験に基づくレビュー、独自の調査・分析
- ✅ 読みやすい段落・セクション・見出し構造
- ✅ 関連性ある高品質な画像・動画（画像/動画SEOに沿えばAIにも反映される）
- ✅ ユーザーが「満足した」と感じる読後感

#### NGパターン
- ❌ 他サイトの要約や言い換えだけ
- ❌ クエリバリエーション全部に個別ページを量産（→ Scaled Content Abuse）
- ❌ 検索流入が主目的のコンテンツ（"search engine-first"）

### 2-2. 技術構造をクリーンに保つ

#### 最低限の技術要件（Search Essentials Technical）
1. **Googlebotがブロックされていない**（robots.txt / 認証ページではない）
2. **HTTP 200 で正常応答する**
3. **インデックス対応のファイル形式で、テキストコンテンツがある**

> ⚠ これらを満たしても**インデックスは保証されない**。最低要件であって十分条件ではない。

#### ベストプラクティス
- セマンティックHTMLを使う（必須ではないがスクリーンリーダー含むアクセシビリティに寄与）
- JavaScriptはブロックしなければGoogleが処理可能。ただしフレームワーク使用時はJavaScript SEOガイドに従う
- Core Web Vitals / ページ体験を整備
- 重複コンテンツを減らす（クロール予算の浪費＆UX低下）
- Search Consoleで検証

### 2-3. ローカル/EC情報の最適化
- Google Business Profile / Merchant Center を整備
- 商品データ・店舗情報をフィードで送る
- 将来的に Business Agent（会話型）にも反映される

---

## 3. やってはいけないこと（Don't / Mythbusting）

Google公式が明確に否定している"AIOハック"の一覧。

| 都市伝説 | Google公式見解 |
|---|---|
| `llms.txt` を置けばAIに優遇される | ❌ 不要。Googleは特別扱いしない |
| AI向けの専用Markdownファイルやマークアップ | ❌ 不要 |
| コンテンツを細かくチャンキングする必要がある | ❌ "Google systems are able to understand the nuance of multiple topics on a page" |
| AI向けの特定の文体・書き方が必要 | ❌ AIは同義語・意図を理解する |
| ロングテール・クエリのバリエーションを網羅 | ❌ 不要 |
| Web全体での「メンション数」を増やす | ❌ "inauthentic mentions" は無意味どころかスパム扱いリスク |
| 構造化データがAI機能に必須 | ❌ 必須ではない（リッチリザルト等には依然有効） |
| 特定の文字数・ページ長が推奨される | ❌ そのような推奨はない |

---

## 4. AI機能の表示資格と制御

### 4-1. 表示対象になる条件
- ページがインデックス済み
- スニペット表示の対象である
- Search技術要件を満たしている

→ **追加要件ゼロ**。既に通常検索で出ているページは、すでにAI機能の表示候補。

### 4-2. AI機能への表示を制御するメタタグ
| 指令 | 用途 |
|---|---|
| `nosnippet` | **テキストスニペットおよびビデオプレビューを非表示**。公式表現："will also prevent the content from being used as a direct input for AI Overviews and AI Mode" → **AI Overviews / AI Mode の入力からも除外される** |
| `data-nosnippet` | `<span>` `<div>` `<section>` に付与し、ページ内の特定箇所だけスニペット／AI機能の入力から除外（JS動的付与は非推奨：不確実性） |
| `max-snippet:[n]` | スニペット最大文字数を制限。低い値ほど Featured Snippets / AI Overviews の対象になりにくい |
| `max-image-preview:[none\|standard\|large]` | 画像プレビューサイズ制御 |
| `max-video-preview:[n]` | 動画プレビュー最大秒数を制御 |
| `noindex` | インデックス自体を拒否（=AI機能にも出ない） |
| `indexifembedded` | `noindex` 併用時のみ意味あり。iframe等で他ページに埋め込まれた場合のインデックスを許可 |
| `notranslate` | 翻訳結果の非表示 |
| `robots.txt` の `User-agent: Googlebot` Disallow | クロール自体を拒否（=メタタグも読まれない） |

**`X-Robots-Tag` HTTPヘッダ**でも同じディレクティブが指定可能。非HTMLファイル（PDF・画像）の制御や、サーバー側で一括制御する場合に有効。

> ⚠ **robots.txt で Disallow したページのメタタグは読まれない**。「AIには出したくないが検索には出したい」場合は robots.txt ではなく `nosnippet` を使う。

### 4-3. Googleクローラの種類と AI関連の制御

| クローラ | User-agent トークン | 用途 | robots.txt 制御 |
|---|---|---|---|
| **Googlebot** | `Googlebot` | Google Search全般（Discover/Image/Video/News含む）。**AI Overviews / AI Mode もこれが取得した内容を使う** | `User-agent: Googlebot` |
| **Google-Extended** | `Google-Extended` | **Gemini Apps / Vertex AI API for Gemini の学習用**。検索のランキング信号にはならない | `User-agent: Google-Extended` |
| **GoogleOther** | `GoogleOther` | 内部R&D等の汎用クロール。特定製品に紐づかない | `User-agent: GoogleOther` |

#### 重要な区別
- **AI Overviews / AI Mode を出したくない** → `Googlebot` を Disallow するか `nosnippet` を使う（ただし Googlebot Disallow は検索結果からも消える）
- **Gemini系の学習からのみ除外したい** → `Google-Extended` のみ Disallow（検索には影響しない）
- **両方拒否したい** → 両方 Disallow

```txt
# 例：検索には出すが、Gemini系の学習データには使わせない
User-agent: Google-Extended
Disallow: /

User-agent: Googlebot
Allow: /
```

### 4-4. パフォーマンス計測
- Search Console「パフォーマンスレポート」の **Web検索タイプ** でAI機能由来のクリック・インプレッションを確認

---

## 5. コンテンツ品質の指針：Helpful, Reliable, People-First

### 5-1. 自己診断質問（コンテンツ品質）
- オリジナルな情報・調査・分析があるか
- 主題に対して実質的で包括的か
- 自明な範囲を超えた洞察があるか
- 他ソースを参照する場合、単なる引用ではなく付加価値を出しているか
- タイトル・H1が誇張やクリックベイトでなく的確な要約か
- ブックマーク・人に勧めたくなる質か
- 印刷雑誌・書籍に載るレベルか

### 5-2. 自己診断質問（専門性）
- 著者の背景情報や信頼性の根拠を示しているか
- 専門家または熱心な愛好家が書いた（チェックした）か
- 容易に検証可能な事実誤認がないか

### 5-3. People-First の判断軸
すべて「Yes」なら People-First：
- 想定オーディエンスが**直接訪問しても**有用と感じる
- **一次情報（実際に使った/行った）** に基づく
- サイトに主目的・フォーカスがある
- 読者が学び目標達成できる
- 満足体験を提供している

### 5-4. Search-Engine-First の警告サイン（一つでも該当したら見直し）
- 検索流入獲得が主目的
- トピックを乱発して一部が当たるのを期待
- 大規模自動化でコンテンツを量産
- 他者要約のみで付加価値が薄い
- トレンド追従のためだけに書いている
- 「Googleが特定の文字数を好む」と信じて書いている
- 専門性がないニッチに検索流入目的で参入
- 確定していない未来情報（リリース日など）を断定
- 内容を変えていないのに日付だけ更新する
- "フレッシュ性"演出のための大量加除

---

## 6. E-E-A-T と Who/How/Why

### 6-1. E-E-A-T（重要度順）
1. **Trustworthiness（信頼性）** ← 最重要
2. **Experience（経験）**
3. **Expertise（専門性）**
4. **Authoritativeness（権威性）**

> YMYL（Your Money or Your Life：健康・金融・安全・社会福祉）領域では E-E-A-T がより強く評価される。

### 6-2. Who / How / Why フレームワーク

#### Who（誰が作ったか）
- 著者バイラインを明示
- 著者プロフィール（経歴・所属）へのリンク

#### How（どう作ったか）
- レビューならテスト数・方法論・写真などの証拠を提示
- **AI/自動化を使った場合は開示する**（後述）

#### Why（なぜ作ったか）← もっとも重要
- 「人を助けるため」なら ✅
- 「検索順位を取るため」なら ❌（スパム判定リスク）

---

## 7. 生成AIコンテンツの扱い

### 7-1. 基本ルール
- **AI生成自体は禁止ではない**
- 「ユーザー価値を加える」AI活用は許容（リサーチ補助、構造化、表現の磨き上げ）
- **ユーザー価値なしの量産はスパム**（Scaled Content Abuse / Spam Policy違反）

### 7-2. 推奨される運用
- メタデータ（title/description/altテキスト）の精度を担保
- 構造化データの整合性を検証
- **AI使用を開示する**（特に画像・本文）
- AIをどう使ったか・なぜ有用かを文脈として示す

### 7-3. EC特有の追加要件（AI生成画像）
- IPTC `DigitalSourceType` メタデータ
- `TrainedAlgorithmicMedia` の指定
- AI生成テキスト（商品説明等）も明示的にラベル

---

## 8. スパムポリシー（AI最適化で踏み抜きやすい地雷）

AI最適化を装って踏みがちな違反パターンを抜粋。

| 類型 | 内容 | AIO文脈での典型例 |
|---|---|---|
| **Scaled Content Abuse** | ユーザー価値なき大量生成 | AIで無価値ページを量産、フィード/検索結果のスクレイピング自動変換 |
| **Site Reputation Abuse** | 既存ドメインの信用度を利用した第三者コンテンツ | 教育サイト下にペイデイローン記事、ニュースサイトに無関連クーポン |
| **Expired Domain Abuse** | 失効ドメインの転用 | 元政府ドメインにアフィリエイト掲載 |
| **Link Spam** | リンク売買・自動生成・対価リンク | 「メンション獲得」目的の有料記事、未開示ネイティブ広告 |
| **Cloaking / Sneaky Redirects** | Googleとユーザーに別物を見せる | UA判定で検索エンジンにだけ豪華なテキスト、ユーザーは別ドメイン転送 |
| **Hidden Text/Links** | 白背景白文字、画面外CSS、font-size:0 | AI向けに"見えないテキスト"を埋める |
| **Keyword Stuffing** | キーワード過剰詰め込み | クエリバリエーション網羅のための地域名・キーワード羅列 |
| **Doorway Abuse** | 微差サイト/ページの大量作成 | 地域別ファネリングサイトを大量生成 |
| **Thin Affiliation** | マーチャント説明のコピペアフィリエイト | 独自レビューなしでAmazon説明を流用 |
| **Misleading Functionality** | 実現しない機能を装う | 「無料○○ジェネレータ」と称して詐欺広告へ誘導 |

> ⚠ サイト全体の降格・除外に直結する。AI最適化を装った"裏技"はほぼここに引っかかる。

---

## 9. エージェント体験（Agentic Experiences）への備え

- AIエージェント = ユーザーの代わりに予約・比較などのタスクを実行する自律システム
- ブラウザエージェントは **スクリーンショット解析・DOM検査・アクセシビリティツリー** を使う
- セマンティックHTML / アクセシビリティ整備が将来的にエージェント可読性に効く
- 参考：
  - [Agent-friendly website best practices (web.dev)](https://web.dev/articles/ai-agent-site-ux)
  - [Universal Commerce Protocol (UCP)](https://ucp.dev/latest/)

---

## 9-A. Core Web Vitals（具体閾値）

ページ体験の中核指標。AI機能の表示資格に直接の閾値要件はないが、**コアランキング要因に含まれる**ためコンテンツ競合時に効く。

| 指標 | 何を測るか | 推奨閾値 |
|---|---|---|
| **LCP** (Largest Contentful Paint) | 最大要素の描画完了までの時間（読み込み速度） | **< 2.5 秒** |
| **INP** (Interaction to Next Paint) | クリック/タップ後の応答までの時間（応答性） | **< 200 ms** |
| **CLS** (Cumulative Layout Shift) | 視覚要素のずれ量（視覚的安定性） | **< 0.1** |

- 計測ツール：Search Console「Core Web Vitals」レポート、PageSpeed Insights、Chrome UX Report（CrUX）
- INP は 2024 年に FID から置き換わった現行指標
- その他のページ体験要素：**HTTPS必須**、モバイル対応、侵入型インタースティシャル回避、広告が主コンテンツを邪魔しないこと

---

## 9-B. 構造化データの実装ガイドライン

AI機能の必須要件ではないが、リッチリザルト適格・商品/レビュー/イベント等の表示で引き続き重要。

### フォーマット
| 形式 | Google推奨度 | 特徴 |
|---|---|---|
| **JSON-LD** | ★★★（推奨） | `<script type="application/ld+json">` 内に埋め込み、保守容易 |
| Microdata | △ | HTML属性で表現 |
| RDFa | △ | HTML5拡張 |

### 実装の必須条件
- **schema.org の語彙に準拠**しつつ、Google Search Central の各機能ドキュメントを優先
- **必須プロパティをすべて含める**（欠落=リッチリザルト非対象）
- **推奨プロパティは"質"重視**（完全で正確に）
- **可視テキストとの一致**：ページに表示されていないデータをマークアップに入れない（ポリシー違反）

### 検証
- **Rich Results Test**（開発時）
- **Rich result status reports**（デプロイ後の継続監視）
- **URL Inspection Tool**（個別ページのマークアップ認識確認）

---

## 9-C. Featured Snippets と AI Overviews の関係

- Featured Snippets（強調スニペット）= 通常検索結果の上に「説明文→タイトル」の逆順で表示される特別な結果
- **Featured Snippets の表示を狙ってリクエストすることはできない**（Googleが自動判定）
- AI Overviews との関係：両者は別機能だが、`nosnippet` / `max-snippet` でまとめて制御可能
- 完全に出したくない → `nosnippet`
- 部分的に抑制したい → `max-snippet:[小さい数字]`（保証はされない）

---

## 9-D. JavaScript SEO の落とし穴

GoogleはJSをレンダリングするが、以下は典型的な失敗パターン：

- **フラグメントルーティング**（`#/products` 形式）→ ❌ Googlebot がリンクとして認識しない。**History API** を使い `/products` 形式に
- **クライアントサイド 404**：実際には HTTP 200 を返してJSで「Not Found」を表示 → ソフト404扱い。JSで `<meta name="robots" content="noindex">` を付与するか、サーバ側で正しい 404 を返す
- **canonical をJSで設定**：非推奨。元のHTMLと同じ値にすること
- **キャッシュ問題**：Googlebot は積極的にキャッシュする。ファイル名にフィンガープリント（`main.2bb85551.js` 形式）を入れる
- **Web Components**：レンダリング後の HTML に見えるコンテンツのみ評価対象。Shadow DOM と Light DOM の両方が表示されるよう slot を活用
- **SSR / Hybrid Rendering を優先**：UXもクローラ互換性も向上する

---

## 9-E. eコマース固有の対応

### 商品データのGoogleへの伝達経路
1. **構造化データ**（`Product` schema：価格・在庫・レビュー）
2. **Merchant Center フィード**（商品カタログを直接送信）
3. **Google Business Profile**（実店舗情報）

### EC SEO の8重点領域（公式）
1. コンテンツ可視性（Google各サーフェスでの商品情報の出方）
2. データ共有方法の選択
3. 構造化データ実装
4. サイト立ち上げタイミング（新規ドメインの登録）
5. レビュー品質（信頼できる商品評価）
6. URL設計（クローラブルで論理的）
7. ナビゲーション階層（重要度を伝える）
8. UXパターン（ページネーション・遅延読み込みの影響管理）

### AI生成コンテンツのEC特別ルール
- AI生成画像：IPTC `DigitalSourceType` メタデータ + `TrainedAlgorithmicMedia` 指定
- AI生成テキスト（商品説明など）：明示的にラベル

---

## 10. サイト構築時のチェックリスト（実務適用版）

### A. コンテンツ
- [ ] そのページにしかない一次情報・体験・分析があるか
- [ ] 著者の専門性・経歴をプロフィールページで明示しているか
- [ ] バイラインから著者プロフィールへリンクしているか
- [ ] 見出し階層（H1→H2→H3）が論理的か
- [ ] 関連トピックを1ページで包括的に扱えているか（チャンキング不要）
- [ ] AI生成を使った箇所を開示しているか
- [ ] YMYL領域なら情報源・更新日・監修者を明示しているか

### B. テクニカル
- [ ] HTTP 200 で返るか
- [ ] Googlebot が robots.txt でブロックされていないか
- [ ] noindex / nosnippet が誤って付いていないか（AI機能から消したい場合のみ意図的に）
- [ ] レンダリングされた最終HTMLにテキストコンテンツが含まれるか（JSフレームワーク注意）
- [ ] Core Web Vitals が良好か（LCP<2.5s / INP<200ms / CLS<0.1）
- [ ] HTTPS で配信されているか
- [ ] モバイル対応済みか（モバイルファーストインデックス）
- [ ] 侵入型インタースティシャルがないか
- [ ] フラグメントルーティング（`#/`）を使っていないか
- [ ] 重複コンテンツに canonical を設定しているか
- [ ] 301リダイレクトが適切に張られているか
- [ ] Search Console にサイトマップを送信済みか
- [ ] Google-Extended の許可/拒否方針を決めているか（Gemini学習データに使わせるか）

### C. メディア
- [ ] 画像に説明的なalt属性が付いているか
- [ ] 画像/動画サイトマップを送信しているか
- [ ] AI生成画像にIPTCメタデータを付与しているか（EC）

### D. 構造化データ（必須ではないが推奨）
- [ ] リッチリザルト対象のスキーマを適切に実装
- [ ] 構造化データが可視テキストと一致している
- [ ] 構造化データテストツールで検証

### E. ビジネス情報（ローカル/EC）
- [ ] Google Business Profile を最新化
- [ ] Merchant Center に商品フィード送信
- [ ] NAP（Name/Address/Phone）の整合性

### F. やらないこと（避ける）
- [ ] llms.txt を置こうとしていない
- [ ] AI専用Markdownを生成しようとしていない
- [ ] AI向け不可視テキストを埋めていない
- [ ] 「メンション獲得」のために有料/対価リンクを撒いていない
- [ ] 1クエリ1ページの大量量産をしていない

---

## 11. 関連公式リソース（一次ソース集）

### 中核ドキュメント
- [Optimizing your website for generative AI features on Google Search](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide)
- [Search Essentials](https://developers.google.com/search/docs/essentials)
- [Technical Requirements](https://developers.google.com/search/docs/essentials/technical)
- [Spam Policies](https://developers.google.com/search/docs/essentials/spam-policies)
- [Creating helpful, reliable, people-first content](https://developers.google.com/search/docs/fundamentals/creating-helpful-content)
- [Using AI-generated content](https://developers.google.com/search/docs/fundamentals/using-gen-ai-content)
- [AI features in Google Search](https://developers.google.com/search/docs/appearance/ai-features)

### 技術系
- [SEO Starter Guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide)
- [How Google Search Works](https://developers.google.com/search/docs/fundamentals/how-search-works)
- [JavaScript SEO basics](https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics)
- [robots.txt intro](https://developers.google.com/search/docs/crawling-indexing/robots/intro)
- [Robots meta tag, data-nosnippet, X-Robots-Tag](https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag)
- [Core Web Vitals](https://developers.google.com/search/docs/appearance/core-web-vitals)
- [Page Experience](https://developers.google.com/search/docs/appearance/page-experience)

### 構造化データ・外観
- [Structured data intro](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data)
- [Structured data policies](https://developers.google.com/search/docs/appearance/structured-data/sd-policies)
- [Featured Snippets](https://developers.google.com/search/docs/appearance/featured-snippets)

### EC・ローカル・国際
- [Ecommerce SEO overview](https://developers.google.com/search/docs/specialty/ecommerce)
- [Share product data with Google](https://developers.google.com/search/docs/specialty/ecommerce/share-your-product-data-with-google)
- [International sites](https://developers.google.com/search/docs/specialty/international)

### モニタリング
- [Search Console](https://developers.google.com/search/docs/monitor-debug/search-console-start)
- [Debug traffic drops](https://developers.google.com/search/docs/monitor-debug/debugging-search-traffic-drops)

### 公式情報源（最新動向追跡）
- [Google Search Central Blog](https://developers.google.com/search/blog)
- [LinkedIn - Google Search Central](https://www.linkedin.com/showcase/googlesearchcentral/)
- [X/Twitter - @googlesearchc](https://twitter.com/googlesearchc)
- [YouTube - Google Search Central](https://www.youtube.com/c/GoogleSearchCentral)
- [Help Forum](https://support.google.com/webmasters/community)

---

## 12. 「サイト作成で迷ったら」最終判断軸

公式の一文がすべてを言い切っている：

> **"Focus on what your visitors would enjoy, find helpful, and feel satisfied with after visiting your website. If you're ever unsure about a decision for your site, ask yourself: 'Is this content that my visitors would find satisfying?'"**

迷ったら「自分の訪問者が満足するか？」だけを判断軸にする。AIO/GEOの裏技に走らない。

---

## 改訂履歴
- 2026-05-20 初版作成（出典：Google Search Central 公式ドキュメント / 取得日同日）
- 2026-05-20 公式ナレッジカバレッジ精査により以下を追記：
  - 4-2: `nosnippet` が AI Overviews / AI Mode の直接入力を明示的にブロックする公式仕様、`max-image-preview` / `max-video-preview` / `indexifembedded` / `notranslate`、`X-Robots-Tag` ヘッダ、robots.txt と メタタグの読み順注意
  - 4-3: Googleクローラ一覧（Googlebot / Google-Extended / GoogleOther）と AI機能/Gemini学習の制御区別、robots.txt 設定例
  - 9-A: Core Web Vitals の具体閾値（LCP/INP/CLS）、HTTPS必須、インタースティシャル回避
  - 9-B: 構造化データの形式比較・必須/推奨プロパティ・検証ツール（Rich Results Test 等）
  - 9-C: Featured Snippets と AI Overviews の制御関係
  - 9-D: JavaScript SEO の典型的落とし穴（フラグメントルーティング・ソフト404・キャッシュ等）
  - 9-E: ECフィード経路と EC SEO 8重点領域
  - チェックリストB: Core Web Vitals 閾値・HTTPS・モバイルファースト・フラグメントルーティング・Google-Extended方針を追加
