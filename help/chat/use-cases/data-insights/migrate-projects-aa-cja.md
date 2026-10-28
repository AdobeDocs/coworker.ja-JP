---
title: Adobe Analytics プロジェクトのCustomer Journey Analyticsへの移行
description: Coworkerを使用して、Adobe Analytics Workspace プロジェクトとそのコンポーネントを検証、マッピング、Customer Journey Analyticsに移行してから、移行ステータスを確認します。
feature: AI Tools
role: Admin
level: Intermediate
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 1ec3a8bf6dff44df068529cf1f7ceb699a027d65
workflow-type: tm+mt
source-wordcount: '1785'
ht-degree: 1%
---

# Coworkerを使用したAdobe Analytics プロジェクトのCustomer Journey Analyticsへの移行

<!-- FLAG: Confidence: High for the conversation flow, which is sourced from screenshots of the Coworker UI (October 2026) and the aa-mcp tool descriptions. The component migration tools run through the aa-mcp integration; there's no dedicated skill yet. Medium for statements that Coworker shares mappings and migration rules with migrations in the Adobe Analytics user interface; the user believes this is likely. Confirm with engineering. -->

Adobe CX Enterprise Coworkerを使用すると、Adobe Analytics プロジェクトとその関連コンポーネントを1回の会話でCustomer Journey Analyticsに移行できます。

Coworkerは、プロジェクト内のディメンションと指標がCustomer Journey Analytics データビューにマッピングされていることを検証し、マッピングされていないものをマッピングしてから、Customer Journey Analyticsでプロジェクトを再作成します。

<!-- FLAG: Add the planned general availability date when it's confirmed. -->

>[!AVAILABILITY]
>
>この記事で説明する機能は、リリースの限定的なテスト段階にあり、お使いの環境ではまだ利用できない場合があります。 このメモは、機能が一般公開された時点で削除されます。

>[!IMPORTANT]
>
>プロジェクトを移行する前に、Adobe Analytics ドキュメントの「[Adobe AnalyticsからCustomer Journey Analyticsへのコンポーネントとプロジェクトの移行の準備](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration)」を参照してください。 移行に備える方法、含まれる要素、エラーの原因、マッピングが組織全体にどのような影響を与えるかを説明します。 この情報は、Coworkerでの移行に適用されます。

## Adobe Analytics ユーザーインターフェイスでの移行との違い

<!-- FLAG: Add rows as differences are confirmed. Who can migrate and How you migrate: SME Scott Tomko (October 2026); Coworker matches the Analytics 2.0 Component Migration APIs, and functionally both methods do much the same thing. Project owner: Coworker behavior is from a test conversation (October 2026); the Adobe Analytics user interface behavior is from component-migration.md in the Adobe Analytics docs. Mapping dimensions and metrics: Confidence Medium for the Coworker column, which is based on the aa-mcp tool descriptions and a test conversation, not on an observed failed validation. Confirm that Coworker suggests and updates mappings, and whether it asks for confirmation before it updates a mapping. The Adobe Analytics user interface behavior is from component-migration.md in the Adobe Analytics docs. -->

Coworkerを使用したプロジェクトの移行は、Adobe Analytics ユーザーインターフェイスでのプロジェクトの移行とは次の点で異なります。

