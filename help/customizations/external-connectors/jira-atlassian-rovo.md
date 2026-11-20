---
title: Jira / Atlassian Rovo外部コネクタ
description: CX Enterprise CoworkerでJira / Atlassian Rovo外部コネクタを設定し、AtlassianでサインインしてJira作業項目を読み取り、検索する方法について説明します。
role: Admin, User
level: Beginner
badgeBeta: label="Beta" type="Informative" tooltip="このコネクタはベータ版です。"
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
hide: true
source-git-commit: 92e7715a5eb7ab4f8feb7348384c94fabc1b78cf
workflow-type: tm+mt
source-wordcount: '1482'
ht-degree: 1%
---

# Jira / Atlassian Rovo外部コネクタ {#jira-atlassian-rovo}

[!DNL Jira] / [!DNL Atlassian Rovo]外部コネクタを使用して、Adobe CX Enterprise Coworkerで[!DNL Jira]件の作業項目を読み取り、検索します。 コネクタを設定したら、共同作業者に作業項目の検索、詳細の読み取り、Jira Query Language （JQL）を使用した検索を依頼します。 コネクタは、[!DNL Atlassian]によってホストされているモデル コンテキスト プロトコル （MCP） サーバーです。

>[!AVAILABILITY]
>
>[!DNL Jira] / [!DNL Atlassian Rovo]外部コネクタはベータ版です。 ドキュメントと機能は変更される場合があります。

## コネクタ設定 {#connector-configuration}

コネクタ設定プロセスには、次の3つの部分があります。

* **[!DNL Atlassian]の準備：** [!DNL Atlassian]組織の管理者は、CoworkerがURL ドメインをリダイレクトすることを許可し、MCP アクセス ポリシーを確認します。
* **組織の設定：**&#x200B;共同作業者の管理者は、組織全体に対して1回コネクタを設定します。 管理者は、メンバーが使用できる読み取り専用ツールを選択します。
* **メンバーのログイン：**&#x200B;各メンバーは、自分の[!DNL Atlassian] アカウントでログインします。 メンバーは、自分のアカウントが表示権限を持つ[!DNL Jira] データのみにアクセスできます。

組織設定を保存しても、メンバーはログインせず、[!DNL Jira]権限も付与されません。 各メンバーは個別にサインインする必要があります。

コネクタには、共有サービスアカウントまたはAPI トークンオプションがありません。 CoworkerはOAuth アプリケーションを[!DNL Atlassian]に自動的に登録するので、クライアント IDまたはクライアント秘密鍵を入力しないでください。

コネクタ名には[!DNL Atlassian Rovo]が含まれていますが、コネクタは[!DNL Jira]の読み取りおよび検索アクセスのみを要求します。 [!DNL Confluence]、[!DNL Rovo]固有、書き込み、または破壊的なアクセスをリクエストしません。 その他の[!DNL Atlassian] MCP機能は、必ずしもこのコネクタを通じて使用できるわけではありません。

## 前提条件 {#prerequisites}

始める前に、次の項目を確認してください。

