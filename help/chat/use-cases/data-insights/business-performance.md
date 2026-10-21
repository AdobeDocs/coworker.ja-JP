---
title: Coworker ChatでビジネスパフォーマンスとKPIを分析
description: Adobe Customer Journey Analyticsなら、同僚とのチャットを通じて指標の変化を把握し、今後の展望を予測できます。また、パフォーマンスレビューを実施し、リピート分析を優れたスキルに転換することができます。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: 5973a87d21b23d7621366108716cbd476e6f66ae
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 2%
---

# ビジネスパフォーマンスの概要

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions. -->

Adobe CX Enterprise Coworker Chatを使用して、ビジネスの状況、指標の変化、方向性、次のステップを把握できます。 主要指標の変化を調査し、それを予測して、関係者が利用できる要約や再利用可能なスキルに変えましょう。

ビジネスパフォーマンスは、Coworker Chatのいくつかの分析領域のひとつです。 すべてのドメインを表示するには、「共同作業者チャットを使用したデータの分析」の「[共同作業者チャットでの分析の開始](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)」を参照してください。

**アナリスト、** ビジネスユーザーに最適

## 前提条件

このページのユースケースを使用するには、次のものが必要です。

* Customer Journey AnalyticsデータビューやAdobe Analyticsレポートスイートに接続された共同作業チャット。 [同僚チャット &#x200B;](/help/chat/use-cases/data-insights/analytics-chat.md)によるデータ分析を開始するを参照してください。
* 分析するデータビューまたはレポートスイートへのアクセスを表示します。 共同作業者チャットは、Customer Journey AnalyticsまたはAdobe Analyticsから権限を継承します。

## ユースケース

| ユースケース | 関数 |
| --- | --- |
| [&#x200B; トレンドと根本原因を探る](/help/chat/use-cases/data-insights/root-cause-analysis.md)<p>![&#x200B; トレンドと根本原因を探る](../../assets/data-validation-aa-cja/trend-line-card.png)</p> | Customer Journey AnalyticsとAdobe Analyticsのデータの傾向と、パフォーマンスの変化を促す要因を手動でのクエリなしで特定します。<p>**サンプルプロンプト：** 「コンバージョンが先週ドロップした理由は何ですか？」</p><p>詳しくは、[Customer Journey Analyticsと共同作業者](/help/chat/use-cases/data-insights/root-cause-analysis.md)を参照してください。</p> |
| [指標が移動した理由を説明](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 変更の背後にあるディメンションとセグメントを表示し、残りを除外する根本原因分析を実行します。<p>**サンプルプロンプト：**</p><ul><li>「火曜日に売上が急増したのはなぜですか？」</li><li>「今月のセッションの変化を引き起こしたのは何ですか？」</li></ul><p>詳しくは、[&#x200B; スキルと制限](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。</p> |
| [業績レビューの準備](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 信頼できる指標を、調査結果や推奨される次のステップを含む、説明されたパフォーマンスストーリーに変換。<p>**サンプルプロンプト：**</p><ul><li>「先月の概要を教えてください」</li><li>「リーダーシップチームのパフォーマンスの概要」</li></ul><p>詳しくは、[&#x200B; スキルと制限](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。</p> |
| [指標が見出しの場所を予測](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 過去のデータから指標をプロジェクトし、ミスが発生するのを把握できるようにします。<p>**サンプルプロンプト：**</p><ul><li>「今後30日間のセッションを予測」</li><li>「売上目標を達成する準備は整っていますか？」</li></ul><p>詳しくは、[&#x200B; スキルと制限](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。</p> |
| [&#x200B; カスタム Customer Journey Analytics スキルの作成](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 繰り返し利用できる分析を、セッション全体で永続的な再利用可能なスキルに変換します。<p>**サンプルプロンプト：** 「この週次売上分析を再利用可能なスキルに変換する」</p><p>**追加の前提条件：** [一般的な前提条件](#prerequisites)に加えて、このユースケースではスキルの管理権限も必要です。</p><p>詳しくは、[&#x200B; スキルと制限](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。</p> |
| [市場で成功した分析を繰り返す](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | ブランド、地域、事業部門をまたいで実証済みの分析アプローチを適用。<p>**アナリスト：**&#x200B;に最適</p><p>**サンプルプロンプト：** 「EMEA データビュー用に週次funnel スキルを実行する」</p><p>詳しくは、[&#x200B; スキルと制限](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。</p> |

## 使用するスキル

<!-- FLAG: Confidence: High for the root cause analysis skills, `cja-executive-summary`, forecasting with `cja` and `aa`, and `cja-skill-creator` for creating skills. All are listed in the Skills and limitations table and in workflows.md. Medium for mapping Repeat successful analysis across markets to `cja-skill-creator`: the row describes running a saved skill, which is inferred. workflows.md also lists `cja-bacom-anomaly-tracker-v2`, `cja-cno-weekly-pulse`, and `cja-reporting` for executive summaries. They're left out because they look org-specific. Confirm with the PM. -->

この記事で説明するユースケースでは、次のスキルを使用します。 必要な権限とカバーされていない内容を含む、すべての分析スキルの一覧については、「共同作業者チャットを使用したデータ分析」の[&#x200B; スキルと制限事項](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。

| スキル | に使用 |
| --- | --- |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | 傾向と根本原因を調べる<br>指標が移動した理由を説明する |
| `cja-executive-summary` | 業績レビューの準備 |
| `cja`, `aa` | 指標の見出し先の予測 |
| `cja-skill-creator` | Customer Journey Analyticsのカスタムスキルを作成<br>市場をまたいで分析を繰り返し成功させる |

## より良い結果を得るためのヒント

* 調査する指標と変更期間に名前を付けます。 根本原因の分析は、既知の期間にわたって既知の指標に対して実行できます。
* 指標の変更の内訳が必要な場合は、貢献度ディメンションを尋ねます。
* 指標を予測する際に、「今後30日間」などの予測範囲を求めます。
* 経営陣やマーケティング部門などの概要に対してオーディエンスを指定し、調査結果を提示する場合は、スライドデッキの概要をリクエストします。
* 最初に分析を完了し、次にCoworker Chatにスキルとして保存してもらいます。 スキルにわかりやすい名前を付け、どのくらいの頻度で再利用する予定かを明記します。

## 次の手順

* 他の分析ドメインとベストプラクティスを含む、Coworker Chatによるデータ分析の概要については、[Coworker Chatによるデータ分析](/help/chat/use-cases/data-insights/analytics-overview.md)を参照してください。
* 根本原因の分析を実際に確認するには、[Customer Journey Analyticsと同僚](/help/chat/use-cases/data-insights/root-cause-analysis.md)を参照してください。