| | Coworker | Adobe Analyticsのユーザーインターフェイス |
| --- | --- | --- |
| **プロジェクトを移行できるユーザー** | Adobe Analytics管理者、および&#x200B;[!UICONTROL **コンポーネント移行**]&#x200B;権限を持つユーザー | Adobe Analytics管理者のみ |
| **プロジェクト所有者** | 移行を実行しているユーザー | [!UICONTROL **プロジェクト所有者**] フィールドで指定するユーザー |
| **ディメンションと指標のマッピング** | チームメンバーは、プロジェクトを検証し、各ディメンションと指標がどのようにマッピングされているかを確認します。 自動的にマッピングできないものについては、Coworkerがデータビューでディメンションまたは指標を提案し、マッピングを更新します。 | 「[!UICONTROL **マップスキーマ**]」セクションでは、[!UICONTROL **マッピングされていない**] ステータスを持つ各ディメンションまたは指標を選択し、手動でマッピングします。 |
| **移行方法** | プロンプトに何が必要かを記述します。 チームメンバーは、いくつかの質問をしながら作業を進めます。 たとえば、名前を付けたコンポーネントを使用してプロジェクトを作成し、それを移行することができます。 [特定のコンポーネントから開始](#start-from-specific-components)を参照してください。 | Analysis Workspaceでプロジェクトを作成し、移行するコンポーネントを追加して、プロジェクトを保存します。 次に、[!UICONTROL **コンポーネント移行**]&#x200B;で、プロジェクトを選択し、プロジェクト所有者を指定し、各レポートスイートのスキーマをマッピングして、[!UICONTROL **移行**]&#x200B;を選択します。 |

## 前提条件

<!-- FLAG: Confidence: High for the Adobe Analytics MCP and permission bullets, which come from the release announcement and SME Scott Tomko (October 2026): like the Analytics 2.0 Component Migration APIs, Coworker lets non-admins with the Component Migration permission migrate projects, while the Adobe Analytics UI is admin-only. Open question: Coworker makes the user who runs the migration the owner of the new project, but the aa-mcp tool description says the owner "should be an admin" and the Adobe Analytics component migration docs say the owner must be a Customer Journey Analytics administrator. Confirm whether a non-admin who runs a migration needs Customer Journey Analytics admin rights, or whether Coworker assigns a different owner. -->

Coworkerでプロジェクトを移行するには、次のものが必要です。

* Adobe Analytics MCPへのアクセス。 コンポーネント移行ツールは、Adobe Analytics MCP アクセス権を持つお客様に対して自動的に有効になります。 [!UICONTROL **aa-mcp**]&#x200B;が接続されていることを確認するには、[同僚チャット &#x200B;](/help/chat/use-cases/data-insights/analytics-chat.md)によるデータ分析を開始するを参照してください。

* Adobe Analytics管理者権限、またはAdmin Consoleの&#x200B;[!UICONTROL **Component Migration**]&#x200B;権限。 管理者である必要はありません。

* コンポーネントの移行に関する[前提条件](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#prerequisites)については、Adobe Analytics ドキュメントを参照してください。

* 基本レポートスイートを使用するプロジェクト。 仮想レポートスイートを移行できません。<!-- FLAG: Sourced from Coworker's response in the UI. The Adobe Analytics component migration docs don't mention virtual report suites. Confirm, and consider adding it to those docs. -->

## 移行前にレポートスイートのマッピングを確認する

<!-- FLAG: Confidence: Medium. The recommendation to review mappings before the first migration from a report suite is inferred from the Adobe Analytics guidance to decide mappings as an organization; Coworker also validates mappings during each migration. Confirm with Scott. -->

レポートスイートから最初に移行する前に、レポートスイートのディメンションと指標のマッピング方法を確認することを検討してください。 マッピングは、組織が移行するすべてのプロジェクトに適用されます。そのため、最初にマッピングを設定すると、後のプロジェクトが検証を通過するのに役立ちます。 マッピングの選択に関するガイダンスについては、Adobe Analytics ドキュメントの「[組織としてコンポーネントをどのようにマッピングするかを決定する](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#decide-as-an-organization-how-you-will-map-components)」を参照してください。

マッピングをレビューするには、[!UICONTROL **スコープ**] タブで「[!UICONTROL **マッピングのみをレビュー**]」を選択するか、同僚に直接依頼します。

**プロンプト**

* 「レポートスイートのディメンションと指標が自分のデータビューにどのようにマッピングされるかを表示する」
* 「データビューにマッピングされていないレポートスイートのディメンションと指標はどれですか？」

また、マッピングを更新するように同僚に依頼することもできます。

このレビューをスキップすると、移行する各プロジェクトのマッピングは[引き続き](#review-the-validation-results-and-mappings)確認されます。

## 移行を開始

<!-- FLAG: Confidence: High that migration works at the project level and that components migrate with their project (component-migration.md in the Adobe Analytics docs), and that components that already exist in Customer Journey Analytics aren't re-created (prepare-component-migration.md). Medium-low for when to use each method and for combining them; this guidance is inferred and isn't in the Adobe Analytics docs. Confirm with Scott. Also confirm whether Coworker creates a project automatically when you ask it to migrate only components (for example, "Migrate my Spring sale segments to CJA"), or whether you must ask it to create the project. -->

Workfrontでは、プロジェクトとその関連コンポーネントが常に移行されます。 特定のコンポーネントを移行するには、新しいプロジェクトに追加してから、そのプロジェクトを移行するように同僚に依頼します。

Customer Journey Analyticsにすでに存在するコンポーネントは再作成されないので、両方の方法を使用できます。 例えば、最初に最も重要なプロジェクトを移行し、残りのコンポーネントをすべて移行します。 Customer Journey Analyticsの内容に基づいて開始する場所を選択します。

* Customer Journey Analyticsでプロジェクトのパネルとビジュアライゼーションを保持する場合は、**プロジェクトを移行**&#x200B;します。 [&#x200B; プロジェクトから開始](#start-from-a-project)を参照してください。
* **Customer Journey Analyticsでセグメント、計算指標、日付範囲などのコンポーネントを必要としているが、それらを使用するプロジェクトを必要としない場合は、特定のコンポーネント**&#x200B;を移行します。 たとえば、Customer Journey Analyticsで、新しいプロジェクトを構築する場合に、そのプロジェクトを含めることを計画します。 [特定のコンポーネントから開始](#start-from-specific-components)を参照してください。

### プロジェクトから開始

プロジェクトとその関連コンポーネントを移行するには：

1. Coworkerにログインします。

1. **[!UICONTROL 新しいチャット]**&#x200B;を選択します。

1. テキストフィールドに、プロジェクトを移行するようCoworkerにプロンプトを表示します。 次に例を示します。

   **プロンプト**

   > Adobe AnalyticsからCustomer Journey Analyticsにコンポーネントを移行する。

   同僚が移行できる内容を説明し、アンケートを開始します。

1. 「[!UICONTROL **スコープ**]」タブで、次のいずれかのオプションを選択し、[!UICONTROL **次**]&#x200B;を選択します。

   <!-- FLAG: Confidence: Medium for the "Plan a full upgrade" description. It likely hands off to the implementation guide skill and leaves the migration flow. Confirm with engineering. Also confirm what the Source & target tab asks; it was skipped in the screenshots. The Next and Submit buttons on the first questionnaire's Source & target and Review tabs are assumed to work like the second questionnaire. -->

   | オプション | 説明 |
   | --- | --- |
   | [!UICONTROL **特定のAA プロジェクト**] | 名前を付けたプロジェクトを移行します。 このセクションの残りの手順に従います。 |
   | [!UICONTROL **マッピングのレビューのみ**] | レポートスイートの指標とディメンションが、何も移行することなく、データビューにどのようにマッピングされるかを確認します。 移行する前に、[&#x200B; レポートスイートのマッピングを確認する](#review-report-suite-mappings-before-you-migrate)を参照してください。 |
   | [!UICONTROL **完全なアップグレードの計画**] | Adobe Adobe AnalyticsからCustomer Journey Analyticsへの移行プランをエンドツーエンドでご確認ください。 [同僚との実装計画](/help/chat/use-cases/data-insights/implementation-guide.md)を参照してください。 |

1. （オプション）「[!UICONTROL **Sourceとターゲット**]」タブの質問に答え、「[!UICONTROL **次へ**]」を選択します。

1. 「[!UICONTROL **レビュー**]」タブで、回答を確認し、[!UICONTROL **送信**]&#x200B;を選択します。

   Coworkerは、アクセスできるAdobe Analytics企業と、各レポートスイートの基本レポートスイートの数を確認し、2回目のアンケートを開始します。

1. 次の質問に答え、各質問の後に&#x200B;[!UICONTROL **次**]&#x200B;を選択します。

   | タブ | 質問 | その他のコンテキスト |
   | --- | --- | --- |
   | [!UICONTROL **プロジェクト**] | 移行するAA プロジェクトの名前を教えてください。 | 部分的な名前でも構いません。 |
   | [!UICONTROL **レポートスイート**] | プロジェクトで使用するレポートスイート | リストからレポートスイートを選択するか、別のレポートスイートの名前を入力します。 |
   | [!UICONTROL **データビュー**] | 移行するCJA データビューはどれですか？ | （オプション）データビューの名前を入力するか、空白のままにして、Coworkerが一致するデータビューを提案します。 |

1. 「[!UICONTROL **レビュー**]」タブで、回答を確認し、[!UICONTROL **送信**]&#x200B;を選択します。

   任意の手順でアンケートをスキップするには、[!UICONTROL **アンケートをスキップ**]&#x200B;を選択し、代わりにチャットで何を求めるかを説明します。

1. [検証結果とマッピングを確認](#review-the-validation-results-and-mappings)して続行します。

### 特定のコンポーネントから開始

<!-- FLAG: Sourced from a prompt that SME Scott Tomko ran in Coworker (October 2026). The example is generalized; the original prompt named a customer. Coworker may ask a few questions along the way. Confirm what happens to the project that Coworker creates in Adobe Analytics, and to its migrated copy in Customer Journey Analytics, if you only wanted the components. -->

特定のコンポーネントを移行するには：

1. Coworkerに、これらのコンポーネントを含むプロジェクトを作成して移行するように依頼します。 次に例を示します。

   **プロンプト**

   > すべてのAnalytics セグメントを、名前に「Spring Sale」を付けてCJAに移行します。 これらのセグメントがすべて追加された新しいWorkspace プロジェクトを作成してから、そのプロジェクトをCJAに移行します。

   共同作業者がAdobe Analyticsでプロジェクトを作成します。

1. 次のセクションに進みます。[検証結果とマッピングを確認](#review-the-validation-results-and-mappings)。

## 検証結果とマッピングの確認

<!-- FLAG: Confidence: Medium for the steps that fix a failed validation. They're based on the aa-mcp tool descriptions and on a test conversation where validation passed only after the project's panel was switched to a base report suite. Confirm how Coworker presents a failed validation, and whether it asks for confirmation before it updates a mapping. -->

Coworkerは、選択したデータビューに対してプロジェクトを検証し、プロジェクトを移行できるかどうかをレポートします。 結果には、プロジェクト内の各ディメンションと指標、およびマッピング先のCustomer Journey Analytics ディメンションまたは指標が一覧表示されます。 次に例を示します。

* **指標：**&#x200B;件がイベントになります
* **Dimension:**&#x200B;時間の滞在時間

移行されるコンポーネントとプロジェクト要素については、[移行に含まれるものを理解する](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#understand-what-is-included-in-a-migration)Adobe Analytics ドキュメントを参照してください。

検証が合格しない場合：

* **自動的にマッピングできないディメンションまたは指標：**&#x200B;同僚は、データビューでディメンションまたは指標を提案してマッピングし、マッピングを更新した後、プロジェクトを再度検証します。 また、「ページビューをweb.webPageDetails.pageViews.valueにマッピング」など、マッピングするディメンションや指標をCoworkerに指定することもできます。

* **サポートされていない要素：** Adobe Analyticsのプロジェクトからサポートされていない要素を削除します。 例えば、すべてのパネルで、仮想レポートスイートではなく基本レポートスイートを使用するようにします。 次に、同僚にプロジェクトをもう一度確認するように依頼します。 サポートされていない要素の一覧については、Adobe Analytics ドキュメントの[&#x200B; エラーの原因となるサポートされていない要素について](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#understand-unsupported-elements-that-cause-errors)を参照してください。

移行する前にレポートスイート全体のマッピングを確認するには、[移行する前にレポートスイートのマッピングを確認する](#review-report-suite-mappings-before-you-migrate)を参照してください。

## プロジェクトの移行

1. 検証に合格すると、選択したデータビューでプロジェクトのCustomer Journey Analytics バージョンを作成するかどうかを尋ねられます。 [!UICONTROL **はい、**]&#x200B;を移行してから、[!UICONTROL **送信**]&#x200B;を選択します。

   移行せずに停止するには、[!UICONTROL **いいえ、ここで停止**]&#x200B;を選択します。

   共同作業者は、プロジェクトオーナーと共に、Customer Journey Analyticsでプロジェクトを再作成します。 Adobe Analyticsのプロジェクトは変わりません。

1. 次のセクションに進みます。[移行ステータスを確認する](#check-the-migration-status)。

## 移行ステータスの確認

移行はバックグラウンドで実行されるため、新しいプロジェクトの準備がすぐに整わない可能性があります。

1. 移行のステータスを確認するように同僚に促します。

   **プロンプト**

   > ステータスの確認

   <!-- FLAG: The Failed row links to Retry a failed migration in the Adobe Analytics docs, but those steps use the Component migration page in the Adobe Analytics UI, which is admin-only. A non-admin with the Component Migration permission can't follow them. Confirm with Scott whether Coworker can retry a failed migration (for example, "Retry the migration"). If so, replace the link with a prompt. -->

   共同作業者は、次のいずれかのステータスをレポートします。

   | ステータス | 意味 |
   | --- | --- |
   | キューに追加中 | 移行は開始を待っています。 |
   | 開始済み | 移行は進行中です。 |
   | 完了 | 移行が完了しました。 Coworkerは、プロジェクト名とデータビューを含む、移行された内容の概要を提供します。 |
   | 失敗 | 移行に失敗しました。 移行を再試行できます。 Adobe Analytics ドキュメントの「[失敗した移行を再試行する](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/component-migration#retry-a-failed-migration)」を参照してください。 |

1. 移行が完了したら、Customer Journey Analytics Workspaceのプロジェクトリストから新しいプロジェクトを開きます。

1. （オプション）Customer Journey Analyticsの任意のユーザーにプロジェクトの所有権を転送します。 詳しくは、[&#x200B; アセットの転送](https://experienceleague.adobe.com/en/docs/analytics-platform/using/tools/asset-transfer/transfer-assets)を参照してください。

移行が完了したら、次に移行する別のプロジェクトを同僚から提案できます。

## より良い結果を得るためのヒント

* どのデータビューを使用すればよいかわからない場合は、アンケートでデータビューを空白のままにします。 同僚が、レポートスイートに一致するデータビューを提案します。
* 移行後、Adobe Analytics データとCustomer Journey Analytics データを比較して、レポートが一致することを確認します。 Adobe AnalyticsからCustomer Journey Analyticsにアップグレードする場合は、[Coworkerでデータを検証するを参照してください](/help/chat/use-cases/data-insights/data-validation-aa-cja.md)。

## 次の手順

* 代わりにAdobe Analytics ユーザーインターフェイスでプロジェクトを移行するには、Adobe Analytics ドキュメントの「[Adobe AnalyticsからCustomer Journey Analyticsへのコンポーネントとプロジェクトの移行](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/component-migration)」を参照してください。
* その他の実装と管理の使用例については、[&#x200B; インテリジェント実装と管理の概要](/help/chat/use-cases/data-insights/data-governance-and-validation.md)を参照してください。