* **組織セットアップの場合：** [!DNL Jira] / [!DNL Atlassian Rovo] コネクタが使用可能な組織で、Coworkerで組織コネクタを管理する権限を持つアカウント。
* **[!DNL Atlassian]の準備：** MCP アクセスと同僚のリダイレクト URL ドメインを承認できる[!DNL Atlassian]人の組織管理者。
* **目的の[!DNL Jira]のサイト、プロジェクト、および作業項目にアクセスできる** [!DNL Atlassian]のアカウントで、メンバーがログインする場合。
* **ネットワーク アクセスの場合：** [!DNL Atlassian] IP接続と、その接続を許可するアプリ ポリシーを許可リストに加えるします。 ログインが成功しても、ツールリクエストが許可されていることは確認されません。
* **[!DNL Rovo]が有効になりました：** [!DNL Rovo]は、メンバーがコネクタを使用する前に、お使いの[!DNL Atlassian]組織と対象の[!DNL Jira] サイトに対して有効になっています。 詳しくは、[!DNL Atlassian] ドキュメントの「[Rovo](https://www.atlassian.com/software/rovo/guides/admin-guide/rovo-activation)を有効にする方法」を参照してください。

## [!DNL Atlassian] アクセスを準備 {#prepare-atlassian}

メンバーがログインする前に、[!DNL Atlassian]組織の管理者が[!DNL Atlassian Administration]でアクセスを準備します。

1. [!DNL Atlassian Administration]を開き、目的の組織を選択します。

1. **[!UICONTROL コネクタ]** > **[!UICONTROL アトラシアン MCP サーバー]** > **[!UICONTROL ドメインを追加]**&#x200B;を選択します。

1. 共同作業者設定ダイアログに表示されている&#x200B;**[!UICONTROL リダイレクト URL]**&#x200B;のドメインを追加します。 ダイアログについては、[組織のコネクタの設定](#configure-organization)を参照してください。

   完全なURLを貼り付ける代わりに、[!DNL Atlassian] ドメイン形式のルールに従います。 詳しくは、[!DNL Atlassian] ドキュメントの[使用可能なAtlassian MCP サーバードメイン ](https://support.atlassian.com/security-and-access-policies/docs/available-atlassian-mcp-server-domains/)を参照してください。

1. [!DNL Atlassian]管理者がMCP権限グループ、アプリ ポリシー、およびIP権限許可リストを確認します。 詳しくは、次の[!DNL Atlassian] ドキュメントを参照してください。

   * [各ツールに必要な権限グループとスコープに対して、サポートされているAtlassian MCP ツール ](https://support.atlassian.com/atlassian-ai-gateway/docs/supported-tools/)
   * [認証とIP許可リストに加える用にAtlassian MCP サーバーの設定](https://support.atlassian.com/security-and-access-policies/docs/control-atlassian-mcp-server-settings/)を制御する

設定する環境には、常に同僚ダイアログに表示されるリダイレクト URLを使用してください。 別の環境からリダイレクト URLをコピーしないでください。

## 組織のコネクタの設定 {#configure-organization}

管理者は、組織内のすべてのユーザーが[!DNL Jira] / [!DNL Atlassian Rovo] コネクタを利用できるようにします。 組織ページの変更は、組織内のすべてのユーザーに適用されます。

1. **[!UICONTROL カスタマイズ]**&#x200B;を開き、**[!UICONTROL 組織]**&#x200B;を選択してから、**[!UICONTROL 外部コネクタ]**&#x200B;を選択します。 **[!UICONTROL Jira / Atlassian Rovo]** カードで、**[!UICONTROL Configure]**&#x200B;を選択します。 メンバーは、この接続を設定または削除できません。

1. **[!UICONTROL Connect Jira / Atlassian Rovo]** ダイアログで、修正された&#x200B;**[!UICONTROL サーバーURL]**、`https://mcp.atlassian.com/v2/mcp`を確認します。

   **[!UICONTROL リダイレクト URL]**&#x200B;を確認し、[ アトラシアン アクセスの準備](#prepare-atlassian)の説明に従って、[!DNL Atlassian]管理者がそのドメインを承認していることを確認します。 OAuth資格情報は入力できません。

1. **[!UICONTROL ユーザーが利用できるツール]**&#x200B;で、メンバーが使用できるツールを選択します。 詳しくは、[使用可能なツール ](#available-tools)を参照してください。

   `getAccessibleAtlassianResources` サイト検出ツールが必要で、有効なままです。 他の5つのツールはオプションです。 組織内のすべてのユーザーに対してオプションのツールをブロックするには、そのツールを削除します。 削除したツールを復元するには、**[!UICONTROL すべてのツールを復元]**&#x200B;を選択します。 サイト検出のみを有効にして設定を保存できますが、メンバーは作業項目の読み取りや検索を行うことはできません。

   ![必要なgetAccessibleAtlassianResources ツールと5つのオプション ツールを使用して、サーバーのURL、墨消しされたリダイレクト URL、ユーザーが利用できる6つのツールを表示するJira / Atlassian Rovo接続ダイアログ。](./assets/jira-atlassian-rovo/org-configure.png){width="500" zoomable="yes"}

1. **[!UICONTROL 接続を保存]**&#x200B;を選択し、接続の詳細を確認します。

   各メンバーがサインインすると、コネクタは次のOAuth スコープを要求します。

   | 範囲 | 目的 |
   | --- | --- |
   | `read:me`, `read:account` | メンバーの[!DNL Atlassian] アカウントで認証をサポートします。 |
   | `read:jira:agent-interface` | [!DNL Jira] データを読み取ります。 |
   | `search:jira:agent-interface` | [!DNL Jira] データを検索します。 |
   | `offline_access` | サインイントークンを更新します。 |

   ツールのタイムアウトは60秒です。 最初の接続とツールの検出には時間がかかる場合があります。

### 利用可能なツール {#available-tools}

[!DNL Jira] / [!DNL Atlassian Rovo] コネクタには、次の読み取り専用ツールが用意されています。

| ツール | 説明 | 管理者コントロール |
| --- | --- | --- |
| `getAccessibleAtlassianResources` | アクセスできる[!DNL Atlassian] サイトとクラウド IDを見つけます。 [!DNL Jira] ツールにこのツールが必要です。 | 必須 |
| `atlassianUserInfo` | サインイン ユーザーのアカウント情報を取得します。 | オプション |
| `getJiraIssue` | IDまたはキーで[!DNL Jira]件の作業項目を取得します。 | オプション |
| `searchJiraIssuesUsingJql` | JQLを使用して[!DNL Jira]件の作業項目を検索します。 | オプション |
| `discover` | 追加のツール操作とその入力スキーマを見つけます。 | オプション |
| `executeRead` | コメント、変更履歴、プロジェクト、ボード、スプリントの読み取りなど、`discover`を通じて見つかった読み取り操作を実行します。 | オプション |

>[!IMPORTANT]
>
>`discover`および`executeRead` ツールは、グループとして追加の許可された読み取り操作へのアクセス権をメンバーに付与します。 個々の操作をオフにすることはできません。 このアクセスが組織で受け入れられない場合は、両方のツールを削除します。 コネクタには、書き込み操作（`executeWrite`）または破壊的な操作（`executeDestructive`）は含まれていません。

オプションのツールを削除すると、Coworkerでの利用が制限されます。 コネクタがログイン時に要求するOAuth スコープを減らすことはありません。

各ツールには、特定の[!DNL Atlassian]権限グループとスコープが必要です。 詳しくは、[!DNL Atlassian] ドキュメントの[ サポートされているAtlassian MCP ツール ](https://support.atlassian.com/atlassian-ai-gateway/docs/supported-tools/)を参照してください。

## メンバーとしてログイン {#sign-in-as-a-member}

管理者がコネクタを設定すると、各メンバーは自分の[!DNL Atlassian] アカウントでサインインします。 ログインにクライアント ID、クライアント秘密鍵、またはアクセストークンは必要ありません。

1. **[!UICONTROL カスタマイズ]**&#x200B;を開き、**[!UICONTROL ユーザー]**&#x200B;を選択してから、**[!UICONTROL 外部コネクタ]**&#x200B;を選択します。

1. **[!UICONTROL Jira / Atlassian Rovo]** カードを検索します。 カードに「**[!UICONTROL 未設定]**」と「**[!UICONTROL まだ利用できません」と表示されている場合。 管理者がこの設定を行う必要があります。]**。管理者に[ コネクタの設定](#configure-organization)を依頼してください。 メンバーはコネクタを設定できません。

1. **[!UICONTROL ログイン]**&#x200B;を選択し、対象の[!DNL Jira] サイトへのアクセス権を持つ[!DNL Atlassian] アカウントを使用します。 必要なシングルサインオン（SSO）、多要素認証（MFA）、同意プロンプトを入力します。 同意する前に、要求された読み取りおよび検索アクセスを確認してください。

   >[!IMPORTANT]
   >
   >アプリを認識し、組織がリクエストされたアクセスを承認した場合にのみ続行します。

1. Coworkerに戻り、コネクタの詳細を開きます。 接続はメンバーに対して読み取り専用であり、管理者が有効にしたツールを表示できます。 「**[!UICONTROL 接続をテスト]**」を選択して、接続を確認します。

1. オプションとして、[Jira アクセスの確認](#check-access)の説明に従って、小さな読み取り専用チェックを実行します。

テストが成功しても、[!DNL Jira] サイト、プロジェクト、または作業項目のすべてにアクセスできることが確認されません。

## [!DNL Jira]へのアクセスを確認する {#check-access}

コネクタがデータを読み取れることを確認するには、チャットを開始し、読み取り専用プロンプトを入力します。

プロンプトの例：

* 「Jiraで、自分に割り当てられた最大5つの作業項目を最新の更新で順序付けて検索します。 キーとリンクを含めます。 何も変更しないでください。」

このプロンプトが機能するには、管理者が検索ツールを有効にし、アカウント [!DNL Jira]に作業項目を表示する権限が必要です。

## アクセスのトラブルシューティング {#troubleshoot-access}

ログインまたはアクセスに失敗した場合は、管理者に次の点を確認してください。

| 問題 | 確認すべきこと |
| --- | --- |
| クライアントまたはドメインのログインがブロックされています | 環境のリダイレクト URL ドメインが[!DNL Atlassian Administration]で&#x200B;**[!UICONTROL Atlassian MCP サーバー]**&#x200B;設定の下で承認されていることを確認します。 |
| 同意は成功しますが、ツール呼び出しは拒否されます | [!DNL Jira]権限、MCP権限グループ [!DNL Atlassian]、アプリポリシー、IP権限許可リストを確認します。 各ツールに必要な権限グループについては、[ サポートされているAtlassian MCP ツール ](https://support.atlassian.com/atlassian-ai-gateway/docs/supported-tools/)を参照してください。 |
| JQL検索は失敗しますが、他の読み取りは機能します | 管理者が`searchJiraIssuesUsingJql`を有効にし、接続が`search:jira:agent-interface` スコープを要求していることを確認してください。 |
| 同意が`invalid_request`を返します | 管理者に、接続が[!DNL Jira] スコープに加えて`read:me`と`read:account`を要求していることを確認するように依頼します。 |
| 変更後も古いスコープが表示される | 古いユーザーレベル `jira_login`の認証プロバイダーの上書きは、組織の接続よりも優先される可能性があります。 管理者に、古い上書きのみを更新または削除するように依頼してから、再度ログインしてください。 |
| ツールがありません | 管理者にツールの選択を確認してもらいます。 追加の読み取り操作には、`discover`と`executeRead`の両方、必要なスコープ、適切な権限が必要です。 |
| **[!UICONTROL テスト接続]**&#x200B;の動作が遅いか、タイムアウトしています | ツールの検出には、60秒のツール タイムアウトよりも時間がかかる場合があります。 資格情報を変更する前に、問題が検出の速度が遅いか、ログインに失敗しているかを確認します。 |

ヘルプを求める場合は、パスワード、トークン、認証コード、同意URLを共有しないでください。 スクリーンショットやサポートチケットには含めないでください。
