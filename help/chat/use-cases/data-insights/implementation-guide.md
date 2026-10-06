---
title: Adobe Customer Journey AnalyticsまたはStreaming Mediaの実装計画を共同作業で行う
description: Coworkerの実装ガイドスキルが、エクスポート可能なチェックリストを使用して、ディスカバリーディスカバリーの会話を、パーソナライズされた順序付きの実装計画に変える方法を説明します。
hold: true
source-git-commit: 94cf399a48d13ee83c702804b50fdccd4baa9d71
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 1%
---

# Adobe Workfrontの導入計画

Coworkerには、5つの実装ガイドスキルが含まれています。Customer Journey Analytics、Adobe AnalyticsからCustomer Journey Analyticsへのアップグレード、Content Analytics（ACA）、Marketing Campaign Analytics（MCA）、ストリーミングメディアの各サーフェスごとに1つずつスキルを習得できます。 各スキルは、短いディスカバリー会話を、パーソナライズされた依存関係に対応した実装計画に変換します。インタラクティブなチェックリストとすぐに使用できる書き出しが、すべて1つのCoworker Chat会話内で完結します。

そうしたツールを導入または移行する場合は、Adobeの実装要件を手作業で調べたり、プロジェクト計画をゼロから構築したりする必要はなく、そうしたスキルを活用して、手順に従った順序付きのプランを作成できます。

>[!NOTE]
>
>次の点に留意してください。
>
>* これらの実装ガイドのスキルは、カスタム実装またはアップグレードステップ（これらのガイド）、実装（[Coworker Projectsを使用した実装チェックリストの生成](./intelligent-checklist.md)を参照）、検証（[Adobe AnalyticsからCustomer Journey Analyticsへのアップグレードの検証](./data-validation-aa-cja.md)または[Streaming Mediaの実装の検証](./streaming-media-validation.md)など）という、より大きなオプションのワークフローの一部です。 3つのステージすべてを使う必要はありません。 例えば、計画やチェックリストを作成することなく、データを検証できます。
>* これらのスキルは、Adobeシステムにアクセスしたり、変更を加えたりすることはありません。 CDPは、実装計画の立案に役立ちます。 ライブテナントに対して実行したり確認したりすることはありません。

そうしたスキルを活用して、以下を行います。

* 所有者、労力の見積もり、各ステップの依存関係など、Customer Journey Analyticsをゼロから構築するためのパーソナライズされた順序付きプランを入手できます。

* Adobe AnalyticsからCustomer Journey Analyticsへのアップグレードに関する移行計画（Adobe Analyticsの機能パリティマッピング、過去のバックフィルのシーケンス、Adobe Analyticsを廃止する前の検証ゲートなど）をご確認ください。

* ライセンス、プライバシー、PII スコーピング、ガイド付きコンフィギュレーションウィザードなど、Content Analytics（ACA）の導入に関するガイド付きプランを入手できます。

* Adobe ソースコネクタ、独自のデータセット、ハイブリッドアプローチなど、取り込みパスに適応するMarketing Campaign Analytics（MCA）のオンボーディングプランを入手できます。

* データストリーム設定、プラットフォームごとのSDK/API実装、メディアイベントモデルなど、Edgeでのストリーミングメディア収集の実装計画を説明します。

## 始める前に

<!-- FLAG: Best guess, not confirmed by source docs. Requirements doc doesn't state explicit prerequisites for starting a discovery conversation — verify with skills-overview.md or SME before publishing. -->

### 必要な情報

実装ガイドを活用するには、次のことが必要です。

* 5つの実装パスのうち、Customer Journey Analytics（net-new）、Adobe AnalyticsからCustomer Journey Analyticsへのアップグレード、Content Analytics（ACA）、Marketing Campaign Analytics（MCA）、またはStreaming Mediaのいずれかを適用します。

* 現在の環境に関する基本的な詳細（既存のAdobe Analyticsの実装、ライセンスのステータス、計画されたデータ取り込みパスなど）。 ディスカバリー会話では詳細を尋ねられますが、準備をしておくとプロセスがスピードアップします。

### 制限事項

これらのスキルを使用する前に、次の制限に注意してください。

* **計画のみ**：これらのスキルは、Adobe システムにアクセスしたり、変更を加えたりすることはありません。 実装を実行したり、ライブテナントに対して検証したりすることはありません。
* **スキルごとに1つの製品サーフェス**：各スキルは1つの実装パスをカバーします。 リクエストが別の製品サーフェスに適用される場合、スキルは直接回答するのではなく、正しいサーフェスに誘導します。
* **自分でプロジェクトを追跡するエクスペリエンスではありません**：これらのスキルはプランと書き出しを生成しますが、進行中のステータス、共同作業、または承認を自分で追跡することはできません。 プランを経時的に追跡するには、事前に定義されたプレイブックを使用して、プランをCoworker プロジェクトに変換します。 [同僚プロジェクトによる実装チェックリストの生成](./intelligent-checklist.md)を参照してください。

## 実装計画セッションを開始する

1. Coworkerにログインします。

