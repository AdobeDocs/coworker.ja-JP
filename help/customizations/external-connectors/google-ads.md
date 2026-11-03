---
title: Google Ads外部コネクタ
description: CX Enterprise CoworkerのGoogle Ads外部コネクタを組織に設定し、GoogleでログインしてチャットでGoogle Ads データを使用する方法について説明します。
role: Admin, User
level: Beginner
badgeBeta: label="Beta" type="Informative" tooltip="このコネクタはベータ版です。"
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
hide: true
source-git-commit: 33bbe0ce723fcad4e25353749039c6b81b0dbdf9
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 1%
---

# Google Ads外部コネクタ {#google-ads}

[!DNL Google Ads]外部コネクタを使用して、Adobe CX Enterprise Coworkerで[!DNL Google Ads] データを操作します。 コネクターを設定したら、アクセスできる広告アカウント、使用可能なフィールドと指標、キャンペーンのパフォーマンスを同僚に尋ねます。 コネクタはMCP （Model Context Protocol）サーバです。

>[!AVAILABILITY]
>
>[!DNL Google Ads]外部コネクタはベータ版です。 ドキュメントと機能は変更される場合があります。

## コネクタ設定 {#connector-configuration}

コネクタ設定プロセスには、次の2つの別々の部分があります。

* **組織の設定：**&#x200B;管理者は、組織全体に対して一度コネクタを設定し、メンバーが使用できるツールを選択します。 AdobeはOAuth アプリケーションを提供するので、入力するアプリの資格情報はありません。
* **メンバーのログイン：**&#x200B;各メンバーは、自分の[!DNL Google] アカウントでログインします。 メンバーは、自分の[!DNL Google] アカウントがアクセスできる[!DNL Google Ads] アカウントのみにアクセスできます。

組織設定を保存しても、メンバーはログインせず、[!DNL Google Ads] アカウントへのアクセス権も付与されません。 各メンバーは個別にサインインする必要があります。

## 前提条件 {#prerequisites}

始める前に、次の項目を確認してください。

* **組織のセットアップ用：** Coworkerで組織コネクタを管理する権限を持つアカウント。
* **メンバーのログイン：**&#x200B;使用する予定の[!DNL Google Ads] アカウントにアクセスできる[!DNL Google] アカウント。

## 組織のコネクタの設定 {#configure-organization}

管理者は、組織内のすべてのユーザーが[!DNL Google Ads] コネクタを利用できるようにします。 組織ページの変更は、組織内のすべてのユーザーに適用されます。

1. **[!UICONTROL カスタマイズ]**&#x200B;を開き、**[!UICONTROL 組織]**&#x200B;を選択してから、**[!UICONTROL 外部コネクタ]**&#x200B;を選択します。 **[!UICONTROL Google Ads]** カードで、**[!UICONTROL Configure]**&#x200B;を選択します。

1. 組織の&#x200B;**[!UICONTROL Google Adsの設定]** ダイアログで、**[!UICONTROL OAuth アプリケーション]**&#x200B;が&#x200B;**[!UICONTROL Adobeで管理されているOAuth アプリケーション]**&#x200B;であることを確認します。 Adobeは[!DNL Google Ads] アプリを提供しているので、アプリの資格情報を入力する必要はありません。 ユーザーが利用できる&#x200B;**[!UICONTROL ツール]**&#x200B;で、組織が必要とするツールを選択します。 詳しくは、[使用可能なツール &#x200B;](#available-tools)を参照してください。 **[!UICONTROL 各人が個別にサインインする]**&#x200B;通知を確認し、**[!UICONTROL 接続を保存]**&#x200B;を選択します。

   ![Adobeが管理するOAuth アプリケーションを使用して、Google Ads for your organization ダイアログを構成します。3つのツールをすべて選択し、各担当者が個別にサインインします。](./assets/google-ads/org-configure.png){width="500" zoomable="yes"}

