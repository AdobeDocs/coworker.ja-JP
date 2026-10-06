---
description: Marketo スマートリストと静的リストを同期できるように、Marketo Engage アカウントをCoworker Campaignsに接続する方法について説明します。
title: Marketo Engageに接続
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: dbee38135a5491fd21b65fdbb70ba60d949d7560
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%
---
# Marketo Engageに接続 {#marketo}

Adobe Workfront Campaignsを利用すれば、Marketo Engageアカウントを接続して、スマートリストと静的リストを取得できます。

>[!PREREQUISITES]
>
>このコネクタを使用するには、まず次の要素が必要です。
>
>* アクティブなMarketo Engage アカウント
>* Marketo **インスタンス URL**
>* MarketoのCoworker Campaigns用に[&#x200B; カスタムサービス &#x200B;](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services#custom-services-1)が作成され、その[&#x200B; クライアント IDとクライアントシークレット &#x200B;](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/authentication#creating-an-access-token)が手元にあります

## つながる方法

1. [同僚キャンペーンのホームページ &#x200B;](https://coworker-campaigns.experience.adobe.com/)で、**カスタマイズ**&#x200B;をクリックし、**コネクタ**&#x200B;を選択します。

   ![同僚キャンペーンがナビゲーションを残し、展開をカスタマイズおよびコネクタがハイライト表示される](./assets/marketo-1.png)

1. 「**統合を追加**」をクリックします。

   ![&#x200B; コネクタ画面に統合ボタンを追加](./assets/marketo-2.png)

   >[!NOTE]
   >
   >最初の統合ではない場合は、「コネクタを追加」というボタンが表示されます。

1. Marketo行で、**Connect**&#x200B;をクリックします。

   ![Connect ボタン付きのMarketo コネクタタイル &#x200B;](./assets/marketo-3.png)

1. Marketo **インスタンス URL**、**クライアント ID**、**クライアントシークレット**&#x200B;を入力します。 「**接続**」をクリックします。

   >[!NOTE]
   >
   >My Marketo ページを表示すると、ブラウザーのアドレスバーにMarketo インスタンスのURLが表示されます。

   ![&#x200B; インスタンス URL、クライアント ID、およびクライアント秘密鍵のフィールドを含むMarketo ダイアログの接続](./assets/marketo-4.png)

接続後、Marketoがコネクターリストに表示され、連絡先リストをMarketoから同期にリンクするときに選択できます。

**切断するには：**

1. コネクタ画面で、Marketo タイルを見つけ、**管理**&#x200B;をクリックします。

   ![Marketo タイルに「接続済み」ステータスと「管理」ボタンが表示されているコネクタ画面](./assets/marketo-5.png)

1. 「**切断**」をクリックします（現時点ではクライアント秘密鍵を再入力する必要はありません）。

   ![&#x200B; インスタンス URLおよびクライアント ID フィールドと切断ボタンを含むMarketoの管理ダイアログ &#x200B;](./assets/marketo-6.png)

   >[!NOTE]
   >
   >インスタンス URLが最初に追加されると、デフォルトはREST エンドポイント URLで、`*.mktorest.com`で終わります。

1. 「**切断**」をもう一度クリックして確認します。

   ![接続確認ダイアログの切断](./assets/marketo-7.png)
