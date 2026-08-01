# UDSL Core + Extensions Inventory — Draft Snapshot

これは、utattemita.united-studio.com 制作前に、UDSL V4を Core + Extensions へ再整理するための作業中棚卸です。

この文書は正式なUDSL仕様ではなく、今後のCore化・Extension化・utattemita設計の判断材料です。

## 1. 背景

United Studioでは、予約システムである `reserve.united-studio.com` を起点として、その後に `studio.united-studio.com`、`yosakoi.united-studio.com` が制作された。

各サイトではUSDL V4の思想を共有しながら、対象となる体験に応じた表現が追加されている。

- reserve：迷わせず予約を完了させる業務UX
- studio：写真、空間、残響、静けさによるレコーディングスタジオの信頼表現
- yosakoi：祭り、隊列、演舞、作品アーカイブを扱う「制御された熱量」
- utattemita：これから定義する、POP、FUN、意外性と初心者の安心を両立する入口

次のサイトを制作する前に、現在の表現をすべて一つのUSDLとして積み上げるのではなく、United Studio全体で維持するCoreと、サイト固有のExtensionに分けて整理する必要がある。

### UtattemitaをPOP/FUNにする理由

`rec.united-studio.com` は、機能的で信頼性が高いランディングページとして成立している。

一方で、20代女性を中心とする「歌ってみた」初見ユーザーにとっては、少し重く、かっちりしすぎている可能性がある。サービスの品質や信頼性が伝わっていても、「自分もやってみたい」という最初の感情が、予約行動へ移る前に弱まる可能性がある。

Google広告のコンバージョン計測がよりシビアになる状況では、ホームページを初めて訪れた人が、その場で内容を理解し、安心し、予約へ進める割合が重要になる。

`utattemita.united-studio.com` は `rec.united-studio.com` の置き換えではない。recが担う機能性と信頼性を維持しながら、より軽く、POP性・意外性・FUNを前面に出した別の入口として設計する。

目的は、**「歌ってみたい」という気持ちを、「予約できる」という気持ちへ変えること**である。

## 2. 現在のブランチ・git状態に関する注意

このDraft Snapshotは、ローカルのUSDL V4リポジトリのクリーンな `main` から、`docs/udsl-core-extensions-inventory` ブランチを作成して保存した。

調査時点のUSDL V4リポジトリは `main...origin/main` で、既存ファイルに変更はなかった。

調査に使用したreserve制作コピーは独立したGitリポジトリとして認識されておらず、studioの正式なソースリポジトリも今回のローカル調査範囲では特定できていない。studioについては現行公開サイトの表示と、reserve制作コピー内のAtmosphere関連資料を照合した。

また、ローカルのyosakoiリポジトリと現行公開サイトには表現・コンテンツの差があるため、正式仕様化の前に、どの状態を正本とするか確認する必要がある。

## 3. UDSL V4の保存場所

調査基準としたローカルリポジトリ：

```text
/Users/usi/Documents/Codex/2026-07-14/git/work/usdl-v4-alpha
```

Remote：

```text
https://github.com/tetsufujiki/usi-creative-system
```

主要ファイル：

- `00_EDITORIAL_RULES.md`
- `01_MANIFESTO.md`
- `02_CREATIVE_PRINCIPLES.md`
- `03_CREATIVE_PHENOMENA.md`
- `CREATIVE_COMPASS.md`
- `README.md`

reserve/studioの実用仕様が蓄積されている調査元：

```text
/Users/usi/Documents/Codex/2026-07-14/reserve-production-audit-usdl-v4-reserve/work/usi-reserve-v0-main/.design/usdl
```

yosakoiの設計・運用資料：

```text
/Users/usi/Documents/Codex/2026-07-28/united-studio-com-yosakoi-matsuri-yosakoi-2/docs
```

## 4. V4の主な内容

USDL V4はUIコンポーネントやデザイントークンの仕様ではなく、United Studioの創作観を定義する原典である。

### ブランド命題

> We Design the Beginning of Creation.

United Studioがデザインするのは画面そのものではなく、訪れた人の中で創作が始まる瞬間である。

