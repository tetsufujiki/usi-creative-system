# UDSL Extension Model

> Status: Draft
>
> This document defines how individual United Studio properties can diverge in tone, layout, visual language, and conversion strategy while still belonging to the same creative system.

## 1. Definition

> A domain-specific expression layer for a specific audience, service, or creative context.

Extensionとは、特定の対象者・サービス・創作文脈に合わせて、Coreから意図的に表情を変える表現レイヤーである。

ExtensionはCoreの例外ではない。Coreの共通判断を、それぞれの入口に必要な感情、情報、行動へ翻訳したものである。

## 2. Core vs Extension

| Core | Extension |
| --- | --- |
| 共通思想 | 見た目 |
| 信頼の扱い | 色 |
| 導線設計 | HERO構成 |
| Brand attribution | コピーの温度 |
| Handoff logic | CTA文言 |
| Mobile reading principles | Motion / texture |
|  | 情報量 |
|  | サンプルの扱い |

Coreは、どのサイトでも守る判断基盤を定義する。Extensionは、その基盤を対象者と目的に合わせて具体化する。

## 3. Extension Identity

各Extensionは、最低限、次の項目を定義する。

```text
Primary Feeling
Audience State
Entry Emotion
Trust Strategy
CTA Strategy
Visual Language
Handoff Destination
Avoid List
```

これらを定義することで、Extensionを単なる色やレイアウトの差ではなく、体験目的の差として扱う。

## 4. Allowed Divergence

以下はExtensionごとに変えてよい。

- 色。
- Typography intensity。
- 写真主役かグラフィック主役か。
- Motion量。
- 英語の使用量。
- セクション密度。
- CTA文言。
- FAQの深さ。
- 実績・サンプルの見せ方。

差異は、対象者の心理状態とサイトの責務から説明できることを条件とする。

## 5. Required Consistency

以下は全Extensionで維持する。

- United Studioへの帰属。
- Copyright。
- Metadata。
- Structured data。
- Privacy / terms link。
- 外部導線の明示。
- 誤解を生まないサービス範囲。
- Mobile可読性。
- SEO上の基本整備。

視覚人格が異なっても、提供主体、責任、行動結果を曖昧にしない。

## 6. Handoff Responsibilities

Extensionはすべてを説明しない。ただし、次に進む導線を曖昧にしない。

- `reserve`：空き状況確認、予約、アカウント、確認。
- `rec`：料金、対応範囲、詳しいFAQ、録音サービスの機能説明。
- `studio`：空間、設備、録音環境、スタジオとしての信頼。
- `united-studio.com`：会社情報、全体像、各創作入口の関係。
- LINE：個別条件や予約前相談。

外部ハンドオフでは、移動先と、そこでできることをCTA付近で示す。

## 7. Extension Matrix

| Extension | Primary Feeling | Audience | Hero Role | Trust Strategy | Main Handoff | Avoid |
| --- | --- | --- | --- | --- | --- | --- |
| studio | Crafted Trust / Deep Focus | Recording clients, artists, creators | 空間・音・信頼を感じさせる | 写真・設備・導線・structured data | reserve / contact / company | 軽すぎるPOP化 |
| yosakoi | Festival Archive / Creative Continuity | よさこいチーム、制作検討者、過去作品閲覧者 | 歴史と熱量を見せる | 作品量・継続性・実績 | contact / works / company | 単なる動画一覧化 |
| utattemita | Playful Confidence | 20代女性中心、初見歌ってみたユーザー | 「自分にもできそう」を起こす | 後半で信頼を戻す | reserve / rec FAQ / LINE | 教室感、安心感の出しすぎ |
| rec | Practical Confidence | 録音・制作を具体的に検討している人 | 料金・内容・予約判断を支える | 説明量・FAQ・料金・実績 | reserve | 軽すぎて情報不足になること |
| reserve | Clarity / Execution | 予約する人 | 空き確認と予約を完了させる | UIの分かりやすさ・規約・確認導線 | account / payment / confirmation | 過剰演出 |

## 8. Anti-patterns

- Coreを全サイト共通デザインテンプレートとして扱う。
- Extensionを単なるカラーバリエーションとして扱う。
- 一つのサイトですべてを説明しようとする。
- HEROに情報を詰め込みすぎる。
- Target audienceより会社都合を優先する。
- Mobile改行を成り行きにする。

## 9. Promotion to Core

Extensionで成功した判断は、次の条件を満たす場合にCoreへの昇格を検討する。

- 複数サイトで有効である。
- 対象者が変わっても機能する。
- ブランド帰属を強める。
- Handoffを明確にする。
- Mobile可読性を改善する。
- サイト人格を壊さず再利用できる。

昇格は自動では行わない。実装結果と複数Extensionでの検証を経て判断する。
