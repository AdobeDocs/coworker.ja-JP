---
description: 生成からメール配信まで、Coworker for teamsが画像にC2PA メタデータを自動的に添付して保存する方法をご確認ください。
title: Coworker for teamsのC2PA メタデータ
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: 7af4950080b8805d94062567bdf4075d1f57fc13
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 27%
---
# Coworker for teamsのC2PA メタデータ {#overview}

生成 AI の透明性に関する新しい法律が制定されつつあり、アドビでは管轄区域をまたいｄ適用される要件への対応に取り組んでいます。 [C2PA メタデータ &#x200B;](https://c2pa.org/)は、Adobeがこれらの法律の要件を満たすために使用する来歴ツールです。

C2PA メタデータは、コンテンツがどのように作成または編集されたかを記録する、耐久性のある目に見えないメタデータです。 Coworker for teamsの生成AI ツールを使用して画像を生成または編集すると、C2PA メタデータが自動的にその画像に添付されます。 お客様の側で操作は必要ありません。

## メールキャンペーンのC2PA メタデータ {#c2pa-metadate-email}

メールキャンペーンで送信された画像はC2PA メタデータを維持するので、受信者は配信されたメールから直接画像の由来と信頼性を確認できます。

## C2PA メタデータを添付するアクション {#actions}

次の表は、Coworker グループ版での画像生成で実行された画像アクションに基づいて、C2PA メタデータが添付されるタイミングを示しています。

| アクション | 説明 | C2PA メタデータは添付されていますか？ | ユースケースの例 |
| --- | --- | --- | --- |
| **画像を生成** | テキストプロンプトや参照画像から新しい画像を作成したり、既存の画像から類似した画像を生成したりできます。 | 常に添付されています。 画像は生成AIによって生成されるので、常に新しいC2PA メタデータを持ちます。 | メールキャンペーン用のバナー画像は、目的のビジュアルを説明するテキストプロンプトから生成されます。 |

## コンテンツタイプとその範囲 {#content-types}

* **画像**：対象とされています。 生成AIで画像を生成すると、C2PA メタデータが添付され、Coworker for Teamsで画像生成によって実行されるトリミング、テキストオーバーレイ、画像オーバーレイ操作を通じて保存されます。
* **テキスト**：該当しません。 コピーの生成、翻訳、ブランド整列の提案など、Coworkerのテキストのみの出力には、C2PA メタデータは必要ありません。

## コンテンツが移動する際の取り扱い {#content-moves}

Coworker for teamsは、サポートされている画像アセットに関連するC2PA メタデータを保持します。 画像にCoworker for teamsに読み込まれたときにC2PA メタデータが含まれている場合、生成されたキャンペーンコンテンツとアウトバウンドメールエクスペリエンスでアセットが使用されるときに、それらの資格情報が保持されます。

## その他のリソース {#resources}

* [生成 AI コンテンツの透明性](https://experienceleague.adobe.com/ja/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency){target="_blank"}
* [Adobe Experience Cloud 生成 AI ユーザーガイドライン](https://www.adobe.com/jp/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}
* [ガードレールと制限](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/content-management/generate-content/gs-generative#generative-guardrails){target="_blank"}
