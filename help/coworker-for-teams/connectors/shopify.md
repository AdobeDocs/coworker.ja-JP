---
description: Coworker for teamsを使用すると、Shopify アカウントを接続して顧客とセグメントを取り込むことができます。
title: Shopifyに接続する
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 312450e09d9252f17cb2b5d471ee33e1a22b9a05
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%
---
# Shopifyに接続する {#shopify}

Coworker for teamsを使用すると、Shopify アカウントを接続して顧客とセグメントを取り込むことができます。

>[!PREREQUISITES]
>
>このコネクタを使用するには、まず次の要素が必要です。
>
>* アクティブなShopify アカウント
>* Shopifyの次の権限：`read_customers`
>* Shopify ストアのURLと[管理者API アクセストークン &#x200B;](https://shopify.dev/docs/apps/build/authentication-authorization){target="_blank"}便利

## つながる方法

1. [Coworker for teamsのホームページ &#x200B;](https://coworker-campaigns.experience.adobe.com/){target="_blank"}で、**Context**&#x200B;をクリックし、**Connectors**&#x200B;を選択します。

   ![&#x200B; チームの同僚は、コンテキストが展開され、コネクタが強調表示されたナビゲーションを残しました](./assets/shopify-1.png)

1. 「**統合を追加**」をクリックします。

   ![&#x200B; コネクタ画面に統合ボタンを追加](./assets/shopify-2.png)

   >[!NOTE]
   >
   >最初の統合ではない場合は、「コネクタを追加」というボタンが表示されます。

1. Shopify行で、**Connect**&#x200B;をクリックします。

   ![接続ボタン付きのShopify コネクタタイル &#x200B;](./assets/shopify-3.png)

1. 必要な権限を確認し、**続行**&#x200B;をクリックします。

   ![続行ボタンが表示されたShopifyの必要な権限レビュー画面](./assets/shopify-4.png)

1. Shopify **ストア URL**&#x200B;と&#x200B;**管理者API アクセストークン**&#x200B;を入力します。 「**接続**」をクリックします。

>[!NOTE]
>
>Shopifyで、**Settings** › **Apps** › **Develop apps** › **従来のカスタムアプリを作成** › **Admin API設定** › **必要なスコープを追加**&#x200B;して、Admin API アクセストークンを取得します。

![&#x200B; ストア URLと管理者API アクセストークンのフィールドを含むShopify ダイアログを接続](./assets/shopify-5.png)

接続後、Shopifyがコネクターリストに表示されます。

**切断するには：**

1. コネクタ画面で、Shopify タイルを見つけて、**管理**&#x200B;をクリックします。

1. 「**切断**」をクリックします（現時点では、Admin API アクセストークンを再入力する必要はありません）。

1. 「**切断**」をもう一度クリックして確認します。
