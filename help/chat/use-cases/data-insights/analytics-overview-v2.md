---
title: Adobe Customer Journey Analyticsのデータを分析する（チャット）
description: Adobe CX Enterprise Coworker Chatを使用してAdobe Customer Journey Analyticsのデータを分析し、ファネルを構築して、カスタマージャーニーのどの段階で顧客が脱落しているのかを把握する方法を紹介します。
hold: true
product_v2:
  internal-label: CX Enterprise Coworker
feature_v2:
  internal-label: CX Enterprise Coworker
source-git-commit: 2bf31c1348054a16ba7e7c0c26c0ff913634aa27
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 1%
---

# Coworker Chatでデータを分析

Adobe CX Enterprise Coworker Chatの概要と、自社のデータを分析する方法について解説します。

Coworker Chatなら、自然言語を使ってAdobe Adobeのプロダクトタスクを自動化し、柔軟なプランニング、カスタマイズ可能なスキル、インテリジェントな実行によってアイデアをすばやくアクションに結び付けることができます。 Coworkerの一般的な詳細については、[CX Enterprise Coworkerの概要](/help/home.md)を参照してください。

>[!VIDEO](https://video.tv.adobe.com/v/3503519/?learn=on&enablevpops)

## データ分析の仕組み

Coworker Chatは、以前はAnalysis Workspaceでのみ可能だった高度なデータ分析を実行できます。 Coworker Chatは、Customer Journey AnalyticsデータビューやAdobe Analyticsレポートスイートからデータにアクセスし、データを検索して、自然言語プロンプトで回答を得ることができます。

Coworker Chatは、Customer Journey AnalyticsまたはAdobe Analyticsから権限を継承します。 Analysis Workspaceで使用できるデータビュー、レポートスイート、ディメンション、指標、セグメントのみにアクセスできます。

Coworker チャットでビジュアライゼーションを作成する場合は、Analysis Workspaceでいつでも開いて、より手動制御を行うことができます。

## 迅速な回答と高度な思考による作業

Coworker Chatは、必要な分析に応じて、次の2つの方法で使用できます。

* **簡単な回答** – 直接の平易な言葉で質問すると、すぐに回答が得られます。 ビジネスユーザーはこの方法でCoworker Chatを使用することが多く、アナリストは関係者に迅速な回答が必要な場合にも使用します。
* **深く考えた作業** - ビジネス上の問題を調査し、原因を除外し、推奨事項を得るために、Coworker Chatと拡張された複数回の会話を行います。 アナリストは通常、このアプローチを利用して、レコメンデーションの前にデータを詳細に分析します。

## 同僚チャットで分析を開始

最初に、知りたいことを分かりやすい言葉で説明しましょう。 Coworker Chatは分析計画を立て、データビューやレポートスイートのクエリを行い、ビジュアライゼーションや概要を作成します。

次のユースケースは、達成したい目標でグループ化されています。 各グループには、最も適した役割がリストされています。

### パフォーマンスを測定

**アナリスト、** ビジネスユーザーに最適

| ユースケース | 関数 |
| --- | --- |
| [Customer Journey AnalyticsとAdobe Analytics データの分析](/help/chat/use-cases/data-insights/analytics-chat.md)<p>![Customer Journey AnalyticsとAdobe Analytics データの分析](../../assets/coworker-funnel-response-card.png)</p> | データビューやレポートスイートに関する自然言語の質問に答え、ファネルやその他のビジュアライゼーションを構築し、顧客が離脱する原因を見つけ出します。 Analysis Workspaceで任意のビジュアライゼーションを開いて、さらに詳しく分析できます。<p>**サンプルプロンプト：** 「過去30日間のページビューを表示する」</p><p>詳しくは、[同僚チャットによるデータ分析の基本を学ぶ](/help/chat/use-cases/data-insights/analytics-chat.md)を参照してください。</p> |
| [ パフォーマンスを比較](#skills-and-limitations) | チャネル、期間、セグメントをまたいで指標を並べて比較できます。<p>**プロンプトの例：** 「月々のチャネル別の収益の比較」</p><p>詳しくは、[ スキルと制限](#skills-and-limitations)を参照してください。</p> |
| [施策のパフォーマンスを測定](/help/chat/use-cases/overview.md#data-insights) | キャンペーン、チャネル、web プロパティの特定の期間におけるパフォーマンスを確認できます。<p>**サンプルプロンプト：** 「Acrobatのweb キャンペーンの先月のパフォーマンスは？」</p><p>詳しくは、「Coworker Chat ユースケースの[ データインサイト ](/help/chat/use-cases/overview.md#data-insights)」を参照してください。</p> |
| [ ファネルの分析](#skills-and-limitations) | マルチステップのコンバージョンファネルを進め、各ステージでの離脱を確認します。<p>**アナリスト：**&#x200B;に最適</p><p>**サンプルプロンプト：** 「チェックアウトfunnelの手順を説明」</p><p>詳しくは、[ スキルと制限](#skills-and-limitations)を参照してください。</p> |

### 指標が変化した理由

**アナリスト：**&#x200B;に最適

| ユースケース | 関数 |
| --- | --- |
| [ トレンドと根本原因を探る](/help/chat/use-cases/data-insights/root-cause-analysis.md)<p>![ トレンドと根本原因を探る](../../assets/data-validation-aa-cja/trend-line-card.png)</p> | Customer Journey AnalyticsとAdobe Analyticsのデータの傾向と、パフォーマンスの変化を促す要因を手動でのクエリなしで特定します。<p>**サンプルプロンプト：** 「コンバージョンが先週ドロップした理由は何ですか？」</p><p>詳しくは、[Customer Journey Analyticsと共同作業者](/help/chat/use-cases/data-insights/root-cause-analysis.md)を参照してください。</p> |
| [運用上の傾向と原因を分析](/help/chat/use-cases/overview.md#data-insights) | オーディエンス、データセット、ジャーニーに関する過去の時系列データをクエリし、変更の原因を特定できます。<p>**管理者、アナリスト：**&#x200B;に最適</p><p>**サンプルプロンプト：** 「過去90日間のオーディエンスサイズの傾向を表示する」</p><p>詳しくは、「Coworker Chat ユースケースの[ データインサイト ](/help/chat/use-cases/overview.md#data-insights)」を参照してください。</p> |

### 将来のパフォーマンスを予測

**アナリスト：**&#x200B;に最適

| ユースケース | 関数 |
| --- | --- |
| [予測指標](#skills-and-limitations) | 売上目標を達成するための進捗状況など、過去のCustomer Journey AnalyticsやAdobe Analyticsのデータから得られた将来の指標値をプロジェクトします。<p>**プロンプトのサンプル：** 「今後30日間のセッションを予測」</p><p>詳しくは、[ スキルと制限](#skills-and-limitations)を参照してください。</p> |

### 関係者とインサイトを共有する

**アナリスト、** ビジネスユーザーに最適

| ユースケース | 関数 |
| --- | --- |
| [ エグゼクティブの概要とKPI ダイジェストの作成](#skills-and-limitations) | 関係者に提供可能なパフォーマンスの概要、レコメンデーション、スライドデッキの概要を作成します。<p>**サンプルプロンプト：** 「先月のエグゼクティブサマリーを教えてください」</p><p>詳しくは、[ スキルと制限](#skills-and-limitations)を参照してください。</p> |

### 実装計画またはアップグレード

**管理者：**&#x200B;に最適

| ユースケース | 関数 |
| --- | --- |
| [実装の計画](/help/chat/use-cases/data-insights/implementation-guide.md)<p>![実装の計画](../../assets/ui-guide-6.png)</p> | Customer Journey Analyticsの実装、Adobe Analyticsからのアップグレード、EdgeでのContent Analytics、Marketing Campaign Analytics、ストリーミングメディアコレクションの設定などについて、パーソナライズされたステップバイステップの計画を作成します。 計画には、所有者、労力の見積もり、依存関係、検証手順などの詳細が含まれます。<p>**サンプルプロンプト：** 「Customer Journey Analyticsの実装の計画を手伝ってください」</p><p>詳しくは、[同僚との実装の計画](/help/chat/use-cases/data-insights/implementation-guide.md)を参照してください。</p> |
| [実装チェックリストを生成](/help/chat/use-cases/data-insights/intelligent-checklist.md)<p>![実装チェックリストを生成](../../assets/data-validation-aa-cja/date-detail.png)</p> | Customer Journey Analyticsの導入計画をCoworker Projectsのチェックリストに変換し、手順の割り当て、ステータスの追跡、承認ゲートの追加を可能にします。<p>詳しくは、[同僚プロジェクトを使用した実装チェックリストの生成](/help/chat/use-cases/data-insights/intelligent-checklist.md)を参照してください。</p> |

### データが正確であることを確認する

**管理者：**&#x200B;に最適

| ユースケース | 関数 |
| --- | --- |
| [Adobe AnalyticsからCustomer Journey Analyticsへのアップグレード時にデータを検証](/help/chat/use-cases/data-insights/data-validation-aa-cja.md)<p>![Adobe AnalyticsからCustomer Journey Analyticsへのアップグレード時にデータを検証](../../assets/data-validation-aa-cja/trend-bar-card.png)</p> | Adobe Analytics レポートスイートとCustomer Journey Analytics データビュー間のディメンション、指標、傾向を比較し、アップグレードをサポートするための修正を推奨します。<p>**管理者、アナリスト：**&#x200B;に最適</p><p>**サンプルプロンプト：** 「AA レポートスイートとCJA データビューの比較」</p><p>詳しくは、「[Adobe AnalyticsからCustomer Journey Analyticsにアップグレードする際にCoworkerでデータを検証する](/help/chat/use-cases/data-insights/data-validation-aa-cja.md)」を参照してください。</p> |
| [ ストリーミングメディア実装の検証](/help/chat/use-cases/data-insights/streaming-media-validation.md)<p>![ ストリーミングメディア実装の検証](../../assets/ui-guide-8.png)</p> | データストリーム、スキーマ、データセット、データビュー、セッションデータを確認して、ストリーミングメディアトラッキングが設定され、データが正しく収集されていることを確認します。<p>**サンプルプロンプト：** 「ストリーミングメディアの実装は全体的にどれくらい正常ですか？」</p><p>詳しくは、[ ストリーミングメディア実装を共同作業者と検証](/help/chat/use-cases/data-insights/streaming-media-validation.md)するを参照してください。</p> |
| [Customer Journey Analyticsのデータセット品質を検証](/help/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md)<p>![Customer Journey Analyticsのデータセット品質を検証](../../assets/data-validation-aep/dataset-validation.png)</p> | Customer Journey Analyticsレポートに使用するデータセットを特定し、スキーマ、ID品質、フィールド品質をチェックすることで、ダッシュボードを構築する前に問題を解決できます。<p>詳しくは、「[Coworkerでのデータ検証スキルを使用したCustomer Journey Analytics データの検証](/help/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md)」を参照してください。</p> |
| [Experience Platformに取り込んだ後のデータの検証](/help/chat/use-cases/data-insights/data-validation-aep.md)<p>![Experience Platformに取り込んだ後のデータの検証](../../assets/data-validation-aep/null-values.png)</p> | Experience Platformのデータセットとフィールドに対して統計チェックとセマンティックチェックを実行し、無効な値やマッピングの問題などのデータ品質の問題を見つけます。<p>**サンプルプロンプト：** 「データセット Electronics サンプル 1000の検証」</p><p>詳しくは、[Experience Platform データを共同作業者と検証](/help/chat/use-cases/data-insights/data-validation-aep.md)するを参照してください。</p> |

### 繰り返す分析の自動化

**アナリスト：**&#x200B;に最適

| ユースケース | 関数 |
| --- | --- |
| [ カスタム Customer Journey Analytics スキルの作成](#skills-and-limitations) | 繰り返し利用できる分析を、セッション全体で永続的な再利用可能なスキルに変換します。<p>**サンプルプロンプト：** 「この週次売上分析を再利用可能なスキルに変換する」</p><p>詳しくは、[ スキルと制限](#skills-and-limitations)を参照してください。</p> |

使用するスキルやサンプルプロンプトなど、これらのユースケースについて詳しくは、[ データインサイトのユースケース ](/help/chat/use-cases/overview.md#data-insights)を参照してください。

## スキルと制限

Customer Journey AnalyticsまたはAdobe Analytics データの分析には、次のスキルを使用できます。

| スキル | 次の目的で使用します | 必要な権限 | 範囲外 |
| --- | --- | --- | --- |
| `cja`, `aa` | Customer Journey Analytics データビュー（`cja`）またはAdobe Analytics レポートスイート（`aa`）をリアルタイムでクエリします。<ul><li>指標、ディメンション、セグメント、データビュー、レポートスイートを取得し</li><li>チャネル、期間、セグメントを並べて比較できます</li><li>マルチステップのfunnelとフォールアウト分析の実行</li><li>過去のトレンドにもとづいて指標を予測する</li></ul> | クエリするデータビューまたはレポートスイートへのアクセスを表示します | <ul><li>データビューまたはレポートスイートコンポーネントの作成または編集</li><li>アクセスできるデータビューまたはレポートスイート以外のデータ</li><li>指標予測を超えた予測モデリング</li></ul> |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | 指標が変化したと報告するだけでなく、変化した理由を探ります。<ul><li>既知の期間における既知の指標の変化を調査する</li><li>変更に貢献したディメンションとセグメントを表示</li></ul> | 分析中のデータビューまたはレポートスイートへのアクセスを表示します | <ul><li>質問していない異常の検出（自動化されたアラートやリアルタイムのアラートはない）</li><li>アクセス権のあるデータビューまたはレポートスイート以外の指標の根本原因分析</li></ul> |
| `cja-executive-summary` | 関係者に配慮したデータ要約の作成：<ul><li>指定した期間のパフォーマンスを要約します</li><li>データに基づいた規範的な推奨事項の生成</li><li>スライドデッキや関係者が読み上げるコンテンツの概要</li></ul> | 概要で説明されているデータビューまたはレポートスイートへのアクセスを表示する | <ul><li>最後のスライド デッキまたはプレゼンテーション ファイルの作成</li><li>アクセス権のないデータビューまたはレポートスイートにまたがる要約</li></ul> |
| `aa-cja-validation` | [!DNL Adobe Analytics]とCustomer Journey Analytics間のデータの比較、監査、調整：<ul><li>レポートスイートとデータビュー間の指標値の比較</li><li>2つのデータソース間の不一致のフラグを立てる</li></ul> | [!DNL Adobe Analytics] レポートスイートと比較されるCustomer Journey Analytics データビューへのアクセスを表示します | <ul><li>データの不整合の根本的な原因を解決する</li><li>[!DNL Adobe Analytics]およびCustomer Journey Analytics以外のデータソースを検証しています</li></ul> |
| `cja-skill-creator` | 再利用可能なスキルが見つかったら、次のステップに進みます。<ul><li>完了した分析を、名前付きの再利用可能なスキルに変換する</li><li>今後のチャットセッションで、保存したスキルを利用できるようにします</li></ul> | スキルの管理 | <ul><li>保存したスキルを他のユーザーと自動的に共有する（組織レベルのスキルライブラリには管理者の設定が必要）</li><li>スキル参照でのデータビューまたはレポートスイートコンポーネントの編集</li></ul> |

## 同僚とのチャットでデータを分析する際のベストプラクティス

### 組織レベルのベストプラクティス

* 自社のアナリストをCoworker Championとして任命します。

* 利用者が利用できるデータやコンポーネントに関連する、プロンプトやスキルのライブラリを作成できます。

* 分析で使用するコンポーネントのみを使用するように、共同作業者チャットを指示する1つ以上のスキルを作成します。 これにより、同僚とのチャットにより、組織内のユーザーに最も関連性の高いデータを提供できます。

* Coworker Chatに質問して簡単に回答を得られるタイミングと、深く考えた作業に使用できるタイミングをユーザーに提供します。

### ユーザーレベルのベストプラクティス

* プランモードを使用します。

  このモードは、複雑なタスクに特に役立ちますが、単純なタスクにも優れた結果をもたらします。同僚は、アクションを起こす前にフォローアップで質問することができるからです。 詳しくは、[ プランモード ](/help/chat/ui-guide.md#plan-mode)を参照してください。

* プロンプトを作成する際には、できるだけ具体的に次のように記述します。

  * 分析するディメンション、指標、日付範囲に名前を付けます。
  * コンポーネントを名前で参照します。
  * 含める、除外、比較するセグメント、オーディエンス、チャネル、デバイスを指定します。
  * Funnel、トレンド、コホートテーブルなど、特定のビジュアライゼーションタイプを設定するかどうかを指定します。
  * 同僚チャットでフォローアップの質問を提案する場合は、次のステップの推奨を尋ねます。
  * 指標を予測する際に、「今後30日間」などの予測範囲を求めます。
  * 既存の仮説を記載しておくことで、Coworker Chatで検証したり、除外したりできます。
  * 指標の変更の内訳が必要な場合は、貢献度ディメンションを尋ねます。
  * 経営陣やマーケティング部門などの概要に対してオーディエンスを指定し、調査結果を提示する場合は、スライドデッキの概要をリクエストします。
  * データの検証時に比較する特定のレポートスイートとデータビューに名前を付けます。
  * まず分析を完了し、次にCoworker Chatにスキルとして保存してもらいます。その際、わかりやすい名前を付け、どのくらいの頻度で再利用する予定かを書き留めます。

* Coworker Chat メモリに標準的な方向を追加します。 例えば、同じデータビューまたはレポートスイートのデータを常に使用する場合は、それをメモリに追加します。 詳しくは、「共同作業チャットを使用したデータ分析の開始」の「[ メモリでのデータビューまたはレポートスイートの環境設定の追加](/help/chat/use-cases/data-insights/analytics-chat.md#add-a-data-view-or-report-suite-preference-in-memory)」を参照してください。

## 次の手順

共同作業者チャットを設定し、作業例について説明するには、[共同作業者チャットを使用したデータ分析の基本を学ぶ](/help/chat/use-cases/data-insights/analytics-chat.md)を参照してください。


