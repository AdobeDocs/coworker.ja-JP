---
title: 同僚とのオンボーディングデータ
description: CX Coworkerのデータオンボーディングスキルを使用して、対話型ワークフローを通じて新しいデータソースをAdobe Experience Platformにオンボーディングする方法について説明します。
hide: true
source-git-commit: 8f7d5307b1928c052f020ca5e7aae3feee7af03e
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 3%
---

# 同僚とのオンボーディングデータ

>[!AVAILABILITY]
>
>データオンボーディングスキルはベータ版です。 ドキュメントと機能は変更される場合があります。
>
>データオンボーディングスキルは、Adobe CX Enterprise Coworkerへのアクセス権を持つお客様が利用できます。組織でも有効にする必要があります。<!-- VERIFY BEFORE PUBLISH: confirm exact permission/entitlement name with Umesh Gohil, PLAT-296546. -->

CX Coworkerのデータオンボーディングスキルを活用して、単一の対話型ワークフローを通じて、新しいデータをAdobe Experience Platformにオンボーディングします。 複数の画面を操作してソースを接続し、スキーマを手作業で作成する代わりに、インテントを記述し、Coworkerがソースの選択、データ品質、セマンティックエンリッチメント、スキーママッピング、スキーマ作成、データフロー作成をガイドします。

<!-- VERIFY BEFORE PUBLISH: confirm the loaded skill name ("Onboard Data to Experience Platform") and the exact post-landing prompt/flow with Umesh Gohil once flag access is arranged. -->

## 前提条件 {#prerequisites}

始める前に、次のことを確認してください。

- 適切な組織やサンドボックスにAdobe Experience Platformからアクセスできます。
- Adobe CX Enterprise Coworkerへのアクセス。自社のデータオンボーディングスキルが有効になっている。
- Adobe Experience Platformでスキーマを作成する権限。

プラグインのインストール手順については、[Coworker UI ガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide)を参照してください。

## データオンボーディングスキルの活用 {#use-the-data-onboarding-skill}

今日、データオンボーディングスキルは、Experience Platform UIでのスキーマ作成から始まります。これにより、既に入力されたインテントを持つCoworkerが開きます。

データオンボーディングスキルを活用するには：

1. Adobe Experience Platformで、**[!UICONTROL Schemas]**&#x200B;に移動し、**[!UICONTROL Create schema]**&#x200B;を選択します。
1. **[!UICONTROL スキーマを作成]** ダイアログで、**[!UICONTROL AIを使用したデータのオンボーディング]**&#x200B;を選択し、**[!UICONTROL 選択]**&#x200B;を選択します。

   ![AI オプションを選択したオンボードデータを使用したスキーマの作成ダイアログ。](./assets/data-onboarding-skill/create-a-schema-dialog.png)

1. CX Coworkerが新しいブラウザータブで開き、スキーマ作成インテントから事前入力されたプロンプトが表示されるので、それを再集計する必要はありません。
1. プロンプトが表示されたときにオンボーディングするソース（例：[!DNL Amazon S3]、[!DNL Data Landing Zone]、[!DNL Delta Share]、または[!DNL Marketo]）を選択します。

   <!-- VERIFY BEFORE PUBLISH: screenshot of the Coworker landing/session-start state does not exist yet anywhere. Capture once flag access is confirmed. -->

1. データ品質のレビュー、セマンティックエンリッチメント、スキーママッピング、スキーマの作成を通じて、Adobe Workfrontの従業員との会話を継続し、必要に応じて各ステップを確認しましょう。

CX Coworkerの使用について詳しくは、[Coworker UI ガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide)を参照してください。

## サポートされるユースケース {#supported-use-cases}

データオンボーディングスキルを活用して、オンボーディングワークフローを改善する方法を解説します。

### ソースの選択と接続

ソースコネクタを手動で検索して設定する代わりに、取り込むデータを記述し、適切なソースを特定するのに役立てることができます。

### データ品質の評価

Coworkerは、スキーマにコミットする前に、選択したソースのデータ品質信号を表示するので、プロセスの早い段階で問題を検出できます。

### データを意味でエンリッチする

Coworkerは、入力フィールドのセマンティックな意味を提案し、生フィールドを標準定義にマッピングする手作業を減らします。

### スキーマのマッピングと作成

共同作業者は、レビュー済みのフィールドを新しいスキーマまたは既存のスキーマにマッピングし、同じ会話の一部としてAdobe Experience Platformで直接作成します。

### データフローの作成

チームメンバーは、継続的にデータを取り込むために必要なデータフローを作成することで、オンボーディングを完了します。

## 次の手順 {#next-steps}

このガイドでは、スキーマの作成からデータオンボーディングスキルを開始する方法と、CX Coworkerで達成できるメリットについて説明します。

Experience Platform UIの手順とアクセス/適格性のシナリオについては、スキーマ UI ガイドの[AIを使用したデータのオンボーディング &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/xdm/ui/resources/schemas#data-onboarding-skill)を参照してください。
