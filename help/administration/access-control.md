---
title: 同僚のアクセス制御
description: 互換性のあるAdobe製品におけるAdobe CX Enterprise Coworkerのアクセス制御と権限について説明します。 管理者コントロールを検索し、アクセスに関するヘルプを表示します。
last-substantial-update: 2026-11-04
level: beginner
role: Admin
jira: KT-22980
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: a14bd350d7259294368acdcb08549ea6e084f1c1
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%
---
# 同僚のアクセス制御 {#access-control}

Adobe CX Enterprise Coworkerのアクセス制御を使用して、Coworkerを使用できるユーザーとそのユーザーが使用できる機能を管理します。

>[!NOTE]
>
>この機能を使用するには、組織を有効にする必要があります。 アクセス制御は段階的に利用できるようになり、起動時にすべてのCoworker組織で有効にできない場合があります。 詳しくは、[同僚チャットの概要](https://experienceleague.adobe.com/ja/docs/coworker/content/chat/overview)を参照してください。

## アクセスの決定方法 {#how-access-is-determined}

同僚のアクセスは、組織全体の設定と、オプションのユーザーまたはグループの上書きによって制御されます。 組織全体の設定では、組織内のユーザーに対する同僚のアクセス権を有効または無効にします。 デフォルトでは、すべてのユーザーに対してアクセスが有効になっています。

| 設定 | アクセスへの影響 |
| --- | --- |
| 組織全体の設定 | すべてのユーザーに対して同僚アクセスを有効にするか、組織に対して無効にします。 |
| ユーザーまたはユーザーグループの上書き | 上書きにより、管理者は特定のユーザーまたはユーザーグループに対する同僚のアクセス権を制御できます。 |
| 互換性のあるアプリケーション権限 | Coworkerのアクセス制御は、一般に利用可能なCoworker機能にアクセスできるかどうかを決定します。 Coworkerは、Coworker互換のCX Enterprise アプリケーションからユーザー権限を継承し、各アプリケーションが既に適用している権限を尊重します。 |


## 共同作業者の管理者 {#add-coworker-admins}

共同作業者の管理者は、組織の&#x200B;**[!UICONTROL システム管理者]**&#x200B;または[!DNL Adobe Admin Console]の&#x200B;**[!UICONTROL 製品管理者]**/[!DNL Adobe Experience Platform]として割り当てられたユーザーです。

## ユーザーアクセスの管理 {#manage-user-access}

1. 「同僚」エクスペリエンスを開きます。 手順については、「[同僚にログイン &#x200B;](/help/chat/ui-guide.md#sign-in)」を参照してください。
2. プロファイルメニューを開き、**[!UICONTROL 管理者設定]**&#x200B;を選択します。

   プロファイルメニューコントロールがハイライト表示された![同僚ホーム。](./assets/access-control/coworker-home.png)

   管理者設定がハイライト表示された![同僚プロファイルメニュー。](./assets/access-control/admin-settings.png)

3. 「**[!UICONTROL アクセス制御]**」を選択します。

   アクセス制御カードがハイライト表示された![管理者設定。](./assets/access-control/access-control.png)

   このビデオでは、同僚ユーザーの管理方法について説明します。

   >[!VIDEO](https://video.tv.adobe.com/v/3507152?captions=jpn&learn=on){transcript=true}

4. Coworkerでは、**[!UICONTROL ユーザー]**&#x200B;を使用して個人のアクセスを管理するか、**[!UICONTROL ユーザーグループ]**&#x200B;を使用してユーザーグループのCoworker アクセスを管理します。 ユーザーグループ設定は、そのメンバーに適用されます。

   共同作業者ユーザーグループは[!DNL Adobe Admin Console] グループとは別です。 [!DNL Adobe Admin Console]から同僚へのユーザーグループの同期は近日リリース予定です。

   ユーザーリストには、組織内のユーザーが含まれます。 これらのユーザーに対しては、デフォルトで同僚アクセスが有効になっています。

   * **有効：** ユーザーまたはユーザーグループがアクティブです。
   * **無効：** ユーザーまたはユーザーグループが非アクティブです。

   全員のアクセスが無効になっている場合は、**[!UICONTROL 上書きの許可]**&#x200B;をオンにし、**[!UICONTROL 上書きの追加]**&#x200B;を選択して、引き続きアクセス権を持つ必要があるユーザーまたはグループを追加します。

## 同僚と互換性のあるCX Enterprise アプリケーションの権限 {#permissions-in-compatible-applications}

同僚と互換性のあるCX Enterprise アプリケーションは、引き続き独自の権限を適用します。

同僚は、互換性のあるアプリケーションの権限を尊重します。 例えば、[!DNL Adobe Experience Platform]のデータセットにアクセスできない場合、Coworkerはそのデータセットを取得または処理できません。

## アクセスに関するヘルプ {#get-help-with-access}

[!UICONTROL &#x200B; アクセス制御]が表示されない場合は、Adobe管理者またはAdobe担当者にお問い合わせください。 ユーザーは、この機能が組織に対して有効になっているかどうか、およびその設定にアクセスできるかどうかを確認できます。

アクセスが拒否された場合は、組織全体のデフォルトとユーザーまたはグループの設定を確認するように管理者に依頼します。 共同作業者と互換性のあるCX Enterprise アプリケーションの場合は、そのアプリケーションに対して個別に管理されている権限を確認するように依頼します。

## このトピックの詳細ヘルプ {#more-help}

共同作業と管理の詳細については、これらのリソースを使用してください。

* [同僚チャットの概要](/help/chat/overview.md)
* [同僚とのチャットを始める](/help/chat/ui-guide.md)
* [プラグインとマーケットプレイスを管理](/help/customizations/plugins/manage-plugins-for-your-org.md)
