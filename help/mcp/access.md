---
title: CX Coworker Gateway Toolsへのアクセス
description: Adobe CX Coworker Gateway ツールを使用する前に、製品の可用性、組織の有効化、権限を確認します。
hide: true
source-git-commit: 6c126810936bea3e883d74e6ff685991cb40cd4a
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 4%
---
# CX Coworker Gateway ツールへのアクセス {#mcp-access}

Adobe CX Enterpriseは、単一のMCPを通じて商品ツールを公開しています。 アクセスは製品ツールによって評価されます。関連する製品ツールに対してAdobe組織を有効にし、ユーザーアカウントには、これらのツールが公開する製品データを表示または変更するために必要な製品権限が必要です。

>[!IMPORTANT]
>
>CX Coworker Gateway ツールを使用する前に、Adobe組織を有効にする必要があります。 組織がまだアクセスできない場合は、Adobe アカウントチームに連絡して、組織のイネーブルメントをリクエストしてください。

## アクセス要件 {#mcp-requirements}


| 製品ツール | 対象 | アクセス要件 |
| --- | --- | --- |
| Real-Time CDP | Beta | アクティブなReal-Time CDPライセンス、Adobe組織のBetaイネーブルメント、クエリを実行するオーディエンス、宛先、ソース、ID、アクティベーションリソースを表示する権限。 |
| Experience Platform | Beta | アクティブなExperience Platformライセンス、Adobe組織のBetaイネーブルメント、クエリするスキーマ、データセット、ガバナンス、クエリサービス、監査、サンドボックスリソースを表示する権限。 |
| Journey Optimizer | Beta | アクティブなJourney Optimizerライセンス、Adobe組織に対するBetaのイネーブルメント、キャンペーン、ジャーニー、チャネル設定を表示する権限。 |
| Customer Journey Analytics | 使用可能 | アクティブなCustomer Journey Analytics ライセンスと、Adobe Admin Consoleの&#x200B;**MCP アクセス**&#x200B;権限項目を含む製品プロファイル。 製品権限は、アクセスまたは変更できるデータビュー、コンポーネント、レポート、プロジェクト、オーディエンスを引き続き管理します。 |
| Adobe Analytics | 使用可能 | アクティブなAdobe Analytics ライセンスと、Adobe Admin Consoleの&#x200B;**MCP アクセス**&#x200B;権限項目を含む製品プロファイル。 製品権限は、アクセスまたは変更できるレポートスイート、コンポーネント、レポート、セグメント、日付範囲、プロジェクトを引き続き管理します。 |
| Workfront | プレビュー | アクティブなWorkfront ライセンスとWorkfront MCPの有効化。 [Workfront MCP ドキュメント &#x200B;](https://experienceleague.adobe.com/ja/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview)を参照してください。 |
| ターゲット | Beta | Adobe Experience Platform組織でのActive Target ライセンス。 [Target MCP ドキュメント &#x200B;](https://experienceleague.adobe.com/ja/docs/target/using/mcp/target-mcp-get-started)を参照してください。 |



>[!NOTE]
>
>MCPは、組織と資格情報が使用できるツールのみを表示します。 ログイン後に製品ツールが見つからない場合は、製品ライセンス、組織の有効化、ユーザー権限を確認します。

## 利用申請 {#mcp-request}

Betaまたは限定リリースの製品ツールの場合は、Adobe アカウント担当者にお問い合わせいただき、使用するAdobe for CX Coworker Gateway製品ツールを指定してください。 担当者は、製品のイネーブルメントを調整し、Adobeの準備が整ったことを確認します。

**MCP アクセス**&#x200B;権限項目を使用する一般利用可能な製品ツールについては、システム管理者または製品管理者に、MCP アクセスを含む製品プロファイルにアカウントを追加するように依頼してください。

## 製品内イネーブルメント {#mcp-product-enablement}

一部の製品では、MCPへのアクセスに加えて、製品内でのイネーブルメントや製品固有の権限が必要です。 次に例を示します。

- Adobe AnalyticsとCustomer Journey Analyticsには、Adobe Admin Consoleの&#x200B;**MCP Access**&#x200B;権限項目が必要です。
- Workfront MCP ツールは、Workfront設定から有効になります。
- Beta製品ツールを使用するには、MCPを通じてツールが表示される前に、Adobe組織のイネーブルメントが必要です。

製品ページで、製品固有の権限、コンテキスト要件、制限事項に使用する製品ツールを確認します。

## インストールする前 {#mcp-prerequisites}

MCP クライアントを接続する前に、次のことを確認します。

- Adobeの組織は、必要な商品ツールに対して有効になっています。
- ユーザーアカウントには、使用する予定のデータと操作に必要な製品権限があります。
- サポートされているMCP クライアント （[!DNL Claude]、[!DNL ChatGPT]、[!DNL Cursor]、[!DNL Claude Code]、[!DNL Codex]、または[!DNL VS Code]など）にアクセスできます。
- エンタープライズ版のインストールでは、MCP クライアントの組織設定でコネクタやカスタムアプリを管理できます。

次：[Adobe CX Coworker Gatewayをインストール &#x200B;](install.md)。