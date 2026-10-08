---
title: CX Coworker GatewayのCustomer Journey Analytics Tools
description: Adobe CX Coworker Gatewayを通じて使用できるAdobe Customer Journey Analytics ツールについて説明します。
hide: true
source-git-commit: 6c126810936bea3e883d74e6ff685991cb40cd4a
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 4%
---

# Adobe CX Coworker GatewayのCustomer Journey Analytics ツール {#cja-mcp}

Customer Journey Analyticsの製品用ツールを使用して、MCP対応クライアントからデータビューの探索、ディメンションと指標の検出、レポートの実行、選択した分析コンポーネントの管理をおこなえます。 これらのツールは、アカウントに必要なCX Coworker ライセンスと権限がある場合、[Customer Journey Analytics Gateway](overview.md)から利用できます。

>[!AVAILABILITY]
>
>Customer Journey Analytics ツールは、Customer Journey Analytics ライセンスをお持ちのお客様が利用できます。 アクセスは、Adobe Admin Consoleの&#x200B;**MCP Access**&#x200B;権限によって制御されます。 [CX Coworker Gateway tools](access.md)へのアクセスを参照してください。

## 主な機能 {#mcp-capabilities}

Customer Journey Analytics ツールは、MCP クライアントから管理された分析ワークフローをサポートします。 以下を行うことができます。

* データビューを確認し、その設定方法を調べます。
* ディメンション、指標、計算指標、セグメント、日付範囲、オーディエンス、プロジェクトを検索できます。
* ディメンション、指標、日付範囲、セグメントフィルターを使用して、ランクレポートやトレンドレポートを実行できます。
* コンポーネントの定義とコンポーネントの使用状況を確認します。
* 選択した分析コンポーネントとワークスペースプロジェクトを作成または更新します。

>[!IMPORTANT]
>
>読み取り専用の[Real-Time CDP](rtcdp-mcp.md)、[Experience Platform](aep-mcp.md)、および[Journey Optimizer](ajo-mcp.md)製品ツールとは異なり、Customer Journey Analytics ツールには書き込み操作が含まれます。 セグメント、計算指標、日付範囲、プロジェクト、オーディエンスを作成および更新できます。 MCPが開始したすべての変更を確認し、検証してから依存します。

## 利用可能なツール {#mcp-tools}

| 面グラフ | ツール | 説明 |
| --- | --- | --- |
| 設定とガイド | `describeCja` | ツール、ディメンション、指標、セグメント、計算指標、プロジェクト構造のリファレンスガイドを返します。 |
| 設定とガイド | `setDefaultSessionDataViewId` | 後続のツール呼び出しに対するセッションレベルのデフォルトデータビューを設定します。 |
| 発見 | `findDimensions` | セマンティック検索をサポートする使用可能なディメンションを検索します。 |
| 発見 | `findMetrics` | 計算指標を除く、標準およびカスタム指標を検索します。 |
| 発見 | `findCalculatedMetrics` | ユーザーが作成および共有した計算指標を参照します。 |
| 発見 | `findSegments` | 現在のユーザーがアクセスできるセグメントを一覧表示します。 |
| 発見 | `findDateRanges` | 保存された日付範囲コンポーネントを取得します。 |
| 発見 | `findDataViews` | 利用可能なデータビューの検索。 |
| 発見 | `findProjects` | ワークスペース プロジェクトを検索します。 |
| 発見 | `findAudiences` | 使用可能なオーディエンスコンポーネントのリストを表示します。 |
| レポートと分析 | `runReport` | ディメンション、指標、日付範囲、オプションのセグメントフィルターを使用して、ランクレポートを実行します。 |
| レポートと分析 | `searchDimensionItems` | 分類レポートに必要なディメンション値を取得します。 |
| コンポーネントの詳細 | `describeDimension` | 特定のディメンションの詳細なメタデータを表示します。 |
| コンポーネントの詳細 | `describeMetric` | 指標のメタデータと測定の詳細を返します。 |
| コンポーネントの詳細 | `describeSegment` | セグメントの定義と互換性に関する情報を表示します。 |
| コンポーネントの詳細 | `describeCalculatedMetric` | 使用される数式とベース指標を表示します。 |
| コンポーネントの詳細 | `describeProject` | ワークスペースプロジェクトの設定を詳しく説明します。 |
| コンポーネントの詳細 | `describeAudience` | オーディエンスのメタデータと公開ステータスを返します。 |
| コンポーネントの使用 | `listComponentUsage` | コンポーネントを使用頻度でランク付けします。 |
| コンポーネントの使用 | `listFrequentlyUsedWith` | 一般的に組み合わされるコンポーネントを識別します。 |
| コンポーネントの使用 | `listSimilarTo` | 同様の目的を果たす代替コンポーネントを見つけます。 |
| 作成と更新 | `upsertSegment` | 新しいセグメントを作成するか、既存のセグメントを変更します。 |
| 作成と更新 | `upsertCalculatedMetric` | 新しい計算指標を作成するか、既存の計算指標を変更します。 |
| 作成と更新 | `createDateRange` | 再利用可能な日付範囲コンポーネントを作成します。 |
| 作成と更新 | `upsertProject` | 新しいワークスペースプロジェクトを作成するか、既存のワークスペースプロジェクトを変更します。 |
| 作成と更新 | `upsertAudience` | 新しいオーディエンス定義を作成するか、既存のオーディエンス定義を変更します。 |

## サンプルプロンプト {#mcp-use-cases}

| 目標 | プロンプトの例 |
| --- | --- |
| データビューのリスト | 「Customer Journey Analyticsで自分が利用できるデータビューを一覧表示します。」 |
| コンポーネントの詳細 | 「データビュー`[data view name]`で収益に関連する指標を検索します。」 |
| レポートの実行 | 「前四半期の受注月別のトレンド・レポートを実行します。」 |
| 指標の分類 | 「訪問ごとに、デバイスの種類ごとに分類された上位10のマーケティングチャネルを表示します。」 |
| コンポーネントの検査 | 「セグメント `[segment name]`について説明し、その定義を教えてください。」 |
| 使用状況の監査 | 「プロジェクト全体で最も頻繁に使用されるディメンションは？」 |
| セグメントの作成 | 「過去30日間に価格ページを閲覧したユーザー向けのセグメントを作成する」 |

## 製品のコンテキストと権限 {#mcp-context}

お客様のアカウントは、Adobe Admin Consoleのシステム管理者または製品管理者から付与された&#x200B;**MCP アクセス**&#x200B;権限項目を含むCustomer Journey Analytics製品プロファイルに属している必要があります。

製品の権限は引き続き適用されます。 アカウントは、クエリするデータビュー、コンポーネント、プロジェクト、オーディエンスを表示でき、セグメント、計算指標、日付範囲、プロジェクト、オーディエンスの作成や更新などの書き込み操作に対して適切な製品権限を持っている必要があります。

## 動画を見る {#mcp-videos}

**概要**

>[!VIDEO](https://video.tv.adobe.com/v/3486313/?learn=on&enablevpops)

**実施中**

>[!VIDEO](https://video.tv.adobe.com/v/3486314/?learn=on&enablevpops)

## 詳細 {#mcp-more}

完全なツールリファレンスと基本ガイドについては、[Customer Journey Analytics MCP ドキュメント &#x200B;](https://developer.adobe.com/analytics-mcp/docs/cja/){target="_blank"}を参照してください。