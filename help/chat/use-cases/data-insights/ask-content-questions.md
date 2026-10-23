---
title: 同僚とのチャットによるコンテンツに関する質問
description: 一般的なコンテンツから具体的なコンテンツまで、平易な言葉でCoworker Chatにコンテンツについて質問すると、アナリストの専門知識がなくても正確なContent Analyticsの回答を得ることができます。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: f1ffc050071fc0ca48ae36c7aea8bc66eff2a147
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 3%
---

# コンテンツについて質問する

<!-- FLAG: Confirm with the PM: (1) availability (GA, beta, or experimental) and whether this page needs an AVAILABILITY note or `hide: true` until launch, and (2) any required Coworker entitlement. Content Analytics itself has no separate permission: users get access through data views that are configured for Content Analytics (Access control section of analytics-platform.en/help/content-analytics/config/configuration.md). -->

Adobe Adobe CX Enterprise Coworker Chatを使用すれば、Adobe Content Analyticsからコンテンツに関する正確な回答を得ることができます。 「前四半期に最も売上を伸ばしたヒーロー画像は？」などの具体的な質問や、「どのようなコンテンツを優先すればよいか？」などの一般的な質問を考えてみましょう。 チームメンバーが、質問を的確な分析に転換。

Adobe Content Analyticsのデータがどのように構造化されているかを理解し、経験豊富なアナリストならではのレポートルールを適用します。そのため、Content Analyticsの専門知識がなくても、マーケターやビジネスユーザーは信頼性の高い結果を得ることができます。

