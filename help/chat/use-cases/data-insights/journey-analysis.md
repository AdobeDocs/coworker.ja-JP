---
title: Workfrontで顧客ジャーニーと離脱を分析
description: Adobe Customer Journey Analyticsの共同作業チャット機能を利用すれば、セールスファネルの構築、顧客の離脱の原因の特定、コンバージョンの低下の診断、分析データを通じたジャーニーの比較などをおこなえます。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 312450e09d9252f17cb2b5d471ee33e1a22b9a05
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 2%
---

# ジャーニー分析の概要

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

Adobe CX Enterprise Coworkerのチャット機能を利用して、チャネル、デバイス、セグメントをまたいで、顧客がコンバージョンに至らなかった箇所とその理由を把握できます。 カスタマージャーニーをわかりやすい言葉で説明しましょう。同僚のチャットはfunnelを構築し、各ステップでの離脱を示し、原因を調査するのに役立ちます。

ジャーニー分析は、Adobe Workfrontの複数の分析ドメインのひとつです。 すべてのドメインを表示するには、「共同作業者チャットを使用したデータの分析」の「[共同作業者チャットでの分析の開始](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)」を参照してください。

**アナリスト、** ビジネスユーザーに最適

## 前提条件

このページのユースケースを使用するには、次のものが必要です。

* Customer Journey AnalyticsデータビューやAdobe Analyticsレポートスイートに接続された共同作業チャット。 [同僚チャット &#x200B;](/help/chat/use-cases/data-insights/analytics-chat.md)によるデータ分析を開始するを参照してください。
* 分析するデータビューまたはレポートスイートへのアクセスを表示します。 共同作業者チャットは、Customer Journey AnalyticsまたはAdobe Analyticsから権限を継承します。

## ユースケース

| ユースケース | 関数 |
| --- | --- |
| [Customer Journey AnalyticsとAdobe Analytics データの分析](/help/chat/use-cases/data-insights/analytics-chat.md)<p>![Customer Journey AnalyticsとAdobe Analytics データの分析](../../assets/coworker-funnel-response-card.png)</p> | データビューやレポートスイートに関する自然言語の質問に答え、ファネルやその他のビジュアライゼーションを構築し、顧客が離脱する原因を見つけ出します。 Analysis Workspaceで任意のビジュアライゼーションを開いて、さらに詳しく分析できます。<p>**サンプルプロンプト：** 「過去30日間のページビューを表示する」</p><p>詳しくは、[同僚チャットによるデータ分析の基本を学ぶ](/help/chat/use-cases/data-insights/analytics-chat.md)を参照してください。</p> |
| [顧客が脱落する場所を検索](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 平易な質問からfunnelを構築し、最大のリークをランク付けし、次のステップを提案します。<p>**最適：** ビジネスユーザー</p><p>**サンプルプロンプト：**</p><ul><li>「どこで買い物に行く途中で人々を失っているのか？」</li><li>&quot;チェックアウトfunnelを通して私を歩く&quot;</li></ul><p>詳しくは、[&#x200B; スキルと制限](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。</p> |
| コンバージョン率の低下の診断 | 顧客がどこで離脱したかを調査し、変化に貢献した要因を評価します。<p>**サンプルプロンプト：**</p><ul><li>「先週、コンバージョンが下がったのはなぜですか？」</li><li>「サイトの変更後、顧客はどこで離脱しましたか？」</li></ul> |
| 脱落の原因の特定 | ルールアウトにより、問題の背後にあるチャネル、デバイス、またはセグメントが1つずつ分離されます。<p>**サンプルプロンプト：**</p><ul><li>「モバイルやデスクトップでのカート放棄の状況は悪化していますか？」</li><li>「買い物かごと購入の間に最もリークするチャネルはどれですか？」</li></ul> |
| 期間をまたいだジャーニーの比較 | 発送した変更内容がfunnelに移動したかどうかをステップバイステップで表示します。<p>**最適：** ビジネスユーザー</p><p>**サンプルプロンプト：**</p><ul><li>「今四半期のチェックアウトコンバージョンと最後のチェックアウトコンバージョンの比較」</li><li>「リニューアル後、私のfunnelはどのように変わりましたか？」</li></ul> |

## 例：顧客の脱落する箇所の特定

最初の質問からレコメンデーションまでの完全な会話例については、「[例：顧客が脱落する場所を見つける](/help/chat/use-cases/data-insights/analytics-chat.md#example-find-where-customers-drop-off)」の「同僚チャットによるデータ分析の開始」を参照してください。

## 使用するスキル

<!-- FLAG: Confidence: High for `cja` and `aa` (the Skills and limitations table lists funnel and fallout analysis and side-by-side comparison of time periods). Medium for the root cause analysis skills: workflows.md maps the prompt "Why did conversions drop last week?" to them, but the mapping to the slide rows "Diagnose conversion declines" and "Isolate the cause of a drop-off" is inferred. Confirm with the PM. -->

この記事で説明するユースケースでは、次のスキルを使用します。 必要な権限とカバーされていない内容を含む、すべての分析スキルの一覧については、「共同作業者チャットを使用したデータ分析」の[&#x200B; スキルと制限事項](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。

| スキル | に使用 |
| --- | --- |
| `cja`, `aa` | Customer Journey AnalyticsとAdobe Analyticsのデータを分析<br>顧客が離脱した場所を特定<br>期間ごとのジャーニーを比較 |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | コンバージョンの低下を診断<br>脱落の原因を特定 |

## より良い結果を得るためのヒント

<!-- FLAG: Confidence: High, except the first bullet (Medium), which moved here from Prerequisites and is inferred from how funnel prompts work. The rest are adapted from the best practices in analytics-overview.md. -->

* 製品ページ、カート、チェックアウト、購入など、分析するジャーニーのステップに名前を付けます。
* 分析するディメンション、指標、日付範囲に名前を付け、コンポーネントを正確な名前で参照します。
* Funnelやフォールアウトビジュアライゼーションが必要な場合は、それらを選択してください。
* 含める、除外または比較するセグメント、チャネル、デバイスを指定します。
* 最近のサイト変更など、既存の仮説をすべて記載することで、Coworker Chatで検証したり、除外したりできます。
* 同僚チャットでフォローアップの質問を提案する場合は、次のステップの推奨を尋ねます。
* 手動制御を必要とする場合は、Analysis Workspaceで任意のビジュアライゼーションを開きます。 [Analysis Workspaceでビジュアライゼーションを開く](/help/chat/use-cases/data-insights/analytics-chat.md#open-a-visualization-in-analysis-workspace)を参照してください。

## 次の手順

* 他の分析ドメインとベストプラクティスを含む、Coworker Chatによるデータ分析の概要については、[Coworker Chatによるデータ分析](/help/chat/use-cases/data-insights/analytics-overview.md)を参照してください。
* 共同作業者チャットを設定し、作業例について説明するには、[共同作業者チャットを使用したデータ分析の基本を学ぶ](/help/chat/use-cases/data-insights/analytics-chat.md)を参照してください。