### 音のタネ

「音のタネ」はUnited Studioが利用者へ与えるものではない。感情、記憶、会話、迷い、喜びなどを通じて、すでにその人の中に存在している。

United Studioはそれを見つけ、守り、対話と共鳴を通じて形になる環境をつくる。

### Creative Compass

```text
Movement
        ↕
Stillness

Contrast
        ↕
Harmony

Dialogue
        ↕
Creation
```

この三軸は新しいサイトごとに増やすものではなく、ExtensionがUnited Studioの中心から外れていないかを確認するための座標として維持する。

### Creative Phenomena

初期語彙は以下である。

- Seed
- Dialogue
- Connection
- Resonance
- Growth
- Silence
- Breath
- Emergence
- Release

Creative Phenomenaはアニメーションやエフェクトの別名ではない。創作の過程、関係、反応、変化、余韻を、時間を通じて知覚可能にする方法である。

### 写真とCreative Phenomena

- 写真は、場所、設備、人、素材など「存在と信頼の現実」を伝える
- Creative Phenomenaは、感情、共鳴、成長、創作の進行など「変化の現実」を伝える

どちらか一方が他方を置き換えるものではない。

### Mobile as the Native Scale

MobileはPC用表現の縮小版ではない。手に近く、縦スクロールで時間が進む環境として、Creative Phenomenaのネイティブスケールに位置づける。

## 5. reserveで維持すべきCore要素

reserveの設計・実装を通じて有効性が確認された次の要素は、サイト横断のCore候補とする。

### 判断順序

```text
Experience
↓
Atmosphere
↓
Composition
↓
Decision
↓
Components
↓
Implementation
```

- UIやコンポーネントから考え始めない
- 最初に何を感じ、理解し、行動できるべきかを決める
- コンポーネントは構成の結果として選ぶ

### 判断とCTA

- 一画面または一つの判断領域につき、主な判断は一つ
- Primary Actionを複数競合させない
- Primary、Secondary、Text Actionの強弱を明確にする
- CTAは押した後に起こることを具体的に示す
- 外部サブドメインへ移る場合は移動先の性質を明示する

### 業務UXからCore化できる原則

- 情報を段階的に開示する
- 現在の判断に不要な情報を先に見せない
- システムが計算できることを利用者に考えさせない
- 入力内容と進行状態を失わない
- 処理中、成功、失敗を即座に伝える
- エラーは「何が起きたか」「なぜか」「どう戻るか」を説明する
- 完了時は、完了したことと次に起こることを明示する

### ブランドシェル

- ヘッダーでサイト固有名とUnited Studioの関係を示す
- フッターの著作権表記から会社サイトへ戻れるようにする
- サービス固有の表現が強くても、帰属先を見失わせない

### 共通品質

- 日本語コピーは短く、直接的で、結果を予測できるものにする
- 余白を情報階層の第一手段とする
- 色だけで状態を伝えない
- キーボード操作、セマンティックHTML、可視フォーカスを維持する
- `prefers-reduced-motion` に対応する
- Mobile Firstで判断する

予約カレンダー、予約ステータス、管理画面、休日色などはCoreではなくReserve Extensionへ残す。

## 6. studioで追加されたExtension要素

studioでは、V4のResonance、Silence、Breath、Emergenceが、レコーディングスタジオの空間表現として具体化された。

- 画面全体に固定されたAtmospheric Engine
- ページが切り替わるのではなく、同じ空間を歩くようなスクロール体験
- 写真とCanvas／モアレ的な光・色場の融合
- 暗いヒーローから紙、光、淡い暖色へ移る色温度の変化
- 暗部、ぼかし、被写界深度による音響的な奥行き
- Instrument Serif系の静かな大見出し
- 写真による設備・環境・実在性の提示
- 機材名、平面図、制作工程による専門性の可視化
- 固定された半透明ヘッダーと、必要時にだけ開くナビゲーション
- 録音空間を、複数の部屋ではなく連続した創作空間として説明する構成
- 最終CTAで予約システムへ明示的に引き渡す
- 初心者ガイドとFAQを、予約CTAより弱い導線として配置する

