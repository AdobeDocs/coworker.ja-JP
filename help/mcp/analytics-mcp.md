---
title: CX Coworker GatewayのAdobe Analytics Tools
description: Adobe CX Coworker Gatewayを通じて使用できるAdobe Analytics ツールについて説明します。
hide: true
source-git-commit: 6c126810936bea3e883d74e6ff685991cb40cd4a
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 5%
---
# Adobe CX Coworker GatewayのAdobe Analytics ツール {#aa-mcp}

Adobe Analytics ツールを使用すると、レポートスイートの検索、ディメンションと指標の検出、レポートの実行、選択した分析コンポーネントの管理を、MCP対応クライアントから行うことができます。 これらのツールは、アカウントに必要なAdobe Analytics ライセンスと権限がある場合に、統合[Adobe CX Coworker Gateway](overview.md)を通じて利用できます。

>[!AVAILABILITY]
>
>分析ツールは、Adobe Analytics ライセンスをお持ちのお客様が利用できます。 アクセスは、Adobe Admin Consoleの&#x200B;**MCP Access**&#x200B;権限によって制御されます。 詳しくは、[CX Coworker Gateway tools](access.md)へのアクセスを参照してください。

## 主な機能 {#mcp-capabilities}

Adobe Analyticsツールは、MCP クライアントからの分析の発見とレポートのワークフローをサポートします。 以下を行うことができます。

- レポートスイートの詳細と設定方法を確認します。
- ディメンション、指標、計算指標、セグメント、日付範囲、ワークスペースプロジェクトを検索できます。
- ディメンション、指標、日付範囲、セグメントフィルターを使用して、ランクレポートやトレンドレポートを実行できます。
- セグメントや日付範囲など、選択した再利用可能なコンポーネントを作成および更新できます。
- 自然言語を使用してAdobe Analyticsデータからインサイトを生成します。

>[!IMPORTANT]
>
>Adobe Analyticsの一部のツールでは、分析コンポーネントを作成または更新できます。 MCPが開始したすべての変更を確認し、検証してから依存します。

## ツールカバレッジ {#mcp-tools}

| 面グラフ | 実行できること |
| --- | --- |
| レポートスイート | アカウントで利用可能なレポートスイートを確認し、設定の詳細を確認します。 |
| コンポーネント | ディメンション、指標、計算指標、セグメント、日付範囲を検索して説明できます。 |
| レポート | 選択したディメンション、指標、日付範囲、セグメントフィルターを使用して、ランクレポートやトレンドレポートを実行できます。 |
| セグメントと日付範囲 | 製品の権限で許可されている再利用可能なセグメントと日付範囲を作成および更新できます。 |
| Workspace プロジェクト | Analysis Workspace プロジェクトの概要を説明します。 |

現在のツールの一覧については、[Adobe Analytics MCP ツール リファレンス ](https://developer.adobe.com/analytics-mcp/docs/aa/reference){target="_blank"}を参照してください。

## サンプルプロンプト {#mcp-use-cases}

| 目標 | プロンプトの例 |
| --- | --- |
| レポートスイートについて | 「アクセスできるレポートスイートのリスト」 |
| コンポーネントを検索 | 「収益に関連する指標を見つける」 |
| レポートの実行 | 「過去7日間のページビュー別ランクレポートを実行します。」 |
| セグメントの検査 | 「セグメント `[segment name]`について説明し、その定義を教えてください。」 |
| プロジェクトを見る | 「私のAnalysis Workspaceの買収に関するプロジェクトをリストアップしてください」 |

## 製品のコンテキストと権限 {#mcp-context}

お客様のアカウントは、Adobe Admin Consoleのシステム管理者または製品管理者から付与された&#x200B;**MCP アクセス**&#x200B;権限項目を含むAdobe Analytics製品プロファイルに属している必要があります。

製品の権限は引き続き適用されます。 アカウントは、クエリを実行するレポートスイート、コンポーネント、レポート、プロジェクトを表示でき、再利用可能なコンポーネントの作成や更新などの書き込み操作に対する適切な製品権限を持っている必要があります。

## 詳細 {#mcp-more}

完全なツールリファレンスと基本ガイドについては、[Adobe Analytics MCP ドキュメント ](https://developer.adobe.com/analytics-mcp/docs/aa/){target="_blank"}を参照してください。