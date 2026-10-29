---
title: Adobe Workfrontの共同作業チャットによる、オーディエンスと顧客セグメントの比較
description: Adobe Customer Journey Analyticsのコラボレーションチャット機能を利用すれば、顧客グループの比較、見落とされていた成長機会の発見、オーディエンスの傾向の追跡、インサイトの活用が可能なオーディエンスに変わります。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 1ec3a8bf6dff44df068529cf1f7ceb699a027d65
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 2%
---

# オーディエンスとセグメント分析の概要

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions. -->

Adobe CX Enterprise Coworker Chatを使用すれば、それぞれのカスタマーグループが異なる行動をとっているかどうかを把握し、最も重要なグループに集中できます。 チャネル、期間、セグメントを並べて比較し、オーディエンスが時間の経過とともにどのように変化するかを追跡して、見つかったものを構築できるオーディエンスに変えます。

オーディエンスとセグメント分析は、Adobe Workfrontの複数の分析ドメインのひとつです。 すべてのドメインを表示するには、「共同作業者チャットを使用したデータの分析」の「[共同作業者チャットでの分析の開始](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)」を参照してください。

**アナリスト、** ビジネスユーザーに最適

## 前提条件

<!-- FLAG: Confidence: High for the shared bullets (sourced from the Skills and limitations table and analytics-chat.md). Medium for the "Additional prerequisite" notes on the operational trends rows in the Use cases table: workflows.md lists the operational time-series skill as available for "All Eligible Applications" but doesn't state required permissions. Mapping Track audience size trends to the same requirement is inferred. Low for the "Additional prerequisite" note on the Take an insight into an audience row: inferred from the Audiences section of workflows.md, which lists Real-Time CDP as the application for audience creation. Confirm with the PM. -->

このページのユースケースを使用するには、次のものが必要です。

* Customer Journey AnalyticsデータビューやAdobe Analyticsレポートスイートに接続された共同作業チャット。 [同僚チャット &#x200B;](/help/chat/use-cases/data-insights/analytics-chat.md)によるデータ分析を開始するを参照してください。
* 分析するデータビューまたはレポートスイートへのアクセスを表示します。 共同作業者チャットは、Customer Journey AnalyticsまたはAdobe Analyticsから権限を継承します。

## ユースケース

| ユースケース | 関数 |
| --- | --- |
| [&#x200B; パフォーマンスを比較](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | チャネル、期間、セグメントをまたいで指標を並べて比較できます。<p>**プロンプトの例：** 「月々のチャネル別の収益の比較」</p><p>詳しくは、[&#x200B; スキルと制限](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。</p> |
| [顧客グループの比較](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | セグメントロジックを記述することなく、どのグループが異なる動作をするかを示します。<p>**最適：** ビジネスユーザー</p><p>**サンプルプロンプト：**</p><ul><li>「有料のソーシャル訪問者は、メールとは異なるコンバージョンをおこないますか？」</li><li>「新規訪問者とリピート訪問者を収益で比較」</li></ul><p>詳しくは、[&#x200B; スキルと制限](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。</p> |
| 見落とされていた成長機会を発見 | オーディエンス、ジャーニー、チャネルを調査し、全体的なパフォーマンス指標で隠すことができる機会を特定します。<p>**サンプルプロンプト：**</p><ul><li>「平均以上のコンバージョン率を上げていても、トラフィックが少ないオーディエンスはどれか？」</li><li>「コンバージョン率が低いチャネルはどれか？」</li></ul> |
| [運用上の傾向と原因を分析](/help/chat/use-cases/workflows.md#data-insights) | オーディエンス、データセット、ジャーニーに関する過去の時系列データをクエリし、変更の原因を特定できます。<p>**管理者、アナリスト：**&#x200B;に最適</p><p>**サンプルプロンプト：** 「過去90日間のオーディエンスサイズの傾向を表示する」</p><p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、この使用例では、分析するオーディエンス、データセット、ジャーニーへのアクセスも必要です。</p><p>詳しくは、「Coworker Chat ユースケースの[&#x200B; データインサイト &#x200B;](/help/chat/use-cases/workflows.md#data-insights)」を参照してください。</p> |
| オーディエンスサイズの傾向を追跡 | 拡大しているオーディエンスや縮小しているオーディエンスを特定し、原因を調べます。<p>**管理者、アナリスト：**&#x200B;に最適</p><p>**サンプルプロンプト：** 「今四半期で最も成長したオーディエンスはどれですか？」</p><p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、このユースケースでは、追跡するオーディエンスへのアクセスも必要です。</p> |
| Insightをオーディエンスに取り込む | Insightから始めて、構築できるオーディエンスに移行します。<p>**サンプルプロンプト：**</p><ul><li>「この比較をAnalysis Workspaceで開く」</li><li>「このグループからオーディエンスを作成するのに役立つ」</li></ul><p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、このユースケースでは、Real-Time Customer Data Platformへのアクセスとオーディエンスを作成するための権限も必要です。</p> |

## 使用するスキル

<!-- FLAG: Confidence: High for Compare performance and Analyze operational trends and causes (skills listed for "Comparative analysis" and "Operational time-series & causal analysis" in workflows.md). Medium for Compare customer groups and Track audience size trends, which are mapped to the same skills based on their descriptions. Low for `audience-creation-flow`: inferred from the Audiences section of workflows.md. No skill is listed for Find overlooked growth opportunities because no source names one. Only `cja`, `aa`, and the root cause analysis skills currently appear in the Skills and limitations table on analytics-overview.md. -->

この記事で説明するユースケースでは、次のスキルを使用します。 必要な権限とカバーされていない内容を含む、すべての分析スキルの一覧については、「共同作業者チャットを使用したデータ分析」の[&#x200B; スキルと制限事項](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。

| スキル | に使用 |
| --- | --- |
| `cja`, `aa` | パフォーマンスの比較<br>顧客グループの比較 |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | パフォーマンスを比較 |
| `operational-stats-causal-analysis` | 運用上の傾向を分析して原因を特定<br> オーディエンスサイズの傾向を追跡 |
| `audience-creation-flow` | Insightをオーディエンスに取り込む |

## より良い結果を得るためのヒント

* 含める、除外する、または比較するセグメント、オーディエンス、チャネル、デバイスを指定します。
* セグメントやその他のコンポーネントを、その正確な名前で参照します。
* 収益の月数など、比較する指標と日付範囲に名前を付けます。
* あるグループが別のグループと異なる行動をする理由を知りたい場合は、貢献度ディメンションを尋ねます。

## 次の手順

* 他の分析ドメインとベストプラクティスを含む、Coworker Chatによるデータ分析の概要については、[Coworker Chatによるデータ分析](/help/chat/use-cases/data-insights/analytics-overview.md)を参照してください。
* Coworker Chatで直接オーディエンスを構築するには、[Experience Platformの健全性を評価し、Coworkerと自然言語でオーディエンスを構築する](/help/chat/use-cases/audiences/create-audience-from-natural-language.md)を参照してください。
