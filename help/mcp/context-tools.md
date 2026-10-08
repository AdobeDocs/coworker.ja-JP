---
title: CX Coworker Gatewayのセッションコンテキストツール
description: すべてのCX Coworker Gateway ツール呼び出しの整理、サンドボックス、データビューのコンテキストを設定するコアツールについて説明します。
hide: true
source-git-commit: 6c126810936bea3e883d74e6ff685991cb40cd4a
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 1%
---
# Adobe CX Coworker Gatewayのセッションコンテキストツール {#mcp-core}

Adobe CX Coworker Gatewayには、Adobeの組織、Adobe Experience Platform サンドボックス、Customer Journey Analytics データビューを設定するセッションコンテキストツールのセットが含まれています。これらのツールは、他のすべてのプロダクトツールで動作します。 追加のライセンスや有効化は必要ありません。これらのツールは、[CX Coworker Gateway サーバー](overview.md)に接続した後、すべての認証済みユーザーが使用できます。

## コンテキストの仕組み {#mcp-core-how}

CX Coworker Gatewayは、1つのアクティブなAdobe組織に対するすべてのツール呼び出しをスコープします。 それ以外のコンテキスト要件は、製品によって異なります。

- **Experience Platform ベースの製品** — [Real-Time CDP](rtcdp-mcp.md)、[Experience Platform](aep-mcp.md)、[Journey Optimizer](ajo-mcp.md) ツールは、Experience Platform サンドボックス内で動作します。 `core-set_sandbox`のセッションごとに1回サンドボックスを設定します。3つはすべて共有します。
- **その他の製品** — Experience Platform上に構築されていない製品では、サンドボックスコンテキストは使用されません。 例えば、[Customer Journey Analytics](cja-mcp.md)個のツールはデータビューに対して解決され、[Adobe Analytics](analytics-mcp.md)個のツールはレポートスイートに対して解決されます。

セッションの開始時にコンテキストを1回設定：各プロダクトツールは、セッションの途中で組織、サンドボックス、データビューを切り替えません。

## 利用可能なツール {#mcp-core-tools}

| ツール | 説明 |
| --- | --- |
| `core-list_orgs` | 認証済みユーザーがアクセスできるAdobe組織を一覧表示します。 各組織の表示名と`@AdobeOrg`識別子を返します。 `core-switch_org`を呼び出す前に組織IDを検索する場合に使用します。 |
| `core-switch_org` | セッションのアクティブなAdobe組織を設定します。 以降のすべてのツール呼び出しは、セッションが終了するか、組織が再度切り替わるまで、この組織に対してスコープが設定されます。 |
| `core-list_sandboxes` | アクティブな組織で使用可能なExperience Platform サンドボックスの一覧が表示されます。 各サンドボックスの名前、タイトル、タイプ（実稼動または開発）、状態を返します。 `core-set_sandbox`を呼び出す前にサンドボックス名を検索する場合に使用します。 |
| `core-set_sandbox` | セッションのアクティブなExperience Platform サンドボックスを設定します。 Real-Time CDP、Experience Platform、Journey Optimizerの各ツールでは、このサンドボックスにデータがスコープされます。 |
| `core-list_dataviews` | 現在のコンテキストで認証済みユーザーが使用できるCustomer Journey Analytics データビューを一覧表示します。 データビューIDと表示名を返します。 `core-set_dataview`を呼び出す前にデータ ビューを検索する場合に使用します。 |
| `core-set_dataview` | セッションのデフォルトのCustomer Journey Analytics データビューを設定します。 設定すると、`findDimensions`、`findMetrics`、`runReport`などのデータビューを必要とするCJA ツールは、個々のツール呼び出しで別のデータビューが指定されない限り、この値を自動的に使用します。 |

## 一般的なセッション設定 {#mcp-core-setup}

製品ツールを呼び出す前に、セッションの開始時にコンテキストを設定します。

1. **組織** — `core-list_orgs`に電話してアクセス可能な組織を一覧表示し、次に`core-switch_org`にターゲット組織IDを指定します。
2. **サンドボックス** — Real-Time CDP、Experience Platform、またはJourney Optimizer ツールを使用する場合は、`core-list_sandboxes`に電話して、使用可能なサンドボックスを一覧表示してから、対象のサンドボックス名を付けて`core-set_sandbox`してください。
3. **データビュー** （CJAのみ） – Customer Journey Analytics ツールを使用する場合は、`core-list_dataviews`に電話して使用可能なデータビューを一覧表示し、選択したデータビューで`core-set_dataview`します。

MCP クライアントに、1つの自然言語リクエストでこの設定を完了するように依頼できます。

> このセッションには、組織`1234ABCD@AdobeOrg`、サンドボックス `prod`、データビュー`My Company — Global`を使用します。」

クライアントは適切なツールを呼び出し、コンテキストが設定されたら確認します。

>[!TIP]
>
>Adobe資格情報が1つの組織のみに属している場合、`core-list_orgs`と`core-switch_org`は引き続き機能しますが、有効な組織は同じになります。 Real-Time CDP、Experience Platform、またはJourney Optimizer ツールを使用する場合は`core-set_sandbox`に、Customer Journey Analytics ツールを使用する場合は`core-set_dataview`に電話する必要があります。

## サンプルプロンプト {#mcp-core-examples}

| 目標 | プロンプトの例 |
| --- | --- |
| 利用可能な組織を見つける | 「どのAdobe組織にアクセスできますか？」 |
| 組織コンテキストの設定 | 「組織`My Org (1234ABCD@AdobeOrg)`に切り替えます。」 |
| 利用可能なサンドボックスの確認 | 「現在の組織で使用可能なサンドボックスをリストアップします。」 |
| サンドボックスコンテキストの設定 | 「このセッションには`prod` サンドボックスを使用します。」 |
| 利用可能なデータビューの確認 | 「どのCustomer Journey Analytics データビューにアクセスできますか？」 |
| データビューのコンテキストの設定 | 「デフォルトのデータビューとして`My Company — Global`を設定します。」 |
| セッションの完全設定 | 「組織`1234ABCD@AdobeOrg`、サンドボックス `prod`、データビュー`My Company — Global`を使用してセッションを設定します。」 |

## 関連ページ {#mcp-core-related}

- [Adobe CX Coworker Gatewayをインストール &#x200B;](install.md) – 製品コンテキストの設定セクションを含む、MCP クライアントを接続する方法。
- [CX Coworker Gateway tools](access.md)へのアクセス – 製品別のアクセス要件。