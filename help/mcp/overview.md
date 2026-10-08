---
title: Adobe CX Coworker Gatewayの概要
description: Adobe CX Coworker Gatewayは、Adobe CX Enterpriseの統合MCPであり、MCP クライアントにサポートされている製品ツールへのシングルコネクションを提供します。
hide: true
source-git-commit: 6c126810936bea3e883d74e6ff685991cb40cd4a
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 4%
---
# Adobe CX Coworker Gateway {#mcp-overview}

Adobe CX Coworker Gatewayは、Adobe CX Enterpriseの統合モデルコンテキストプロトコル（MCP）です。 MCP互換のクライアントは、1つのコネクションで、組織とアカウントが使用できるAdobe製品ツールにアクセスできます。

>[!IMPORTANT]
>
>**CX Coworker Gateway** ツールを使用する前に、Adobe組織を有効にする必要があります。
>
>組織にまだアクセス権がない場合は、[cx-coworker-gateway-support@adobe.com](mailto:cx-coworker-gateway-support@adobe.com)にメールを送信して、組織のイネーブルメントをリクエストしてください。

すべてのMCP クライアント設定にCX Coworker Gateway エンドポイントを使用します。

```
https://cx-coworker-gateway.adobe.io/mcp
```

接続後、エンドポイントは、Adobe組織と資格情報で利用可能なツールを公開します。 このガイドの製品固有のページでは、各製品ツールで何ができるか、どのようなデータにアクセスできるか、製品固有の制限について説明します。

## モデル コンテキスト プロトコルとは何ですか？ {#mcp-what-is}

MCP （Model Context Protocol）は、AI アプリケーションを外部システムに接続するためのオープンソース標準です。 [!DNL Claude]、[!DNL ChatGPT]、[!DNL Cursor]、[!DNL Claude Code]、[!DNL Codex]、[!DNL VS Code]などのMCP互換クライアントは、これらのツールを使用して、製品コンテキストを取得し、サポートされている操作を実行し、自然言語で回答を返すことができます。

CX Coworker Gatewayは、CX Coworker Gateway製品ツール用の管理エンドポイントを提供します。 製品サーバーを個別に追加する代わりに、エンドポイントに1回接続し、使用権限のあるソリューションに表示される製品ツールを使用します。

## 利用可能な製品ツール {#available-product-tools}

このガイドでは、次の製品ツールについて説明します。


| 製品ツール | エンドポイントを通じて公開される情報 | 対象 | ドキュメント |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **Real-Time CDP** | オーディエンス、宛先、ソース、ID名前空間、アクティベーションの正常性（読み取り専用） | Beta | [Real-Time CDP ツール &#x200B;](rtcdp-mcp.md) |
| **Experience Platform** | スキーマ、データセット、データガバナンス、クエリサービス、監査イベント、オブザーバビリティ指標、サンドボックス正常性チェック評価（読み取り専用） | Beta | [Experience Platform ツール &#x200B;](aep-mcp.md) |
| **Journey Optimizer** | キャンペーン、ジャーニー、チャネル設定（読み取り専用）、コンテンツテンプレート、フラグメント、ランディングページ、インラインメッセージコンテンツ（読み取りと書き込み） | Beta | [Journey Optimizer ツール &#x200B;](ajo-mcp.md) |
| **Customer Journey Analytics** | データビュー、ディメンション、指標、レポート、セグメント、日付範囲、プロジェクト、オーディエンス（読み取りと書き込み） | 使用可能 | [Customer Journey Analytics ツール &#x200B;](cja-mcp.md) |
| **Adobe Analytics** | レポートスイート、ディメンション、指標、レポート、セグメント、日付範囲、ワークスペースプロジェクト（サポートされているコンポーネントの読み取りと書き込み） | 使用可能 | [Adobe Analytics ツール &#x200B;](analytics-mcp.md) |
| **Workfront** | プロジェクト、タスク、承認ワークフローの作業管理ツール | プレビュー | [Workfront MCP サーバー](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview) |


>[!NOTE]
>
>ツールの可用性は、製品ライセンス、組織の有効化、製品の権限、認証に使用されるAdobeの資格情報によって異なります。 MCPは、組織とユーザーアカウントがアクセス権を持つツールのみを表示します。 [CX Coworker Gateway tools](access.md)へのアクセスを参照してください。



## 基本を学ぶ {#mcp-get-started}

1. [CX Coworker Gateway tools](access.md)へのアクセスを確認して、製品の可用性、イネーブルメント、権限を確認します。
2. [CX Coworker Gateway用Adobeのインストール &#x200B;](install.md)に従って、MCP クライアントをエンドポイントに接続します。
3. 使用する各製品ツールの製品ページを確認します。

