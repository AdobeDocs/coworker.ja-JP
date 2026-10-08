---
title: Adobe CX Coworker Gatewayのインストール
description: MCP互換クライアントをAdobe CX Coworker Gatewayに接続する方法を説明します。
hide: true
source-git-commit: 6c126810936bea3e883d74e6ff685991cb40cd4a
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 0%
---
# Adobe CX Coworker Gatewayのインストール {#mcp-install}

このガイドでは、MCP互換クライアントをAdobe CX Coworker Gatewayに接続する方法について説明します。  CX Coworker Gatewayは、すべての文書化された製品ツールに対して1つのエンドポイントを使用します。

```
https://cx-coworker-gateway.adobe.io/mcp
```

インストールする前に、組織とユーザーアカウントが必要な製品ツールにアクセスできることを確認してください。 [CX Coworker Gateway tools](access.md)へのアクセスを参照してください。

## インストールの動作 {#mcp-install-how}

CX Coworker Gatewayは、ブラウザーベースのAdobe サインインフローでリモート HTTP トランスポートを使用します。 サポートされているすべてのクライアントでは、設定パターンは同じです。

1. エンドポイント URL `https://cx-coworker-gateway.adobe.io/mcp`を追加します。
2. 接続を保存または有効にします。
3. クライアントが初めてツールを呼び出すときに、ブラウザーベースのAdobe ログインを完了します。
4. ツールで必要に応じて、セッションの製品コンテキスト（すべての製品の整理、Experience Platformベースのツールのサンドボックス、Customer Journey Analyticsのデータビュー）を設定します。 ツール呼び出しについては、[製品コンテキスト ](#mcp-connect-params)を参照してください。

>[!NOTE]
>
>MCP クライアント設定では、API キー、ベアラートークン、クライアントシークレット、追加ヘッダーは必要ありません。 認証は、初回使用時にAdobeのサインインフローを通じて処理されます。

## エンタープライズインストール（管理者管理） {#mcp-install-enterprise}

ほとんどのチームおよびエンタープライズ MCP クライアントプランでは、組織用のカスタムコネクタを追加するために管理者が必要です。 これらの環境では、インストールには2つの手順があります。

1. 管理者は、CX Coworker Gateway エンドポイントを1回追加します。
2. 各ユーザーがコネクタを有効にし、独自のAdobe資格情報でログインします。

### 手順1：管理者がエンドポイントを追加する {#mcp-install-enterprise-admin}

管理者は、`https://cx-coworker-gateway.adobe.io/mcp`をカスタムコネクタまたはリモート MCP サーバーとしてクライアントの組織設定に追加します。 正確な場所はクライアントによって異なります。

#### Claude Team and Enterprise {#mcp-install-enterprise-claude}

[!DNL Claude]のTeam プランおよびEnterprise プランでは、組織レベルのコネクタはワークスペース **オーナー**&#x200B;または&#x200B;**プライマリオーナー**&#x200B;によって管理されます。

1. [!DNL Claude]に&#x200B;**所有者**&#x200B;または&#x200B;**プライマリ所有者**&#x200B;としてログインします。
2. **設定** > **管理** > **コネクタ**&#x200B;に移動します。 一部のプランでは、**組織の設定** > **コネクタ**&#x200B;と表示されます。
3. 「**カスタムコネクタを追加**」を選択します。
4. サーバーURLとして`https://cx-coworker-gateway.adobe.io/mcp`を入力し、「CX Coworker Gateway用Adobe」などの認識可能な名前を使用します。
5. コネクタを保存します。

#### ChatGPT チームとエンタープライズ {#mcp-install-enterprise-chatgpt}

[!DNL ChatGPT] チームおよびエンタープライズ ワークスペースでは、ワークスペース管理者がコネクタを追加します。

1. ワークスペース管理者として[!DNL ChatGPT]にログインします。
2. **設定** > **コネクタ**&#x200B;に移動します。 一部のプランでは、**設定** > **アプリとコネクタ**&#x200B;と表示されます。
3. 「**コネクタを追加**」を選択します。
4. サーバーURLとして`https://cx-coworker-gateway.adobe.io/mcp`を入力します。
5. コネクタを保存します。 ワークスペースの設定によっては、この手順で開発者モードを有効にしたり、ワークスペースレベルの承認を付与したりする必要がある場合があります。

#### その他の組織で管理されている顧客 {#mcp-install-enterprise-other}

組織管理のリモートコネクタをサポートする他のクライアントの場合は、`https://cx-coworker-gateway.adobe.io/mcp`を使用してCX Coworker Gatewayをリモート HTTP MCP サーバーとして追加します。 オプションのヘッダー、ベアラートークンのフィールド、クライアント ID フィールド、およびクライアント秘密鍵のフィールドは、クライアントがプレースホルダー値を必要としない限り空のままにします。

### 手順2: ユーザーがコネクタを有効にする {#mcp-install-enterprise-user}

管理者がCX Coworker Gatewayを追加すると、各ユーザーは自分のアカウントに対して次の操作を実行できます。

1. クライアントで個人用コネクタ、アプリ、またはMCP設定を開きます。
2. CX Coworker Gateway コネクタを見つけて有効にします。
3. 会話を開始し、Adobe ツールのいずれかを呼び出し、プロンプトが表示されたら、ブラウザーベースのAdobe ログインを完了します。
4. ツールで必要に応じて、セッションの製品コンテキスト（すべての製品の整理、Experience Platformベースのツールのサンドボックス、Customer Journey Analyticsのデータビュー）を設定します。 ツール呼び出しについては、[製品コンテキスト ](#mcp-connect-params)を参照してください。

管理者が既に組織のコネクタを追加している場合、ユーザーはURLを自分で入力する必要はありません。

## 個人用インストール（セルフサービス） {#mcp-install-individual}

個人プラン、ローカルに設定された開発者クライアント、またはメンバーが独自のコネクタを追加できる組織を使用する場合は、独自のクライアント設定にエンドポイントを直接追加します。

### クロード・パーソン {#mcp-install-individual-claude}

個人版プランの`claude.ai`および[!DNL Claude] デスクトップの場合：

1. **設定** > **コネクタ**&#x200B;を開きます。
2. 「**カスタムコネクタを追加**」を選択します。
3. サーバーURLとして`https://cx-coworker-gateway.adobe.io/mcp`を入力します。
4. コネクタを保存して有効にしてから、最初に使用する際にAdobeのサインインフローを完了します。

### ChatGPT個人版 {#mcp-install-individual-chatgpt}

1. **設定** > **コネクタ**&#x200B;を開きます。 一部のプランでは、**設定** > **アプリとコネクタ**&#x200B;と表示されます。
2. 「**コネクタを追加**」を選択します。
3. サーバーURLとして`https://cx-coworker-gateway.adobe.io/mcp`を入力します。
4. コネクタを保存して有効にしてから、最初に使用する際にAdobeのサインインフローを完了します。

### カーソル {#mcp-install-individual-cursor}

1. **設定** > **MCP**&#x200B;を開きます。
2. 「**新しいサーバーを追加**」を選択します。
3. サーバーURLとして`https://cx-coworker-gateway.adobe.io/mcp`を入力します。
4. **Connect**&#x200B;を選択し、Adobeのサインインフローを完了します。

接続後、CX Coworker Gateway ツール用のAdobeというタイトルが、カーソルのコンポーザーモードとエージェントモードで使用できるようになります。

### クロード・コード {#mcp-install-individual-claude-code}

ターミナルからエンドポイントを追加します。

```bash
claude mcp add --transport http cx-enterprise https://cx-coworker-gateway.adobe.io/mcp
```

次に、[!DNL Claude Code]を開始して実行します：

```text
/mcp
```

`cx-enterprise` サーバーを選択し、ブラウザーでAdobe サインインフローを実行します。

### Codex {#mcp-install-individual-codex}

ターミナルからエンドポイントを追加します。

```bash
codex mcp add cx-enterprise --url https://cx-coworker-gateway.adobe.io/mcp
```

認証：

```bash
codex mcp login cx-enterprise
```

設定を確認します。

```bash
codex mcp list
```

エンドポイントを`~/.codex/config.toml`に直接追加することもできます。

```toml
[mcp_servers.cx-enterprise]
url = "https://cx-coworker-gateway.adobe.io/mcp"
```

### 一般的なJSON設定 {#mcp-install-individual-json}

JSON ベースのMCP サーバー設定を受け入れるクライアントの場合、クライアントがネイティブリモート HTTPをサポートしているか、ローカルブリッジを必要とするかに応じて、次のいずれかの形式を使用します。

**`mcp-remote` ブリッジ経由**

```json
{
  "mcpServers": {
    "cx-enterprise": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://cx-coworker-gateway.adobe.io/mcp"
      ]
    }
  }
}
```

**ネイティブ リモート HTTP**

```json
{
  "mcpServers": {
    "cx-enterprise": {
      "url": "https://cx-coworker-gateway.adobe.io/mcp",
      "transport": "http"
    }
  }
}
```

### その他の顧客 {#mcp-install-individual-other}

リモート MCPをサポートする他のデスクトップまたはweb クライアントの場合は、`https://cx-coworker-gateway.adobe.io/mcp`を使用してAdobe for CX Coworker Gatewayをリモート HTTP サーバーとして追加します。 オプションのヘッダー、ベアラートークンのフィールド、クライアント ID フィールド、およびクライアント秘密鍵のフィールドは、クライアントがプレースホルダー値を必要としない限り空のままにします。

## ツールコールの製品コンテキスト {#mcp-connect-params}

MCPは、アクティブな1つのAdobe組織に対するすべてのツール呼び出しをスコープします。 それ以外のコンテキスト要件は、製品によって異なります。

- **Experience Platform ベースの製品** — Real-Time CDP、Experience Platform、およびJourney Optimizer ツールは、Experience Platform サンドボックス内で動作します。 サンドボックスはセッションごとに1回設定し、3つはすべて共有します。
- **その他の製品** — Experience Platform上に構築されていない製品では、サンドボックスコンテキストは使用されません。 Adobe Analytics、Customer Journey Analytics、Workfront、Marketo、Targetの各ツールは、Customer Journey AnalyticsのデータビューやAdobe Analyticsのレポートスイートなど、独自の製品リソースに対して処理されます。

セッションの開始時にコンテキストを1回設定：各プロダクトツールは、セッションの途中で組織、サンドボックス、データビューを切り替えません。 組織、サンドボックス、データビューのコンテキストを設定するツールについては、[ セッションコンテキストツール ](context-tools.md)を参照してください。

例：

> このセッションには、組織`1234ABCD@AdobeOrg`、サンドボックス `prod`、データビュー`My Company — Global`を使用します。」

必要な値がわからない場合は、MCP クライアントに対して、Adobe資格情報で使用可能な組織、サンドボックス、またはデータビューのリストを取得するように依頼します。