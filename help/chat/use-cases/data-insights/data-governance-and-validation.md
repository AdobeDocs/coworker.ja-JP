---
title: Adobe Analyticsの実装と管理（Coworker Chatを使用）
description: Adobe Workfrontの共同作業チャット機能を利用すれば、導入の計画を立て、チェックリストに従って追跡し、Adobe Analytics、Customer Journey Analytics、Experience Platformのデータを検証できます。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: decc8d209d4c9c177c6329a30668f0bbb8bd2c00
workflow-type: tm+mt
source-wordcount: '1235'
ht-degree: 0%
---

# インテリジェントな実装と管理の概要

Adobe Adobe CX Enterprise Coworker Chatを使用すれば、Adobe Analyticsの実装を設定、移行、管理し、あらゆる回答の背後にあるデータを信頼できるようにします。 Adobe Workfrontの導入を計画し、その計画をチェックリストに変換してチームで追跡できるようにすることで、データの収集後に検証することができます。

インテリジェントな実装と管理は、Adobe Workfrontのいくつかの分析領域のひとつです。 すべてのドメインを表示するには、「共同作業者チャットを使用したデータの分析」の「[共同作業者チャットでの分析の開始](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)」を参照してください。

**管理者：**&#x200B;に最適

## Adobe Workfrontの導入ワークフローの連携

このページのユースケースは、オプションの3段階のワークフローに従います。 任意のステージを単独で使用できます。 例えば、最初に計画やチェックリストを作成することなく、データを検証できます。