1. [!UICONTROL **新しいチャット**]&#x200B;を選択します。

1. テキストフィールドに、計画する実装または移行を記述します。 次に例を示します。

   **プロンプト**

   > Customer Journey Analyticsの実装計画を手伝ってください。

   リクエストは、対応する実装ガイドスキルにルーティングされ、インタラクティブなディスカバリーコミュニケーションが開始されます。

1. （条件付き）どの実装パスが適用されるかをスキルが判断できない場合は、そのスキルが求める明確な質問に答えてから、続行します。

## 導入パスの選択

各実装ガイドスキルは、1つの製品表面をカバーしています。

### Customer Journey Analytics

既存のAdobe Analyticsを導入することなく、Customer Journey Analyticsをゼロから構築するためのパーソナライズされた順序付きの実装計画を作成できます。 プランには、各ステップの所有者、労力の見積もり、依存関係が含まれます。

プロンプトの例：

* Customer Journey Analyticsの実装計画を手伝ってください。
* 私はCustomer Journey Analyticsをゼロから立ち上げました。 実行計画を立てる。

### Adobe AnalyticsからCustomer Journey Analyticsへのアップグレード

Adobe Analytics機能のパリティをCustomer Journey Analyticsにマッピングし、過去のバックフィルをシーケンス化し、Adobe Analyticsを廃止する前に検証と並列実行ゲートを含む移行計画を取得します。

プロンプトの例：

* Adobe AnalyticsからCustomer Journey Analyticsへのアップグレードの計画を支援します。
* Adobe AnalyticsからCustomer Journey Analyticsへの移行計画を作成します。

### Content Analytics（ACA）

ライセンス、プライバシー、PII スコーピング、ガイド付きコンフィギュレーションウィザードなど、Content Analytics（ACA）の導入に関するガイド付きプランを入手できます。 ACAはDULE、CMK、HIPAAに対応していないため、プランにはプライバシーゲーティングの手順が含まれます。

プロンプトの例：

* Content Analyticsの実装計画を手伝ってください。
* ACAの導入計画を立案。

### Marketing Campaign Analytics（MCA）

Adobe ソースコネクタ、独自のデータセット、ハイブリッドアプローチのいずれを使用しても、環境に合わせてfunnel マッピングとデータ整合ステップを調整できるため、取り込みパスに適応するMarketing Campaign Analytics（MCA） Essentialsのオンボーディングプランを入手できます。

プロンプトの例：

* Marketing Campaign Analyticsの実装計画を手伝ってください。
* 独自のデータセットを使用して、MCA オンボーディングプランを作成する。

### Streaming Media

Edgeでのストリーミングメディア収集の実装計画を取得します。データストリームの設定、プラットフォームごとのSDK/APIの実装、メディアイベントモデルをカバーしているので、Customer Journey AnalyticsやAdobe Analytics レポートのセッション、ping、補完を正しく測定できます。

プロンプトの例：

* ストリーミングメディアの実装計画を立てる方法を教えてください。
* Edgeでストリーミングメディアをインストルメントするための計画を作成します。

## 結果を見る

Coworkerは、同じ会話で、実装計画をインタラクティブなチェックリストと概要として返します。

**インタラクティブ チェックリスト**

Adobe HTMLのチェックリスト。導入のステップをフェーズとマイルストーンに分類します。 各ステップのチェックリストには、次の項目が含まれます。

* 労力見積もり
* プライマリオーナーおよびサポートするオーナー
* 他のステップへのハードな依存
* ステップをスキップできるかどうか
* 関連するExperience Leagueまたはdeveloper.adobe.com ドキュメントへのリンク

**書き出し**

ワークフローに合った形式でプランをダウンロードします。

| 書き出し | この記事の内容 |
| --- | --- |
| CSV | 手順の簡単なリスト |
| Jira-import CSV | Jiraに読み込むストーリーポイント、優先度、ラベルでフォーマットされたステップ |
| WORKFRONT CSV | Workfrontに読み込む期間と先行タスクでフォーマットされた手順 |
| Markdown | ドキュメントやWikiにペーストできるチェックリスト |

**チャット内の概要**

Coworkerは、チェックリストと共に、会話の中で直接3つの部分の要約を提供します。

1. プランの概要
1. 完全なステップテーブル
1. 各エクスポートのダウンロードリンク

## どのように計画が立てられるか

実装ガイドの各スキルは、同じ4段階のプロセスに従います。

* **検出**：段階的な会話では、実装パスに固有の5 ～ 9組の質問を使用して、環境と目標について学習します。
* **計算**: LLMは、回答に適用される条件付き手順と依存関係の上書きを決定します。 計画そのものを書くのではない。
* **組み立てとレンダリング**：決定論的プロセスは、ステップ間の依存関係を解決し、それらを注文し、クリティカルパス（依存するステップの最長チェーン）を計算し、チェックリストと書き出しを生成します。
* **配信**：共同作業者がダウンロードリンクとプランのチャット内サマリーを提供します。

このガイド付きの発見と決定論的な組み合わせにより、プランはフリーハンドで書かれるのではなく、回答から一貫して生成されます。
