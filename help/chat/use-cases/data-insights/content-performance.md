---
title: Adobe Experience Manager SitesでCreativeのパフォーマンスを分析
description: 同僚とのチャットを利用して、共通の優れたコンテンツを見つけ、売上を顧客に表示する画像に結びつけ、チャネルやオーディエンスをまたいでクリエイティブを比較できます。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: e3d485f7cd1c45bf3fd1217ffcceeccfd4242c7b
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 1%
---

# コンテンツパフォーマンスの概要

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

Adobe CX Enterprise Coworker Chatを使用すれば、各アセットの属性にもとづいて、どのようなコンテンツが効果的であり、その理由を把握し、優れた施策に投資できます。 どのファイルがクリックされたかだけでなく、どの画像、メッセージ、テーマがチャネルやオーディエンスをまたいでエンゲージメントと収益を促進しているのかを確認できます。

コンテンツのパフォーマンスは、Adobe Workfrontの複数の分析ドメインのひとつです。 すべてのドメインを表示するには、「共同作業者チャットを使用したデータの分析」の「[共同作業者チャットでの分析の開始](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)」を参照してください。

**最適：** ビジネスユーザー

## 前提条件

<!-- FLAG: Confidence: High for the first two bullets (sourced from analytics-chat.md and the Skills and limitations table). Low for the third bullet: the attribute-level and image exposure descriptions suggest that these use cases rely on Content Analytics data in Customer Journey Analytics, and implementation-guide.md lists Content Analytics as an implementation path, but no source confirms this. It's a shared bullet rather than a table row because it would apply to every use case on this page. The paid channel row ("Compare Meta ad creative to our web banners") may need an additional data source, which would become an "Additional prerequisite" note on that row in the Use cases table. Confirm with the PM. -->

このページのユースケースを使用するには、次のものが必要です。

* Customer Journey AnalyticsデータビューやAdobe Analyticsレポートスイートに接続された共同作業チャット。 [同僚チャット &#x200B;](/help/chat/use-cases/data-insights/analytics-chat.md)によるデータ分析を開始するを参照してください。
* 分析するデータビューまたはレポートスイートへのアクセスを表示します。 共同作業者チャットは、Customer Journey AnalyticsまたはAdobe Analyticsから権限を継承します。
* Adobe Customer Journey AnalyticsでContent Analyticsを設定し、Adobe Workfrontでコンテンツの属性や画像の露出を分析できるようにします。 Content Analyticsの実装を計画するには、[Coworkerを使用した実装の計画](/help/chat/use-cases/data-insights/implementation-guide.md)を参照してください。

## ユースケース

| ユースケース | 関数 |
| --- | --- |
| 優れたコンテンツには何が共通するのかを把握する<p>![共通の勝利コンテンツを検索](assets/content-performance.png)</p> | クリックされたファイルだけでなく、属性レベルでどの画像やメッセージが機能するかを示します。<p>**サンプルプロンプト：**</p><ul><li>「最もパフォーマンスの高い画像に共通する点は何ですか？」</li><li>「最もエンゲージメントを促進するコンテンツ属性は？」</li></ul> |
| 顧客に表示されるコンテンツに売上を関連付け | アルゴリズムによるアトリビューションで、画像の露出を収益、コンバージョン、エンゲージメントに結び付ける。<p>**アナリスト、** ビジネスユーザーに最適</p><p>**サンプルプロンプト：**</p><ul><li>「前四半期に最も売上を伸ばしたヒーロー画像は？」</li><li>「このバナーにどれだけの収益が関連付けられているか？」</li></ul> |
| ペイドチャネルとオウンドチャネルを跨いだクリエイティブの比較 | web、モバイル、有料チャネルをまたいで、どのビジュアルとテーマが優れているかを一元的に確認できます。<p>**サンプルプロンプト：**</p><ul><li>「有料でサイト上で獲得できるクリエイティブテーマはどれですか？」</li><li>「Metaとクリエイティブをweb バナーと比較する」</li></ul> |
| 各オーディエンスを動かすビジュアルを把握 | パーソナライゼーションとクリエイティブなブリーフを導くために、各オーディエンスに適したビジュアルを示します。<p>**サンプルプロンプト：**</p><ul><li>「各セグメントに対して最も効果的なビジュアルはどれですか？」</li><li>「初回訪問者にはどのような画像が適していますか？」</li></ul> |

<!--
HIDDEN until the skills are confirmed. To publish, remove this comment wrapper.

## Skills used

FLAG: Confidence: Low. No source in the repo (workflows.md, the Skills and limitations table, or any data insights article) names the skills behind these use cases. Get the skill IDs from the PM, replace the placeholder rows, and add the skills to the Skills and limitations table on analytics-overview.md so that the link above the table covers them. When you unhide this section, wrap this FLAG note in its own HTML comment.

Coworker uses the following skills for the use cases described in this article. For a list of all analytics skills, including the permissions they require and what they don't cover, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) in Analyze data with Coworker Chat.

| Skill | Used for |
| --- | --- |
| *[Skill to be confirmed]* | Find what winning content has in common<br>Attribute revenue to the content customers see<br>Compare creative across paid and owned channels<br>Know which visuals move each audience |

-->

## より良い結果を得るためのヒント

<!-- FLAG: Confidence: Medium. The first two bullets are adapted from the best practices in analytics-overview.md. The third bullet is inferred from the row descriptions. -->

* 分析する指標と日付範囲（収益の前四半期など）に名前を付けます。
* 比較するセグメント、オーディエンス、チャネルを指定します。
* コンテンツが効果的に機能する理由を把握するには、個々のファイルではなく、画像、テーマ、メッセージなどのコンテンツ属性について確認します。

## 次の手順

* 他の分析ドメインとベストプラクティスを含む、Coworker Chatによるデータ分析の概要については、[Coworker Chatによるデータ分析](/help/chat/use-cases/data-insights/analytics-overview.md)を参照してください。
* 共同作業者チャットを設定し、作業例について説明するには、[共同作業者チャットを使用したデータ分析の基本を学ぶ](/help/chat/use-cases/data-insights/analytics-chat.md)を参照してください。