Studio Extensionの核は「暗いサイト」ではない。写真で信頼を示しながら、音の残響、距離、時間を空間として感じさせることにある。

## 7. yosakoiで追加されたExtension要素

yosakoiでは、V4の思想が「制御された熱量」と、長期運用される作品アーカイブへ翻訳された。

### 表現語彙

| Phenomenon | 意味 |
| --- | --- |
| Formation | 隊列、集団の秩序 |
| Surge | 押し寄せる熱量 |
| Pulse | 太鼓、リズム、鼓動 |
| Flow | 演舞構成の流れ |
| Burst | 見せ場の爆発 |
| Trace | 演舞後の軌跡と余韻 |
| Festival Layer | 衣装、光、会場感の重なり |

### 視覚・時間表現

- 深い緑、クリーム、橙、祭りの金色
- 非常に大きな明朝見出し
- 暗色、紙色、金、橙を切り替える強いセクション構成
- HEROとFinaleに限定したCanvas Kinetics
- 強い動きの間に、大きな静止面と読み物を置く
- reduced motionでは動きを止め、Formationの静止構成を残す
- ArchiveではCanvasを使わず、探索と操作を主役にする

### 作品アーカイブ

- 年度、チーム、曲名による検索
- 年度とチームによるフィルター
- 初期表示件数を限定し、「もっと見る」で段階的に展開
- 写真を必須にしない自動生成サムネイル
- 年度から色、チームから視覚パターンを決定
- YouTubeを初期HTMLで大量に読み込まない
- 利用者が再生を選んだ時だけiframeを生成する
- 同時に存在するiframeを最大1件に制限する
- 外部YouTubeで開く導線も残す
- チームID、表示名、作品IDを長期運用可能なデータ契約として管理する

## 8. Coreへ昇格すべき要素

| Core候補 | 出所 | Core化する理由 |
| --- | --- | --- |
| ExperienceからImplementationまでの判断順序 | reserve | 全サイトの制作判断に適用できる |
| 創作原則からPhenomenonを導く方法 | V4 | Extensionが単なるテーマ変更になることを防ぐ |
| 写真は信頼、Phenomenaは創作の変化を伝えるという役割分担 | V4 / studio | 異なるサイトでも意味が維持される |
| 一瞬に一つのPrimary Phenomenon | V4 / studio / yosakoi | 表現同士の競合を防ぐ |
| Atmosphereは判断やCTAを妨げない | reserve / studio | 表現が強いサイトにも必要な制御規則 |
| HERO、読み物、業務画面で表現強度を変える | 全サイト | 体験目的に応じた抑揚を作れる |
| Primary / Secondary / Text CTA | reserve / yosakoi | 行動の優先順位が共通する |
| 外部サービスへの遷移明示 | studio / reserve | サブドメイン間の迷いを防ぐ |
| サービス名とUnited Studioの二層アイデンティティ | 全サイト | 独立サイト化しても親ブランドを維持できる |
| 著作権表記から会社サイトへ戻る導線 | 全サイト | 現在のサイト間で共通している |
| reduced motion、可視フォーカス、skip link | reserve / yosakoi | ブランドに依存しない品質要件 |
| 音声・動画はユーザー操作を起点にする | yosakoi | utattemitaでも重要になる |
| Mobileを現象のネイティブスケールとする | V4 | PC版の縮小設計を防ぐ |
| 表現語彙ごとに用途と禁止事項を定義する方式 | studio / yosakoi | Extensionを安全に増やせる |

タイポグラフィは特定フォントをCoreに固定せず、次の役割をCoreとして定義する。

- Display：感情と世界観を伝える
- Body：長文と説明の可読性を担う
- Meta：年度、機材、ラベル、状態を整理する
- Action：結果を予測できる明瞭さを持つ

## 9. 各サイト固有に残すべき要素

### Reserve Extension

- 予約カレンダーと空き時間計算
- 予約、確認、完了フロー
- Pending、Confirmed、Cancelledなどの状態
- 土日祝の色分け
- 入力検証、二重送信防止、エラー復旧
- 顧客アカウント
- 管理画面、表、設定、監査
- 情報密度を上げた業務画面
- Atmosphereを極端に弱めるWorking Space