その他のコンテンツ パフォーマンスの使用例については、[&#x200B; コンテンツ パフォーマンスの概要](/help/chat/use-cases/data-insights/content-performance.md)を参照してください。

**最適：** ビジネスユーザー、アナリスト

## 前提条件

<!-- FLAG: Confidence: High. The first two bullets match the other data insights pages. The third bullet follows the Content Analytics docs in analytics-platform.en: Content Analytics components are available only in data views that are configured for Content Analytics (report/report.md), and there's no separate Content Analytics permission (config/configuration.md). -->

コンテンツについて質問する場合は、次のことが必要です。

* Customer Journey Analyticsのデータビューに接続された共同作業チャット。 [同僚チャット &#x200B;](/help/chat/use-cases/data-insights/analytics-chat.md)によるデータ分析を開始するを参照してください。
* 分析したいデータビューへのアクセスを表示します。 共同作業者チャットは、Customer Journey Analyticsから権限を継承します。
* Content Analytics用に設定されたデータビュー。 Customer Journey Analytics ガイドの「[Content Analyticsの設定](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/configuration/configuration)」を参照してください。

## コンテンツに質問する

1. Coworkerにログインします。

1. **[!UICONTROL 新しいチャット]**&#x200B;を選択します。

1. テキストフィールドで、コンテンツについて質問します。 次に例を示します。

   **プロンプト**

   > どのようなコンテンツを優先すればよいか？

   <!-- FLAG: The skill includes activation words and phrases, but they weren't provided. Confirm with the PM whether customers need to use specific words to trigger the skill, or whether any content question routes to it automatically. If specific words are needed, list them here. -->

   共同作業者は`analyze-content` スキルを使用してコンテンツの質問に回答します。

1. （条件付き）質問が複数の解釈に対してオープンな場合は、どのコンテンツタイプ、チャネル、日付範囲を意味するかなど、同僚が尋ねる明確な質問に答えてください。

1. 結果の検証：

1. （オプション）同じ会話でフォローアップの質問を行って詳細を確認するか、Analysis Workspaceでビジュアライゼーションを開いて手動コントロールを強化します。 [Analysis Workspaceでビジュアライゼーションを開く](/help/chat/use-cases/data-insights/analytics-chat.md#open-a-visualization-in-analysis-workspace)を参照してください。

## サンプルプロンプト

次の表に、様々なタイプのコンテンツに関する質問のプロンプトの例を示します。 ベースとして使用し、自分のコンテンツに適応させることができます。

| 質問のタイプ | サンプルプロンプト |
| --- | --- |
| 広範または探索的 | <ul><li>「どの種類のコンテンツを優先すればよいですか？」</li><li>「コンテンツのパフォーマンスはどうですか？」</li></ul> |
| 属性レベル | <ul><li>「最もパフォーマンスの高い画像に共通する点は何ですか？」</li><li>「最もエンゲージメントを促進するコンテンツ属性は？」</li></ul> |
| 売上とコンバージョン | <ul><li>「前四半期に最も売上を伸ばしたヒーロー画像は？」</li><li>「このバナーにどれだけの収益が関連付けられているか？」</li></ul> |
| チャネルとオーディエンス | <ul><li>「有料でサイト上で獲得できるクリエイティブテーマはどれですか？」</li><li>「初回訪問者にはどのような画像が適していますか？」</li></ul> |

## Coworkerがコンテンツに関する質問に回答する方法

<!-- FLAG: Confidence: High for the list of what the skill includes, metric matching, filtering pages by Experience ID, and choosing an attribution model per question (sourced from the PM's skill description and feature summary). Medium for the remaining details, which combine the skill description with the Content Analytics component reference in the Customer Journey Analytics guide. The skill's specific query defaults, attribution models, and visualization rules weren't provided. Confirm with the PM before adding them. -->

共同作業者は、次のコンテキストとガードレールを含む`analyze-content` スキルでコンテンツの質問に回答します。 スキルは`cja` スキルとペアになり、同じCustomer Journey Analytics ツールを使用して、Customer Journey Analytics データビューに対するすべてのクエリを実行します。

### デフォルトのクエリと質問の明確化

質問で詳細が示されない場合、スキルは適切なデフォルトを適用します。 スキルが何を意味するのかわからない場合は、推測の代わりに明確な質問をします。

### アセットとエクスペリエンスの指標マッチング

<!-- FLAG: The table covers web and mobile content. Paid media content uses separate summary metrics, such as Impressions, Clicks, and Spend with a reporting-level suffix (for example, Clicks | Asset Summary), that can't be combined with event metrics such as Asset Views (config/paid-media.md in analytics-platform.en). Confirm with the PM how the skill handles paid media, then add a row or note. -->

Content Analyticsでは、アセットとエクスペリエンスの2種類のコンテンツをトラッキングします。 それぞれ独自の指標があります。 スキルは常に、指標と求めるコンテンツのタイプを組み合わせます。

| コンテンツタイプ | 概要 | スキルが使用する指標 |
| --- | --- | --- |
| アセット | 画像などの個別のコンテンツ | アセット表示、アセットクリック、アセットのクリックスルー率（CTR） |
| エクスペリエンス | web ページ上のあらゆるテキスト、またはモバイルアプリ内のテキスト、アセット、CTAの組み合わせ | エクスペリエンスビュー、エクスペリエンスクリック数、エクスペリエンスのクリック率（CTR） |

### Content Analyticsのアーキテクチャ

ここでは、Content Analyticsのデータ構造を理解します。 次に例を示します。

* **エクスペリエンス ID:**&#x200B;特定のページについて質問すると、そのページを識別するコンテンツ エクスペリエンス IDによってスキルがフィルタリングされます。
* **AIが生成した属性：**&#x200B;各アセットとエクスペリエンスは、写真のスタイル、色、トーン、説得戦略などの属性で表されます。 スキルでは、これらの属性を利用して、どのコンテンツが効果的に機能するのかだけでなく、コンテンツが効果的に機能する理由を説明できます。

コンポーネントの完全なリストについては、Customer Journey Analytics ガイドの[Content Analytics コンポーネント &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/report/components)を参照してください。

### 帰属

スキルは、質問に合わせてアトリビューションモデルを選択します。 例えば、画像のクリック数に関する質問と、その画像がどれだけ売上に貢献したかという質問では、異なる回答が返されます。 詳しくは、Customer Journey Analytics ガイドの[&#x200B; アトリビューションモデル &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/attribution/models#attribution-models)を参照してください。

### 一般的な分析とワークフロー

このスキルには、次のような一般的なコンテンツ分析の手順が含まれます。

* 優れたパフォーマンスを発揮するアセットやエクスペリエンスに共通する属性を発見。
* コンテンツ露出をコンバージョンや売上に結びつける。
* web、モバイル、有料メディアのチャネルをまたいだコンテンツ比較。
* それぞれのオーディエンスやセグメントに対して機能するコンテンツを比較する。
* 過剰に利用されている、または過小利用されているコンテンツを特定する。

### ビジュアライゼーション

スキルは、質問とデータに合ったビジュアライゼーションを選択するので、結果を読みやすく、共有しやすくなります。

## より良い結果を得るためのヒント

* 何を求めればよいかわからない場合は、幅広く始めましょう。 ：チームメンバーは、一般的な質問から焦点を絞った分析をおこない、そこから調整できます
* 画像などの個別のアセットなのか、ページなどの全体的なエクスペリエンスなのか、どちらが望んでいるのかがわかったときに判断します。
* 分析する指標と日付範囲（収益の前四半期など）に名前を付けます。
* 比較するセグメント、オーディエンス、チャネルを指定します。
* コンテンツが効果的に機能する理由を把握するには、個々のファイルではなく、画像、テーマ、メッセージなどのコンテンツ属性について確認します。
* 同じデータビューを分析する場合は、Coworker Chat メモリに好みのデータビューを追加します。 「[&#x200B; メモリでのデータビューまたはレポートスイートの環境設定の追加](/help/chat/use-cases/data-insights/analytics-chat.md#add-a-data-view-or-report-suite-preference-in-memory)」を参照してください。

## 次の手順

* コンテンツパフォーマンスの使用例について詳しくは、[&#x200B; コンテンツパフォーマンスの概要](/help/chat/use-cases/data-insights/content-performance.md)を参照してください。
* Content Analyticsについて詳しくは、Customer Journey Analytics ガイドの[Content Analyticsの概要](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/content-analytics/content-analytics)を参照してください。
* ベストプラクティスを含む、同僚チャットによるデータ分析の概要については、[同僚チャットによるデータ分析](/help/chat/use-cases/data-insights/analytics-overview.md)を参照してください。
