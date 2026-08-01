# UDSL Core

> Status: Draft
>
> This document defines the shared design logic for United Studio digital properties. It is derived from studio, yosakoi, and utattemita implementation learnings, and is not yet a locked specification.

## 1. Purpose

UDSL Coreは、United Studio全体のデジタル表現に共通する思想、構造、判断基準をまとめる。

目的は、全サイトを同じ見た目にすることではない。各サイトの役割、訪問者の心理状態、表現人格を分けながら、United Studioとしての帰属、信頼、導線を維持するための共通基準を持つことである。

Coreはデザインテンプレートではなく、異なる入口を同じCreative Systemとして判断するための基盤である。

## 2. Core Principle

> United Studio is not a single flat company website.
>
> It is a creative system with multiple entry points.

United Studioは、単一の会社案内サイトではなく、複数の創作入口を束ねるシステムである。

各入口は異なる感情、情報量、行動を扱ってよい。ただし、訪問者がどの入口から入っても、誰が提供し、次にどこへ進めるかを見失わせない。

## 3. Role of United Studio

United Studioが扱う領域は、単なるサービスメニューではない。それぞれを、創作が始まる状況と必要な支援の違いとして扱う。

- 歌ってみた：歌いたい気持ちを最初の一曲へ変える。
- レコーディングスタジオ：音をつくる空間、設備、技術、信頼を示す。
- よさこい制作：作品、制作履歴、祭りの熱量と継続性を伝える。
- プロデュース：まだ形になっていない企画や表現を作品へ導く。
- 予約：空き状況の確認から予約完了までを確実に進める。
- 会社情報：すべての入口の帰属、責任主体、活動全体を示す。

## 4. Site Architecture

```text
united-studio.com
→ Core / Hub / Company + Creative System

studio.united-studio.com
→ Space / Trust / Facility / Recording Studio identity

yosakoi.united-studio.com
→ Works / Archive / Festival energy / Production history

utattemita.united-studio.com
→ Psychological entry / POP / FUN / First-action trigger

rec.united-studio.com
→ Functional LP / Pricing / Booking motivation / Service clarity

reserve.united-studio.com
→ Booking execution / Availability / Account / Reservation
```

サイトは上下関係だけで整理しない。各サイトが一つの責務を明確に持ち、必要な情報と行動を別のサイトへ引き渡す分散構造として扱う。

## 5. Trust and Expression

すべてのサイトで、最初から同じ方法・同じ強度の信頼感を出す必要はない。

HEROは対象者の心理を動かす役割へ集中してよい。信頼は、後半の事実情報、footer、metadata、structured data、会社帰属、関連サイトへの導線によって補完できる。

ExpressionとTrustは分離可能である。ただし、どちらかを削除してよいという意味ではない。表現は入口をつくり、信頼は判断と行動を支える。必要になる順序に合わせて配置する。

## 6. Handoff Logic

各サイトはすべてを抱え込まない。

- 詳細説明、料金、対応範囲は `rec` へ引き渡す。
- 空間、設備、録音環境は `studio` へ引き渡す。
- 空き状況確認と予約実行は `reserve` へ引き渡す。
- 会社情報と全体の帰属は `united-studio.com` へ引き渡す。
- 作品履歴は `yosakoi`、将来の `works` / archive系へ引き渡す。

入口サイトは、すべての答えを持つ必要はない。ただし、なぜ次へ進むのか、移動先で何ができるのかを明示する。

## 7. Mobile-first Reading

Mobileでは、見出しの改行を自動折り返しの結果にしない。

- 重要コピーは、2行・3行でどう読まれるかまで設計する。
- 改行によって主語、意味、リズムを壊さない。
- Desktop用見出しの縮小版として扱わない。
- 文字装飾、サイズ差、傾きは可読性を超えない。
- 一画面の主題とPrimary Actionを明確にする。

## 8. Brand Consistency

ブランド統一とは、同じ色、同じ書体、同じUIを全サイトへ適用することではない。

United Studioへの帰属は、サイト名のロックアップ、copyright、metadata、structured data、footer、会社サイトへの導線で担保する。

各サイトのHERO、操作UI、コピー、色、motionは、Extension人格に合わせて変えてよい。共通化するのは見た目ではなく、帰属、責任、誤解のない導線である。

## 9. What Core Does Not Mean

Coreは、次を意味しない。

- すべてのサイトを同じデザインにすること。
- すべてを黒背景にすること。
- すべてにAtmosphere Engineを使うこと。
- すべてに写真HEROを使うこと。
- すべてで同じCTA文言を使うこと。
- すべてを会社案内化すること。

特定サイトで成功した表現を、検証なしに全サイトへ広げない。

## 10. Open Questions

- `united-studio.com` 本体で各Extensionをどの程度見せるか。
- `rec` と `utattemita` の広告流入先をどう分けるか。
- `works` / `archive` / `projects` をどう整理するか。
- Core仕様としてどこまで固定するか。
- どの時点で `main` へmergeするか。
