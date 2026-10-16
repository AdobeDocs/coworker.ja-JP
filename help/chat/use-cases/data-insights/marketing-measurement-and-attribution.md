---
title: Adobe Workfrontでマーケティングの影響とアトリビューションを測定
description: Adobe Workfront Chatを使用して、各チャネルの増分効果の測定、支出が飽和状態になる場所の特定、What-if予算シナリオの構築、マーケティングモデルの品質のチェックを行います。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: f914f4a123216985ae9b562413f26e7b8c29eb0f
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 2%
---

# マーケティングの測定とアトリビューションの概要

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

Adobe CX Enterprise Coworker Chatを使用して、あらゆるマーケティングチャネルや施策の増分効果を把握できるため、ROIを最適化するために予算を割り当てることができます。 チャネルの連携、追加支出の停止、予算配分の比較などを確認できます。

マーケティングの測定とアトリビューションは、Adobe Workfrontのいくつかの分析領域のひとつです。 すべてのドメインを表示するには、「共同作業者チャットを使用したデータの分析」の「[共同作業者チャットでの分析の開始](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)」を参照してください。

**アナリスト、** ビジネスユーザーに最適

## 前提条件

<!-- FLAG: Confidence: High for the shared bullets (sourced from analytics-chat.md and the Skills and limitations table). They're confirmed for Measure campaign performance only; whether the marketing mix modeling use cases also need a data view or report suite connection is unknown. Low for the "Additional prerequisite" notes on the four marketing mix modeling rows in the Use cases table: incremental impact, response curves, budget scenarios, and model retraining describe a marketing mix model, but no source names the product or data that these use cases need. It could be Adobe Mix Modeler or Marketing Campaign Analytics (listed as an implementation path in implementation-guide.md). Confirm with the PM before publishing. -->

このページのユースケースを使用するには、次のものが必要です。

* Customer Journey AnalyticsデータビューやAdobe Analyticsレポートスイートに接続された共同作業チャット。 [同僚チャット ](/help/chat/use-cases/data-insights/analytics-chat.md)によるデータ分析を開始するを参照してください。
* 分析するデータビューまたはレポートスイートへのアクセスを表示します。 共同作業者チャットは、Customer Journey AnalyticsまたはAdobe Analyticsから権限を継承します。

## ユースケース

| ユースケース | 関数 |
| --- | --- |
| 各チャネルの増分効果の把握 | 各チャネルの増分価値、チャネル間の相互増幅方法、外部要因の役割を示します。<p>**サンプルプロンプト：**</p><ul><li>「最もコンバージョン率が高かったチャネルは？」</li><li>「有料検索とディスプレイはどのように互いに増幅し合うのですか？」</li></ul><p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、このユースケースでは、トレーニングされたマーケティング測定モデルも必要です。 *[製品と設定の要件を確認してください。]*</p> |
| 飽和状態を始める場所を特定する<p>![経費の飽和開始場所を検索](assets/marketing-measurement.png)</p> | 応答曲線を表示して、追加支出がどこで発生しないかを明らかにします。<p>**サンプルプロンプト：**</p><ul><li>「有料検索の支出はどこで飽和し始めますか？」</li><li>「各チャネルの応答曲線を表示」</li></ul><p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、このユースケースでは、トレーニングされたマーケティング測定モデルも必要です。 *[製品と設定の要件を確認してください。]*</p> |
| What-if予算シナリオの構築 | 配分オプションを並べて比較し、計画決定に役立てることができます。<p>**最適：** ビジネスユーザー</p><p>**サンプルプロンプト：**</p><ul><li>「次の四半期の予算シナリオの作成」</li><li>「ディスプレイから検索に支出の10%をシフトしたらどうなるか？」</li></ul><p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、このユースケースでは、トレーニングされたマーケティング測定モデルも必要です。 *[製品と設定の要件を確認してください。]*</p> |
| モデルの品質と再トレーニングのタイミングを確認する | モデルの品質、トレーニングの詳細、スコアリング指標を調査し、回答を信頼する方法を把握できます。<p>**アナリスト：**&#x200B;に最適</p><p>**サンプルプロンプト：**</p><ul><li>「このモデルに必要な他の要素はありますか？」</li><li>「このモデルは再訓練する必要がありますか？」</li></ul><p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、このユースケースでは、トレーニングされたマーケティング測定モデルも必要です。 *[製品と設定の要件を確認してください。]*</p> |
| [施策のパフォーマンスを測定](/help/chat/use-cases/workflows.md#data-insights) | キャンペーン、チャネル、web プロパティの特定の期間におけるパフォーマンスを確認できます。<p>**サンプルプロンプト：** 「Acrobatのweb キャンペーンの先月のパフォーマンスは？」</p><p>詳しくは、「Coworker Chat ユースケースの[ データインサイト ](/help/chat/use-cases/workflows.md#data-insights)」を参照してください。</p> |

## 使用するスキル

<!-- FLAG: Confidence: High for Measure campaign performance (workflows.md lists `cja`, `aa`, `dx-api`, and `knowledge-graph` for "Campaign performance"). `dx-api` and `knowledge-graph` aren't in the Skills and limitations table on analytics-overview.md. Low for the other four use cases: no source names their skills. Get the skill IDs from the PM, replace the placeholder row, and add the skills to the Skills and limitations table. -->

この記事で説明するユースケースでは、次のスキルを使用します。 必要な権限とカバーされていない内容を含む、すべての分析スキルの一覧については、「共同作業者チャットを使用したデータ分析」の[ スキルと制限事項](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。

| スキル | に使用 |
| --- | --- |
| `cja`, `aa`, `dx-api`, `knowledge-graph` | 施策のパフォーマンスを測定 |
| *[確認するスキル]* | 各チャネルの増分効果の把握<br>支出の飽和開始場所を特定<br>What-if予算シナリオを作成<br> モデルの品質とリトレーニングのタイミングを確認する |

## より良い結果を得るためのヒント

<!-- FLAG: Confidence: Medium. The first two bullets are adapted from the best practices in analytics-overview.md. The third bullet is inferred from the sample prompts. -->

* 分析するチャネル、キャンペーン、日付範囲に名前を付けます。
* 2つのチャネルの連携など、既存の仮説を記載することで、Coworker Chatで検証したり、除外したりできます。
* What-if シナリオを構築する際にテストしたい予算の具体的なシフト（支出の10%をあるチャネルから別のチャネルに移動するなど）を示します。

## 次の手順

* 他の分析ドメインとベストプラクティスを含む、Coworker Chatによるデータ分析の概要については、[Coworker Chatによるデータ分析](/help/chat/use-cases/data-insights/analytics-overview.md)を参照してください。
* 共同作業者チャットを設定し、作業例について説明するには、[共同作業者チャットを使用したデータ分析の基本を学ぶ](/help/chat/use-cases/data-insights/analytics-chat.md)を参照してください。
