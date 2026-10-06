---
title: Coworkerで品質のゲートスキルを構築して実行する
description: カスタム同僚スキルを使用して、オーディエンスのアクティベーションを、抑制リスト、頻度キャップ、デプロイメント前の命名標準に対して自動的に検証する方法を説明します。
role: User
level: Beginner, Intermediate
doc-type: Feature Video
duration: 101
last-substantial-update: 2026-09-08
jira: KT-22379
source-git-commit: dbee38135a5491fd21b65fdbb70ba60d949d7560
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 1%
---

# カスタム AI スキルを使用して、質の高いゲートスキルを構築、実行する

マーケティング部門は、ルールとガバナンスプロセスを活用して、オーディエンスを正しくアクティベートします。 多くの場合、オーディエンスを配信先に誘導する前に、抑制リスト、頻度の上限、同意要件、命名規則を検証する必要があります。
 
問題は、これらのチェックが頻繁に部族的な知識と手作業によるレビューに依存することです。 人の頭の中でプロセスが生まれれば、ミスが起こることもあります。

この動画では、カスタム同僚スキルがアクティベーションゲートとして機能し、組織のアクティベーション標準に照らし合わせてオーディエンスを自動的に検証し、ダウンストリームに移行する方法をご覧いただけます。

>[!VIDEO](https://video.tv.adobe.com/v/3503166/?captions=jpn&learn=on&enablevpops)

## アクティブ化の品質ゲートスキルの例
 
Coworkerにプロンプトを貼り付けることで、再利用可能な&#x200B;**アクティベーション品質ゲート**&#x200B;独自のスキルを作成できます。 同僚のスキルオーサリング機能により、プロンプトが&#x200B;**自分の環境**&#x200B;内の保存されたスキルに変換されます。 ビデオのデモに基づくサンプルは次のとおりです。
 
重要なのは、3つのガバナンスゲートについて&#x200B;**独自の合否基準**&#x200B;を定義することです。
 
1. 抑制/同意
2. 頻度の上限
3. 命名規則
 
フレームワークは誰にとっても同じです。 組織の標準に合わせて、**`[...]`**&#x200B;でマークされたセクションをカスタマイズします。

## マスタープロンプト

> **これを「Activation Quality Gate」というスキルとして保存します。**

```text
It's a governance gate that runs a pre-activation checklist before any audience is sent to a destination.

It is read-only. It never activates, mutates, or copies anything.

Resolve the named audience and destination from our Knowledge Graph, evaluate the three gates below, then render one visual scorecard containing:

- An Alert banner
- One MetricCard per gate
- A DataTable with:
- Gate
- Status
- Finding
- Required Fix

Provide a single verdict:

- CLEARED only if all three gates pass
- BLOCKED if any gate fails

For every failed gate, provide the specific remediation needed.
 
All gates fail closed:

- Missing data = BLOCKED
- Never assume success when information is unavailable
 
Trigger phrases:

- "run the activation gate"
- "is this audience ready to activate"
- "pre-activation checklist"
- "can I activate to ..."

The three gates are:
 
[Paste Gate 1, Gate 2, and Gate 3 definitions here]
```

## ゲート 1：抑制/同意
 
> このセクションを、組織の抑制と同意要件に合わせて編集します。
 

```text
Gate 1 – Suppression List

Pass only if a recognized suppression, opt-out, or consent audience is applied alongside the target audience.

Discover eligible lists using name patterns such as:

- suppress
- opt-in
- opt out
- consent
- do not contact
 
Because suppression lists may live in destination dataflows rather than audience metadata, require the marketer to confirm one is attached.
 
If no suppression or consent list exists anywhere in the sandbox, fail hard.
 
Our standard:

[Example: A consent audience is mandatory for all email and SMS destinations. For direct mail destinations it is optional.]
```

## ゲート 2：周波数キャップ

> 組織の配信頻度の要件に合わせて、このセクションを編集します。

```text
Gate 2 – Frequency Cap
 
Read the delivery frequency on the resolved destination.

Pass if:

- Frequency is present
- Frequency is bounded

Fail if:

- Frequency is blank
- Frequency is unbounded

Our standard:

[Example: Frequency must be DAILY or less frequent. Any hourly cadence or blank value is blocked.]
```

## ゲート 3：命名規則
 
> 組織のオーディエンスの命名ルールに合わせて、このセクションを編集します。
 

```text
Gate 3 – Naming Convention

Evaluate the audience name programmatically.

Any rule violation causes failure.

Block names that:

- Contain "test"
- Contain "copy"
- Contain an auto-copy suffix such as _[6-hex]
- Contain timestamps
- Contain 24-character object IDs
- Start with a bare number or cryptic short code
- Are entirely lowercase
- Are excessively short or unclear
- Use generic defaults such as:
- Save audience
- Email
- New Accounts
- Lack a category–qualifier separator

Our standard:

[Example: [Line of Business] – [Criteria] in title case]

Example:

Mortgage – High Propensity Prospects

When blocked on naming, always propose a compliant replacement name.
```

## ガイダンス

### &#x200B;1. 角括弧で囲まれたセクションのみをカスタマイズする

**`[...]`**&#x200B;に含まれるセクションのみを更新してください。
 
これらのセクションでは、組織の特定のガバナンス基準を定義します。
 
その他のことは変更すべきではありません。

- オーディエンス解決
- ゲート評価
- スコアカードレンダリング
- 評決ロジック


### &#x200B;2. 前提条件を確認
 
このスキルは、次の要素に依存します。
 
- ナレッジグラフへのアクセス
- オーディエンスの検出
- 配信先の発見
- 抑制リストの検出
- ビジュアルアーティファクトのサポート
- アラートバナー
- MetricCards
- DataTable レンダリング

お客様の環境でこれらの機能が使用できない場合、スキルは設計どおりに実行できません。

### &#x200B;3. スキルを読み取り専用にする

スキルは常に読み取り専用である必要があります。

この要件をプロンプトに明示的に含めて、スキルがアクティベーションワークフローと混同されないようにします。

アクティベーション品質ゲートでは、アクティベーションの準備状況のみが評価されます。 オーディエンスのアクティブ化、設定の変更、データのコピーは&#x200B;**not**&#x200B;です。