### Studio Extension

- 固定Atmospheric Engine
- 写真とモアレ／光場の融合
- 暗いヒーロー
- 音響的な遠近
- 固定された「部屋」の考え方
- 機材、平面図、録音工程
- Studio固有のDisplay Typography
- Studio固有の暖色ハイライト
- Reverberation／Resonanceの具体的描画方式

### Yosakoi Extension

- Formation、Surge、Pulse、Flow、Burst、Trace
- 深緑、金、橙のパレット
- 祭り、隊列、演舞を由来とする動き
- 巨大な明朝見出し
- HERO／Finale限定のKinetics
- 年度、チーム、作品データ契約
- 作品アーカイブの運用ルール
- YouTube再生管理
- 自動生成サムネイル
- 制作枠を過剰に約束しない問い合わせトーン

## 10. Utattemita用に新規定義すべき要素

utattemitaは「studioを明るくする」「yosakoiを軽くする」のではなく、新しい感情モデルを持つExtensionとして定義する。

### 体験目的

訪問前：

> 歌ってみたいけど、自分にできるか分からない。

訪問後：

> これなら自分も一歩目を踏み出せそう。

Primary Feelingは単純な興奮ではなく、楽しさによって不安が小さくなる `Playful Confidence` とする。

### Utattemita Phenomena Draft

| Phenomenon | 意味 | V4との接続 |
| --- | --- | --- |
| Spark | 音のタネに気づく小さな発火 | Seed / Emergence |
| Pop-up | 声や言葉が一段前へ出る | Emergence |
| Chorus | 一つの声に別の声が応答し、層になる | Dialogue / Resonance |
| Flip | 迷いや先入観が別の可能性へ反転する | Contrast / Growth |
| Remix | 見慣れた形が意外な組み合わせに変わる | Connection / Creation |
| Spotlight | 利用者自身が主役として現れる | Emergence / Release |
| Celebration Trace | 完了後に短く残る喜びの余韻 | Release / Trace |

これらはエフェクト名ではなく、利用者の感情や理解の変化を説明できる場合だけ使用する。

### 表現強度

- HERO：強いPOP、FUN、意外性
- サンプル、体験紹介：中程度
- 料金、工程、FAQ：落ち着いた信頼面
- 予約システムへの引き渡し：Core／Reserveに近い静かな状態
- 一画面に複数のSurpriseを重ねない
- Primary CTAの近くでは動きを抑える

### 色

- 高彩度色を複数使えるExtensionとする
- 本文面は安定した高コントラストを維持する
- Primary CTA色はページ内で一貫させる
- 「カラフル」と「選択肢が多い」を混同しない
- 状態表示色と装飾色を分離する

### タイポグラフィ

- 表情のあるDisplay書体を許可する
- 本文、料金、工程は安定したSansを使用する
- 文字の傾き、跳ね、サイズ差は見出し内に限定する
- 日本語の途中改行で意味を壊さない
- 小さな文字をPOP表現の代償にしない

### 写真・映像・音声

- マイクやスタジオだけでなく「歌う人の変化」を見せる
- 初心者が自分を重ねられる人物像を扱う
- 作られすぎた成功イメージだけにしない
- 音声、動画は自動再生しない
- サンプルを選んだ時だけ再生する
- 権利、肖像、YouTube利用方針を実装前に決める

### CTA Draft

- 入口：`歌ってみたい`
- 理解：`できることを見る`
- 不安解消：`初めての流れを見る`
- 相談：`自分の場合を相談する`
- 確定：`収録を予約する`
- reserveへ移るCTA：`予約システムへ移動します` を併記する

### コピー

- 初心者を下に見ない
- 専門用語で入口を狭めない
- 過剰な品質保証をしない
- 短く、話しかけるように書く
- FUNの中にも料金、準備、納品内容を具体的に置く

## 11. 推奨ドキュメント構成

