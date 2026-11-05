---
title: Adobe Adobe AnalyticsとCustomer Journey Analyticsを利用して、根本原因を分析
description: Adobe CX Enterprise Coworkerを使用して、指標の変化を調査し、寄与するディメンションとセグメントを特定し、Adobe AnalyticsとCJAの仮説をテストします。
feature: AI Tools
role: User
level: Beginner
doc-type: Feature Video
duration: 186
last-substantial-update: 2026-08-10T00:00:00.000Z
jira: KT-22082
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 7e096fc9cda2157c02501ee909a80bf4df9a2f32
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%
---

# [!DNL Adobe Analytics]と[!DNL Customer Journey Analytics]を使用して根本原因を分析する

Adobe CX Enterprise Coworker Chatを使用して、Adobe AnalyticsまたはCustomer Journey Analytics（CJA）で指標が変更された理由を調べます。 指定した変更を分析し、貢献度の大きさやセグメントを表示して、自然言語を使って仮説をテストします。

## 根本原因の分析にCustomer Journey Analyticsのデータを活用

次のビデオでは、Coworkerが会話型AIとCustomer Journey Analyticsをどのように組み合わせているかを示しています。 自然言語で質問する方法、結果を可視化する方法、有意義なトレンドを特定する方法、手作業でクエリを作成することなくパフォーマンスを向上させる要因を明らかにする方法を紹介します。

>[!VIDEO](https://video.tv.adobe.com/v/3496847/?learn=on&enablevpops)

### 前提条件

開始する前に：

1. **同僚チャットにアクセスし、Customer Journey Analyticsに接続します。** 組織が必要な統合を設定していることを確認します。
1. **分析するCJA データ ビューにアクセスできます。** チームメンバーは、利用可能なデータビューとコンポーネントのみを使用できます。
1. **関連する指標とディメンションを含むデータビューを選択します。** 複数のデータビューにアクセスできる場合は、使用するデータビューに名前を付けます。
1. **調査する変更を特定します。** 指標、日付範囲、比較期間を指定します。 また、分析の焦点を絞るためのディメンション、セグメント、仮説を指定することもできます。

### Customer Journey Analyticsのサンプルプロンプト

データビューで、角括弧で囲まれたテキストをコンポーネント名と時間帯に置き換えます。

* **[データビュー名]** データビューで、**[比較日付範囲]**&#x200B;と比較して&#x200B;**[日付範囲]**&#x200B;の間に&#x200B;**[指標]**&#x200B;が変更された理由を教えてください。 **[ディメンション]**&#x200B;ごとに変更を分類し、最も貢献したセグメントを表示します。
* **[データビュー名]** データビューで、**[ディメンションまたはセグメント]**&#x200B;は、**[日付範囲A]**&#x200B;から&#x200B;**[日付範囲B]**&#x200B;までの&#x200B;**[指標]**&#x200B;の減少に貢献しましたか？ 両方の期間の値を比較し、何が変更されたかを説明します。
* **[データビュー名]** データビューで、**[日付範囲]**&#x200B;の&#x200B;**[セグメント A]**&#x200B;と&#x200B;**[セグメント B]**&#x200B;について&#x200B;**[指標]**&#x200B;を比較します。 どのディメンションが違いに最も貢献しましたか？
* **[データビュー名]** データビューで、次の仮説をテストします：**[仮説の状態]**。 **[日付範囲]**&#x200B;の&#x200B;**[指標]**&#x200B;を分析し、それをサポートするディメンションまたはセグメントを表示します。

## 根本原因の分析にAdobe Analyticsのデータを活用

Adobe Analyticsレポートスイートで指標が変更された理由を調査できます。 `aa-root-cause-analysis` スキルを使用して、指定した変更を分析し、その変更に貢献したディメンションとセグメントを特定します。

### 前提条件

開始する前に：

1. **同僚チャットにアクセスし、Adobe Analyticsに接続します。** Coworkerで、**カスタマイズ/統合**&#x200B;に移動し、`aa-mcp`統合が一覧表示され、接続されていることを確認します。 利用できない場合は、管理者に組織の設定を確認するように依頼してください。 設定ガイダンスについては、[同僚チャット &#x200B;](https://experienceleague.adobe.com/ja/docs/coworker/content/chat/use-cases/data-insights/analytics-chat)でのデータ分析の概要を参照してください。
1. **分析するAdobe Analytics レポートスイートにアクセスできます。** CoworkerはAdobe Analyticsの権限を継承し、Analysis Workspaceで使用できるレポートスイートとコンポーネントのみを使用できます。
1. **関連データを含むレポートスイートを選択します。** 複数のレポートスイートにアクセスできる場合は、使用するレポートスイートに名前を付けます。
1. **調査する変更を特定します。** 指標と期間を指定します。 より焦点を絞った分析には、比較期間、関連するディメンションまたはセグメント、同僚にテストしてもらいたい仮説を含めます。

### Adobe Analyticsのサンプルプロンプト

括弧で囲まれたテキストを、レポートスイートのコンポーネント名と期間に置き換えます。

* **[レポートスイート名]** レポートスイートで、**[比較日付範囲]**&#x200B;と比較して&#x200B;**[日付範囲]**&#x200B;の間に&#x200B;**[指標]**&#x200B;が変更された理由は何ですか？ **[ディメンション]**&#x200B;ごとに変更を分類し、最も貢献したセグメントを表示します。
* **[レポートスイート名]** レポートスイートで、**[ディメンションまたはセグメント]**&#x200B;は、**[日付範囲A]**&#x200B;から&#x200B;**[日付範囲B]**&#x200B;までの&#x200B;**[指標]**&#x200B;の減少に貢献しましたか？ 両方の期間の値を比較し、何が変更されたかを説明します。
* **[レポートスイート名]** レポートスイートで、**[日付範囲]**&#x200B;の&#x200B;**[セグメント A]**&#x200B;と&#x200B;**[セグメント B]**&#x200B;について&#x200B;**[指標]**&#x200B;を比較します。 どのディメンションが違いに最も貢献しましたか？

## 関連リソース

* [Adobe Adobe CX Enterprise Coworker Chatでデータを分析](https://experienceleague.adobe.com/ja/docs/coworker/content/chat/use-cases/data-insights/analytics-overview)
* [同僚とのチャットによるデータ分析を始める](https://experienceleague.adobe.com/ja/docs/coworker/content/chat/use-cases/data-insights/analytics-chat)