1. **プラン：** パーソナライズされた、注文された実装またはアップグレード プランを入手します。 [同僚との実装計画](/help/chat/use-cases/data-insights/implementation-guide.md)を参照してください。
1. **実装：** チームが割り当てて追跡できるCoworker Projectsのチェックリストにプランを変更します。 [同僚プロジェクトによる実装チェックリストの生成](/help/chat/use-cases/data-insights/intelligent-checklist.md)を参照してください。
1. **検証：** データが正しく設定され、収集されていることを確認します。 [&#x200B; ユースケース &#x200B;](#use-cases) テーブルの検証ユースケースを参照してください。

## 前提条件

<!-- FLAG: Confidence: Medium for the shared bullets. They differ from the other domain pages on purpose: planning doesn't query your data, and Experience Platform validation uses Experience Platform datasets rather than data views or report suites. The permission inheritance for Experience Platform is inferred. High for the "Additional prerequisite" notes in the Use cases table, which are sourced from the "Before you begin" section of each linked article. Some of those articles flag their own prerequisites as unconfirmed (implementation-guide.md, intelligent-checklist.md, streaming-media-validation.md), so verify those rows when those flags are resolved. Validate dataset quality for Customer Journey Analytics is a video page with no stated prerequisites, so it isn't listed. -->

このページのユースケースを使用するには、次のものが必要です。

* 同僚とのチャットへのアクセス： [同僚チャット &#x200B;](/help/chat/use-cases/data-insights/analytics-chat.md)によるデータ分析を開始するを参照してください。
* 検証するデータへのアクセスを表示します。 Coworker Chatは、接続先のAdobe アプリケーションから権限を継承します。

## ユースケース

| ユースケース | 関数 |
| --- | --- |
| [実装の計画](/help/chat/use-cases/data-insights/implementation-guide.md)<p>![実装の計画](../../assets/ui-guide-6.png)</p> | Customer Journey Analyticsの実装、Adobe Analyticsからのアップグレード、EdgeでのContent Analytics、Marketing Campaign Analytics、ストリーミングメディアコレクションの設定などについて、パーソナライズされたステップバイステップの計画を作成します。 計画には、所有者、労力の見積もり、依存関係、検証手順などの詳細が含まれます。<p>**サンプルプロンプト：** 「Customer Journey Analyticsの実装の計画を手伝ってください」</p><p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、このユースケースでは、どの実装パスが適用されるか、ライセンスのステータスや計画されたデータ取り込みパスなど、現在の環境に関する基本的な詳細を把握している必要もあります。</p><p>詳しくは、[同僚との実装の計画](/help/chat/use-cases/data-insights/implementation-guide.md)を参照してください。</p> |
| [実装チェックリストを生成](/help/chat/use-cases/data-insights/intelligent-checklist.md)<p>![実装チェックリストを生成](../../assets/data-validation-aa-cja/date-detail.png)</p> <p>実験的</p> | Customer Journey Analyticsの導入計画をCoworker Projectsのチェックリストに変換し、手順の割り当て、ステータスの追跡、承認ゲートの追加を可能にします。<p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、このユースケースでは、実装ガイドの会話を完了し、組織内の同僚プロジェクトにアクセスする必要もあります。</p><p>詳しくは、[同僚プロジェクトを使用した実装チェックリストの生成](/help/chat/use-cases/data-insights/intelligent-checklist.md)を参照してください。</p> |
| [Adobe AnalyticsからCustomer Journey Analyticsへのアップグレード時にデータを検証](/help/chat/use-cases/data-insights/data-validation-aa-cja.md)<p>![Adobe AnalyticsからCustomer Journey Analyticsへのアップグレード時にデータを検証](../../assets/data-validation-aa-cja/trend-bar-card.png)</p> | Adobe Analytics レポートスイートとCustomer Journey Analytics データビュー間のディメンション、指標、傾向を比較し、不一致を検出して、アップグレードをサポートするための修正を推奨します。<p>**管理者、アナリスト：**&#x200B;に最適</p><p>**サンプルプロンプト：**</p><ul><li>「AA レポートスイートとCJA データビューの比較」</li><li>「AAとCJAの間で一致しない指標はどれですか？」</li></ul><p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、この使用例では、検証するAdobe Analytics レポートスイートと、同じデータを含むCustomer Journey Analytics データビューも必要です。</p><p>詳しくは、「[Adobe AnalyticsからCustomer Journey Analyticsにアップグレードする際にCoworkerでデータを検証する](/help/chat/use-cases/data-insights/data-validation-aa-cja.md)」を参照してください。</p> |
| [Adobe Analytics プロジェクトをCustomer Journey Analyticsに移行](/help/chat/use-cases/data-insights/migrate-projects-aa-cja.md) <br/> （利用制限あり） | Adobe Analytics プロジェクトのディメンションと指標がCustomer Journey Analytics データビューのディメンションと指標にマッピングされていることを検証し、自動マッピングできないディメンションをマッピングし、プロジェクトと関連するコンポーネントをCustomer Journey Analyticsで再作成します。<p>**サンプルプロンプト：** 「AAからCJAにコンポーネントを移行したい」</p><p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、このユースケースでは、Adobe Analytics MCP アクセス、およびAdobe Analyticsの管理者権限またはコンポーネントの移行権限も必要です。</p><p>詳しくは、「[Adobe Analytics プロジェクトをCustomer Journey AnalyticsにCoworkerと共に移行する](/help/chat/use-cases/data-insights/migrate-projects-aa-cja.md)」を参照してください。</p> |
| [&#x200B; ストリーミングメディア実装の検証](/help/chat/use-cases/data-insights/streaming-media-validation.md)<p>![&#x200B; ストリーミングメディア実装の検証](../../assets/ui-guide-8.png)</p> <p>実験的</p> | データストリーム、スキーマ、データセット、データビュー、セッションデータを確認して、ストリーミングメディアトラッキングが設定され、データが正しく収集されていることを確認します。<p>**サンプルプロンプト：** 「ストリーミングメディアの実装は全体的にどれくらい正常ですか？」</p><p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、このユースケースでは、組織のExperience Platform データとCustomer Journey Analytics データがCoworkerに接続されている必要もあります。 一部の検証モードでは、ビデオセッション IDまたはログファイルも必要です。</p><p>詳しくは、[&#x200B; ストリーミングメディア実装を共同作業者と検証](/help/chat/use-cases/data-insights/streaming-media-validation.md)するを参照してください。</p> |
| [Customer Journey Analyticsのデータセット品質を検証](/help/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md)<p>![Customer Journey Analyticsのデータセット品質を検証](../../assets/data-validation-aep/dataset-validation.png)</p> <p>実験（来週）</p> | Customer Journey Analyticsレポートに使用するデータセットを特定し、スキーマ、ID品質、フィールド品質をチェックすることで、ダッシュボードを構築する前に問題を解決できます。<p>詳しくは、「[Coworkerでのデータ検証スキルを使用したCustomer Journey Analytics データの検証](/help/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md)」を参照してください。</p> |
| [Experience Platformに取り込んだ後のデータの検証](/help/chat/use-cases/data-insights/data-validation-aep.md)<p>![Experience Platformに取り込んだ後のデータの検証](../../assets/data-validation-aep/null-values.png)</p> | 新しい実装の後、または継続的なデータ管理の一環として、Experience Platform データセットとフィールドに対して統計チェックとセマンティックチェックを実行し、無効な値やマッピングの問題などのデータ品質の問題を見つけます。<p>**サンプルプロンプト：**</p><ul><li>「データセット [ データセット名]を検証します」</li><li>「データセット [ データセット名]から[ データフィールド ]を検証する」</li></ul><p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、この使用例では、検証するデータセットの名前またはIDも必要です。 必要に応じて、検証する特定のフィールドの名前を指定できます。</p><p>詳しくは、[Experience Platform データを共同作業者と検証](/help/chat/use-cases/data-insights/data-validation-aep.md)するを参照してください。</p> |
| [&#x200B; データインサイトの高速化](/help/chat/use-cases/data-insights/accelerate-data-insights.md) | Adobe Workfrontの導入計画を立て、サポートされているアクションを実行し、web サイトのエンゲージメントデータを分析する準備が整うまで、Adobe Experience Manager、Experience Platform、webSDK、Customer Journey Analyticsをまたいで製品および開発ステップをガイドする様子を動画で紹介します。<p>詳しくは、[同僚、AEM、CJAを使用したデータインサイトの高速化](/help/chat/use-cases/data-insights/accelerate-data-insights.md)を参照してください。</p> |

## 使用するスキル

<!-- FLAG: Confidence: High for `aa-cja-validation` (listed in the Skills and limitations table and in workflows.md). Medium for `data-validation`: workflows.md lists it, but with a TODO to confirm the skill ID with engineering. Medium for the implementation guide skills and the Streaming Media Validation skill: the articles name them but don't give technical skill IDs, so they're listed by display name. Only `aa-cja-validation` currently appears in the Skills and limitations table on analytics-overview.md. Add the others there so the link below covers them. -->

この記事で説明するユースケースでは、次のスキルを使用します。 必要な権限とカバーされていない内容を含む、すべての分析スキルの一覧については、「共同作業者チャットを使用したデータ分析」の[&#x200B; スキルと制限事項](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。

| スキル | に使用 |
| --- | --- |
| 導入ガイドのスキル（Customer Journey Analytics、Adobe AnalyticsからCustomer Journey Analyticsへのアップグレード、Content Analytics、Marketing Campaign Analytics、およびStreaming Mediaの各スキル） | Adobe Experience Manager Sites導入計画 |
| `aa-cja-validation` | Adobe AnalyticsからCustomer Journey Analyticsにアップグレードする際のデータの検証 |
| ストリーミングメディア検証スキル | ストリーミングメディア実装の検証 |
| データ検証スキル （`data-validation`） | Customer Journey Analyticsのデータセット品質の検証<br>Experience Platformに取り込んだ後のデータの検証 |

## より良い結果を得るためのヒント

* データの検証時に比較する特定のレポートスイートとデータビューに名前を付けます。
* 検証結果を自身の変更の手引きとして使用できます。 ストリーミングメディア検証スキルとデータ検証スキルを活用すれば、課題を特定できますが、設定やデータは変更されません。
* 実装が変更されるたびに、ストリーミングメディアの検証を再実行します。 オンデマンドで動作し、継続的なモニタリングは提供されません。
* 実装ガイドスキルは、プランニングにのみ使用してください。 Adobeシステムにアクセスすることも、実装も行うこともありません。

## 次の手順

* 他の分析ドメインとベストプラクティスを含む、Coworker Chatによるデータ分析の概要については、[Coworker Chatによるデータ分析](/help/chat/use-cases/data-insights/analytics-overview.md)を参照してください。
* 共同作業者チャットを設定し、作業例について説明するには、[共同作業者チャットを使用したデータ分析の基本を学ぶ](/help/chat/use-cases/data-insights/analytics-chat.md)を参照してください。