```text
usdl/
├── README.md
├── CORE_PROMOTION_CRITERIA.md
│
├── core/
│   ├── 00_GOVERNANCE.md
│   ├── 01_BRAND_MANIFESTO.md
│   ├── 02_CREATIVE_PRINCIPLES.md
│   ├── 03_CREATIVE_PHENOMENA.md
│   ├── 04_EXPERIENCE_DECISION_ORDER.md
│   ├── 05_VISUAL_FOUNDATION.md
│   ├── 06_TYPOGRAPHY_AND_JAPANESE_COPY.md
│   ├── 07_CTA_NAVIGATION_FOOTER.md
│   ├── 08_INTERACTION_AND_FEEDBACK.md
│   ├── 09_ACCESSIBILITY.md
│   └── 10_RESPONSIVE_AND_PERFORMANCE.md
│
├── extensions/
│   ├── reserve/
│   │   ├── README.md
│   │   ├── WORKFLOWS.md
│   │   ├── STATUS_ERROR_RECOVERY.md
│   │   ├── ADMIN_UI.md
│   │   └── EXPRESSION_PROFILE.md
│   ├── studio/
│   │   ├── README.md
│   │   ├── ATMOSPHERIC_ENGINE.md
│   │   ├── PHOTOGRAPHY_AND_MOIRE.md
│   │   ├── SPATIAL_COMPOSITION.md
│   │   └── EXPRESSION_PROFILE.md
│   ├── yosakoi/
│   │   ├── README.md
│   │   ├── PHENOMENA.md
│   │   ├── KINETICS_CONTRACT.md
│   │   ├── ARCHIVE_PATTERN.md
│   │   └── CONTENT_DATA_CONTRACT.md
│   └── utattemita/
│       ├── README.md
│       ├── EXPERIENCE_HYPOTHESIS.md
│       ├── PHENOMENA_DRAFT.md
│       ├── POP_EXPRESSION_GUARDRAILS.md
│       ├── BEGINNER_JOURNEY.md
│       └── TRUST_AND_BOOKING_HANDOFF.md
│
└── decisions/
    ├── CORE_VS_EXTENSION.md
    ├── TYPOGRAPHY_DECISIONS.md
    ├── MOTION_BUDGET.md
    └── BRAND_SHELL_DECISIONS.md
```

### Core昇格基準

1. 二つ以上のサイトで意味が共通する
2. ドメイン固有語なしで説明できる
3. 異なる感情トーンでも維持できる
4. ブランド、安全性、理解、アクセシビリティのいずれかを守る

## 12. 実装前に決めるべき未決事項

- 新しいUDSL文書を置く正式なリポジトリとディレクトリ
- `USI Creative System V4` と `UDSL` の名称・責務の違い
- V4とreserve内のv3.1資料の優先順位
- studioの正式なソースリポジトリ
- yosakoiのローカル実装と公開状態のどちらを正本とするか
- Coreと各Extensionのバージョニング方法
- ExtensionからCoreへ昇格するレビュー手順
- 全サイト共通のロゴ／サービス名ロックアップ
- ヘッダーから会社サイトへ戻すか、フッターだけにするか
- 著作権表記の日本語／英語表記
- 外部サブドメイン遷移の表示ルール
- Coreで許可するDisplay書体の範囲
- Utattemitaの対象者を完全初心者、経験者、投稿活動者のどこまで含めるか
- 料金、納品、修正、動画制作をどこまで掲載するか
- reserveへ直接送る条件と、相談を先に置く条件
- POP表現の最大強度
- 一画面あたりのMotion／Surprise上限
- Canvas、画像、動画の性能予算
- WCAG 2.2 AAを正式要件にするか
- 音声、映像サンプルの権利処理
- 自動再生禁止とユーザー操作起点のメディア契約
- 実績、レビュー、エンジニア紹介など、信頼を担保する要素
- Utattemita独自の作品アーカイブを持つか
- 初心者導線をガイド、診断、FAQのどれで構成するか

---

このSnapshotは棚卸と仮説の保存を目的とする。ここに記載された構成、Phenomena名、Core昇格候補は、正式なUSDL仕様として承認されたものではない。
