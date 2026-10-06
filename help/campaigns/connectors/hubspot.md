---
description: HubSpot アカウントをCoworker Campaignsにサービスキーを使用して連絡先リストを同期し、いつでも統合を管理または切断できます。
title: HubSpotへの接続
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: dbee38135a5491fd21b65fdbb70ba60d949d7560
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%
---
# HubSpotへの接続 {#hubspot}

Adobe Coworker Campaignsを使用すると、HubSpot アカウントを接続して連絡先リストを取得できます。

>[!PREREQUISITES]
>
>このコネクタを使用するには、まず次の要素が必要です。
>
>* アクティブなHubSpot アカウント
>* 次のスコープで作成された[ サービスキー](https://developers.hubspot.com/docs/apps/developer-platform/build-apps/authentication/account-service-keys#create-a-service-key)が追加されました：`crm.objects.contacts.read`、`crm.objects.leads.read`、`crm.schemas.contacts.read`、`crm.lists.read`、`crm.export`

## つながる方法

1. [同僚キャンペーンのホームページ ](https://coworker-campaigns.experience.adobe.com/)で、**カスタマイズ**&#x200B;をクリックし、**コネクタ**&#x200B;を選択します。

   ![ コネクタを選択した状態でサイドバーに展開されたカスタマイズメニュー](./assets/hubspot-1.png)

1. 「**統合を追加**」をクリックします。

   ![ コネクタ画面に統合ボタンを追加](./assets/hubspot-2.png)

   >[!NOTE]
   >
   >最初の統合ではない場合は、「コネクタを追加」というボタンが表示されます。

1. HubSpot行で、**Connect**&#x200B;をクリックします。

   ![接続ボタンがハイライト表示されたHubSpot タイル ](./assets/hubspot-3.png)

1. 必要な権限を示すモーダルが表示されます（この記事の上部にある前提条件に記載されています）。 「**続行**」をクリックします。

1. HubSpot **サービスキー**&#x200B;を入力し、**接続**&#x200B;をクリックします。

   ![ サービスキーフィールドと接続ボタンを使用してHubSpot ダイアログを接続](./assets/hubspot-4.png)

接続後、HubSpotはコネクターリストに表示され、連絡先リストをHubSpotから同期にリンクするときに選択できます。

**切断するには：**

1. コネクタ画面で、HubSpot タイルを見つけて、**管理**&#x200B;をクリックします。

   ![HubSpotがハイライト表示された「管理」ボタンに接続されていることを示すコネクタ画面](./assets/hubspot-5.png)

1. 「**切断**」をクリックします（現時点ではサービスキーを再入力する必要はありません）。

   ![切断ボタンがハイライト表示されたHubSpotの管理ダイアログ ](./assets/hubspot-6.png)

1. 「**切断**」をもう一度クリックして確認します。

   ![切断ボタンがハイライト表示された接続確認ダイアログ ](./assets/hubspot-7.png)
