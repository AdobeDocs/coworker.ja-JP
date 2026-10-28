---
title: Adobe Experience Manager SitesでCreativeのパフォーマンスを分析
description: 同僚とのチャットを利用して、共通の優れたコンテンツを見つけ、売上を顧客に表示する画像に結びつけ、チャネルやオーディエンスをまたいでクリエイティブを比較できます。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 312450e09d9252f17cb2b5d471ee33e1a22b9a05
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 1%
---

# コンテンツパフォーマンスの概要

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

Adobe CX Enterprise Coworker Chatを使用すれば、各アセットの属性にもとづいて、どのようなコンテンツが効果的であり、その理由を把握し、優れた施策に投資できます。 どのファイルがクリックされたかだけでなく、どの画像、メッセージ、テーマがチャネルやオーディエンスをまたいでエンゲージメントと収益を促進しているのかを確認できます。

コンテンツのパフォーマンスは、Adobe Workfrontの複数の分析ドメインのひとつです。 すべてのドメインを表示するには、「共同作業者チャットを使用したデータの分析」の「[共同作業者チャットでの分析の開始](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)」を参照してください。

**最適：** ビジネスユーザー

## 前提条件

<!-- FLAG: Confidence: High for the first two bullets (sourced from analytics-chat.md and the Skills and limitations table). High for the third bullet: attribute-level and asset analysis needs Content Analytics components, which are available only in data views that are configured for Content Analytics (report/report.md in analytics-platform.en). This applies whichever skill runs the analysis. It's a shared bullet rather than a table row because it applies to every use case on this page. The SME confirmed (October 2026) that the skill doesn't support paid media yet, so the paid channel use case was rewritten for web and mobile. Support is planned, either in this skill or in a separate add-on skill (not decided). When it ships, consider restoring paid channels to that row with an "Additional prerequisite" note: paid media needs the Paid Media channel enabled in Content Analytics through an Experience Platform paid media source connector, such as Meta Ads or Google Ads, and comparing paid creative with on-site revenue needs custom tracking-key mapping (config/paid-media.md in analytics-platform.en). -->

このページのユースケースを使用するには、次のものが必要です。

* Customer Journey AnalyticsデータビューやAdobe Analyticsレポートスイートに接続された共同作業チャット。 [同僚チャット ](/help/chat/use-cases/data-insights/analytics-chat.md)によるデータ分析を開始するを参照してください。
* 分析するデータビューまたはレポートスイートへのアクセスを表示します。 共同作業者チャットは、Customer Journey AnalyticsまたはAdobe Analyticsから権限を継承します。
* Content Analytics用に設定されたデータビュー。 Customer Journey Analytics ガイドの「[Content Analyticsの設定](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/configuration/configuration)」を参照してください。

## ユースケース

| ユースケース | 関数 |
| --- | --- |
| 優れたコンテンツには何が共通するのかを把握する<p>![共通の勝利コンテンツを検索](assets/content-performance.png)</p> | クリックされたファイルだけでなく、属性レベルでどの画像やメッセージが機能するかを示します。<p>**サンプルプロンプト：**</p><ul><li>「最もパフォーマンスの高い画像に共通する点は何ですか？」</li><li>「最もエンゲージメントを促進するコンテンツ属性は？」</li></ul> |
| 顧客に表示されるコンテンツに売上を関連付け | アルゴリズムによるアトリビューションで、画像の露出を収益、コンバージョン、エンゲージメントに結び付ける。<p>**アナリスト、** ビジネスユーザーに最適</p><p>**サンプルプロンプト：**</p><ul><li>「前四半期に最も売上を伸ばした画像は？」</li><li>「https://www.example.com/images/spring-sale.jpgの画像に関連付けられている売上はどれくらいですか？」</li></ul> |
| クリエイティブをwebとモバイルで比較 | サイトとモバイルアプリでどのビジュアルとテーマが優れているかを、一元的に確認できます。<p>**サンプルプロンプト：**</p><ul><li>「モバイルアプリとサイトでは、どのクリエイティブテーマが優れていますか？」</li><li>「モバイルアプリとサイトでの画像パフォーマンスの比較」</li></ul> |
| 各オーディエンスを動かすビジュアルを把握 | パーソナライゼーションとクリエイティブなブリーフを導くために、各オーディエンスに適したビジュアルを示します。<p>**サンプルプロンプト：**</p><ul><li>「各セグメントに対して最も効果的なビジュアルはどれですか？」</li><li>「初回訪問者にはどのような画像が適していますか？」</li></ul> |

## 使用するスキル

<!-- FLAG: Confidence: Medium. The `analyze-content` skill is a foundational skill for content questions, so it's listed for every use case on this page. Confirm with the PM that it covers all four. -->

この記事で説明するユースケースでは、次のスキルを使用します。 必要な権限とカバーされていない内容を含む、すべての分析スキルの一覧については、「共同作業者チャットを使用したデータ分析」の[ スキルと制限事項](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)を参照してください。

| スキル | に使用 |
| --- | --- |
| `cja`,`analyze-content` <br/> （利用制限あり） | 共通のコンテンツとは何かを見つける<br>売上は、顧客に表示されているコンテンツに帰属します<br>webとモバイルのクリエイティブを比較<br>それぞれのオーディエンスを動かすビジュアルを把握します<p>詳しくは、[ コンテンツに関する質問](/help/chat/use-cases/data-insights/ask-content-questions.md)を参照してください。</p> |

## より良い結果を得るためのヒント

<!-- FLAG: Confidence: High for the first bullet (SME feedback, October 2026). Medium for the rest: the second and third bullets are adapted from the best practices in analytics-overview.md, and the fourth bullet is inferred from the row descriptions. -->

* 特定の画像について質問する場合は、そのURLまたはアセット IDを含めます。 ヒーロー画像やバナーなど、ページ上での役割にもとづいて、画像を識別することはできません。
* 分析する指標と日付範囲（収益の前四半期など）に名前を付けます。
* 比較するセグメント、オーディエンス、チャネルを指定します。
* コンテンツが効果的に機能する理由を把握するには、個々のファイルではなく、画像、テーマ、メッセージなどのコンテンツ属性について確認します。

## 次の手順

* Coworkerがコンテンツに関する質問に回答する方法については、「[ コンテンツに関する質問](/help/chat/use-cases/data-insights/ask-content-questions.md) （限定提供）」を参照してください。
* 他の分析ドメインとベストプラクティスを含む、Coworker Chatによるデータ分析の概要については、[Coworker Chatによるデータ分析](/help/chat/use-cases/data-insights/analytics-overview.md)を参照してください。
* 共同作業者チャットを設定し、作業例について説明するには、[共同作業者チャットを使用したデータ分析の基本を学ぶ](/help/chat/use-cases/data-insights/analytics-chat.md)を参照してください。
