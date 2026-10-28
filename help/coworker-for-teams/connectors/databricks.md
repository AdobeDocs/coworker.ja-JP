---
description: Coworker for teamsを使用すると、Databricks ワークスペースでUnity カタログテーブルを接続してクエリし、キャンペーンオーディエンスを構築してアクティブ化できます。
title: Databricksへの接続
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: bd7454ee46cb1ee4ca8b7ae6ab07348a23854979
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%
---
# Databricksへの接続 {#databricks}

Coworker for teamsを使用すると、Databricks ワークスペースでUnity カタログテーブルを接続してクエリし、キャンペーンオーディエンスを構築してアクティブ化できます。

>[!PREREQUISITES]
>
>このコネクタを使用するには、まず次の要素が必要です。
>
>* アクティブなDatabricks アカウント
>* Databricks Workspace ホスト、[SQL warehouse path](https://docs.databricks.com/aws/en/compute/sql-warehouse/create){target="_blank"}、[個人アクセストークン ](https://learn.microsoft.com/en-us/azure/databricks/dev-tools/auth/pat){target="_blank"}、[Unity カタログ ](https://learn.microsoft.com/en-us/azure/databricks/discover/database-objects){target="_blank"}を便利に利用できます。

## つながる方法

1. [Coworker for teamsのホームページ ](https://coworker-campaigns.experience.adobe.com/){target="_blank"}で、**Context**&#x200B;をクリックし、**Connectors**&#x200B;を選択します。

   ![ チームの同僚は、コンテキストが展開され、コネクタが強調表示されたナビゲーションを残しました](./assets/databricks-1.png)

1. 「**統合を追加**」をクリックします。

   ![ コネクタ画面に統合ボタンを追加](./assets/databricks-2.png)

   >[!NOTE]
   >
   >最初の統合ではない場合は、「コネクタを追加」というボタンが表示されます。

1. Databricks行で、**Connect**&#x200B;をクリックします。

   ![接続ボタン付きDatabricks コネクタタイル ](./assets/databricks-3.png)

1. Databricks **Workspace host**、**SQL warehouse path**、**個人アクセストークン**、**Unity カタログ**&#x200B;を入力します。 「**接続**」をクリックします。

   >[!NOTE]
   >
   >Databricksのホームページでは、ブラウザーのアドレスバーにWorkspace ホストが直接表示されます。 その他のすべての資格情報を見つけるには、この記事の上部にある&#x200B;**前提条件**&#x200B;のリンクを参照してください。

   ![Databricks ダイアログに、Workspace ホスト、SQL ウェアハウス パス、個人アクセストークン、およびUnity カタログのフィールドを接続](./assets/databricks-4.png)

接続後、コネクターリストにDatabricksが表示されます。

**切断するには：**

1. コネクタ画面で、Databricks タイルを見つけて、**管理**&#x200B;をクリックします。

1. 「**切断**」をクリックします（現時点では、個人アクセストークンを再入力する必要はありません）。

1. 「**切断**」をもう一度クリックして確認します。
