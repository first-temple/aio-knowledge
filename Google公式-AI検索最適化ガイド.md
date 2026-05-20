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
| `nosnippet` | スニペット表示を完全に抑制（AI Overviews等にも引用されにくくなる） |
| `data-nosnippet` | ページ内の特定箇所だけスニペット利用を抑制 |
| `max-snippet:[n]` | スニペット最大文字数を制限 |
| `noindex` | インデックス自体を拒否 |
| `robots.txt` の Googlebot disallow | クロール自体を拒否 |

### 4-3. パフォーマンス計測
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
- [ ] noindex / nosnippet が誤って付いていないか
- [ ] レンダリングされた最終HTMLにテキストコンテンツが含まれるか（JSフレームワーク注意）
- [ ] Core Web Vitals が良好か
- [ ] モバイル対応済みか
- [ ] 重複コンテンツに canonical を設定しているか
- [ ] Search Console にサイトマップを送信済みか

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