1. 保存された&#x200B;**[!UICONTROL google-ads]** コネクタの詳細を確認します。

   | 設定 | 説明 |
   | --- | --- |
   | **[!UICONTROL ソース]** | 環境のMCP サーバーのURL。 |
   | **[!UICONTROL 認証]** | 認証方法`google-ads_login`。 |
   | **[!UICONTROL ツールポリシー]** | 許可されるツール名またはパターン。 |
   | **[!UICONTROL 接続]** | 自分のサインインステータス。 |

   ![&#x200B; ソース、認証方法、3つの許可されたツールを含むツールポリシー、ログアウトおよび更新ボタンに関連する「署名済み」を示すGoogle-ads コネクタの詳細を保存しました。](./assets/google-ads/org-details.png){width="700" zoomable="yes"}

コネクタの詳細の&#x200B;**[!UICONTROL 接続]** ステータスは、組織ではなく、自分の接続を参照します。 すべてのメンバーは、引き続き自分のアカウントでログインする必要があります。 メンバーがログインしたら、**[!UICONTROL テスト]**&#x200B;を選択してツールの検出をテストできます。 自分でコネクタを使用するには、[&#x200B; メンバーとしてログイン &#x200B;](#sign-in-as-a-member)の手順に従います。

組織へのコネクタの提供を停止するには、コネクタの詳細ページで「**[!UICONTROL 削除]**」を選択します。

### 利用可能なツール {#available-tools}

[!DNL Google Ads] コネクタには、次のツールが用意されています。

| ツール | 説明 |
| --- | --- |
| `customers_list_accessible_customers` | サインインした[!DNL Google] アカウントが直接アクセスできる顧客IDを一覧表示します。 |
| `metadata_get_resource_metadata` | キャンペーンや広告グループなど、[!DNL Google Ads] リソースに使用できるフィールド、指標、セグメントを検索します。 |
| `search_search` | [!DNL Google Ads]設定またはレポートデータを取得します。 |

## メンバーとしてログイン {#sign-in-as-a-member}

管理者がコネクタを設定すると、各メンバーは自分の[!DNL Google] アカウントでサインインします。

1. **[!UICONTROL カスタマイズ]**&#x200B;を開き、**[!UICONTROL ユーザー]**&#x200B;を選択してから、**[!UICONTROL 外部コネクタ]**&#x200B;を選択します。 **[!UICONTROL Google Ads]** カードで、**[!UICONTROL ログイン]**&#x200B;を選択します。

   カードに「**[!UICONTROL 設定されていません]**」と表示されている場合、またはコネクタが使用できない場合は、管理者に[&#x200B; コネクタの設定](#configure-organization)を依頼してください。

1. [!DNL Google] **[!UICONTROL アカウントを選択]**&#x200B;画面で、[!DNL Google Ads] アカウントにアクセスできるアカウントを選択するか、**[!UICONTROL 別のアカウントを使用]**&#x200B;を選択します。 次に、シングルサインオン（SSO）、多要素認証（MFA）、ID検証など、組織が必要とするサインインステップを完了します。

   手順とその順序は、組織とアカウントポリシーによって異なります。

   ![Google Adobe Experience Platformのアカウント画面を選択し、2つの削除済みアカウントと「別のアカウントを使用」オプションを一覧表示します。](./assets/google-ads/member-choose-account.png){width="500" zoomable="yes"}

1. 選択したアカウントと承認中のアプリを確認し、**[!UICONTROL 続行]**&#x200B;を選択します。

   [!DNL Google]はアプリ名を[!DNL Adobe Experience Platform]として表示します。 以前にアプリを使用していた場合、[!DNL Google]は再度ログインしていることを示します。 初めてのユーザーには、異なるプロンプトが表示されることがあります。

   ![Googleの画面で、アカウントが削除され、Adobe Experience Platformに再度ログインする場合と、「キャンセルして続行」ボタンが表示される](./assets/google-ads/member-continue.png){width="500" zoomable="yes"}。

1. アクセス要求を確認し、**[!UICONTROL 続行]**&#x200B;を選択します。

   ![Googleの画面で、Adobe Experience PlatformがGoogle アカウントへのアクセスを希望しており、アカウントが墨消しされている場合、アプリに既に一部のアクセス権が付与されているという通知、および「キャンセル」ボタンと「続行」ボタン &#x200B;](./assets/google-ads/member-consent.png){width="500" zoomable="yes"}

   >[!IMPORTANT]
   >
   >アプリを認識し、組織がリクエストされたアクセスを承認した場合にのみ続行します。

1. [!DNL Google]さんがCoworkerに戻ったら、**[!UICONTROL google-ads]** コネクタの詳細を開きます。 コネクタに「**[!UICONTROL Connected]**」と「**[!UICONTROL Signed in]**」が表示されていることを確認します。

   管理者が別の方法で指示しない限り、**[!UICONTROL リソース ID]**&#x200B;をデフォルト値のままにします。 このフィールドは、ログイン時に送信されるトークンオーディエンスを設定します。 デフォルトに戻すには、フィールドをクリアし、**[!UICONTROL リソース IDを保存]**&#x200B;を選択します。

   ![google-ads コネクタの詳細（接続済みステータス、ログアウトおよび更新ボタンを使用した署名済み接続、およびリソース ID フィールド） &#x200B;](./assets/google-ads/member-connected.png){width="700" zoomable="yes"}

1. 「**[!UICONTROL テスト]**」を選択して、共同作業者がコネクタツールを検出できることを確認します。 次に、管理者&#x200B;**によって有効になっている** ツールを確認して、使用できるツールを表示します。

   **[!UICONTROL テスト]**&#x200B;は、ログイン後に使用できます。

   ![3つのGoogle Ads ツールとその説明を一覧表示する管理者セクションで有効になっているツール。](./assets/google-ads/member-tools.png){width="700" zoomable="yes"}

[!DNL Google] アカウントをコネクタから切断するには、**[!UICONTROL ログアウト]**&#x200B;を選択します。 コネクタの詳細には、**[!UICONTROL ツールタイムアウト]**&#x200B;設定と&#x200B;**[!UICONTROL リフレッシュ]** コントロールも表示されます。

**[!UICONTROL Connected]**&#x200B;のステータスで、特定の広告アカウントへのアクセスが確認されないか、すべてのレポートが正常に実行されます。 アクセスを確認するには、[広告アカウントへのアクセスを確認してください](#check-ad-account-access)。

## 広告アカウントへのアクセスを確認する {#check-ad-account-access}

使用できる[!DNL Google Ads] アカウントを確認するには、チャットを開始し、プロンプトを入力します。

プロンプトの例：

* 「どのGoogle Ads アカウントにアクセスできますか？」

共同作業者は`customers_list_accessible_customers` ツールを使用して、[!DNL Google] アカウントが直接アクセスできる顧客IDを一覧表示します。 これはアカウントアクセスチェックであり、パフォーマンスレポートではありません。 マネージャーアカウントを使用する場合、その下のすべてのアカウントがリストに含まれるわけではありません。

レポートをリクエストする前に、次の操作を行います。

* リストからアカウントを選択します。
* 開始日と終了日を含む日付範囲を指定します。
* レポートで使用できるフィールドと指標を同僚に確認します。

## アクセスのトラブルシューティング {#troubleshoot-access}

[!DNL Google Ads] データにアクセスできない場合は、管理者に次の点を確認してください。

| 面グラフ | 確認すべきこと |
| --- | --- |
| [!DNL Google] アカウント | [!DNL Google Ads] アカウントへのアクセス権を持つ[!DNL Google] アカウントでログインしました。 |
| アカウント権限 | お使いの[!DNL Google] アカウントには、使用する[!DNL Google Ads] アカウントの権限があります。 |
| マネージャーアカウント | マネージャーアカウントを介してアカウントにアクセスする場合、管理者はマネージャーアカウントの設定を確認しました。 |
| ツール選択 | 管理者は、ユーザーが利用できる&#x200B;**[!UICONTROL ツール]**&#x200B;の下で、必要なツールを有効にしました。 |
| リソース識別子 | 管理者が別の方法で指示しない限り、**[!UICONTROL リソース ID]**&#x200B;はデフォルト値を使用します。 |
