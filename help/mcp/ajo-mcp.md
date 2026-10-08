---
title: CX Coworker GatewayのJourney Optimizer Tools
description: CX Coworker Gatewayを通じて使用できるAdobe Journey Optimizer ツールについて説明します。
hide: true
source-git-commit: 6c126810936bea3e883d74e6ff685991cb40cd4a
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 6%
---
# CX Coworker GatewayのAdobe Journey Optimizer ツール {#ajo-mcp}

Adobe Journey Optimizerの製品ツールを使用して、MCP対応クライアントからキャンペーン、ジャーニー、チャネル設定を調査します。 これらのツールは、組織が有効になっていて、ユーザーアカウントに必要なJourney Optimizer権限が付与されている場合、[CX Coworker Gateway](overview.md)から利用できます。

詳しくは、Adobe Journey Optimizer ドキュメントの[MCP クライアントの操作](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/combine/ajo-mcp){target="_blank"}を参照してください。

ジャーニーを作成、分析、シミュレートするための会話型のエージェント型エクスペリエンスについては、代わりに[Journey Agent](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/agents/ajo-agent)を参照してください。

>[!AVAILABILITY]
>
>Journey OptimizerのツールはBetaに搭載されています。 アクセスは招待状によってのみ行われ、Adobe組織の有効化が必要です。 [CX Coworker Gateway tools](access.md)へのアクセスを参照してください。

## 主な機能 {#mcp-capabilities}

Journey Optimizerのツールは、キャンペーン、ジャーニー、チャネル設定のレビューに対して読み取り専用のサーフェスを提供します。 以下を行うことができます。

- Journey Optimizerのキャンペーンをリストアップし、ステータスでフィルタリングできます。
- ターゲティング、スケジュール、チャネル、コンテンツ設定のメタデータなど、キャンペーンの詳細を取得できます。
- 分岐、条件、アクションなど、サンドボックス内のジャーニーを一覧表示して調査します。
- 電子メール、SMS、プッシュ通知、WhatsApp チャネルのチャネル設定をリストアップします。
- データガバナンスポリシーの適用に使用できるマーケティングアクションのリスト。
- 製品スクリーンを操作することなく、キャンペーン、ジャーニー、チャネルの設定を自然言語で確認できます。

>[!IMPORTANT]
>
>現在のBetaのすべてのJourney Optimizer ツールは読み取り専用です。 キャンペーンまたはジャーニーの作成、更新、削除、開始、停止、公開はサポートされていません。

## 利用可能なツール {#mcp-tools}

| ツール | 説明 |
| --- | --- |
| `ajo_campaign_list` | Adobe Journey Optimizerのマーケティング施策。 `DRAFT`、`LIVE`、`STOPPED`、`COMPLETED`などのステータスによるフィルタリングをサポートしています。 |
| `ajo_campaign_get` | オーディエンスのターゲティング、スケジュール、チャネル、コンテンツ設定のメタデータなど、IDごとに特定のキャンペーンの詳細と設定を取得します。 |
| `ajo_journey_list` | Journey Optimizerサンドボックス内のすべてのジャーニーを参照します。 |
| `ajo_journey_get` | 分岐、条件、アクションなど、ID 別の特定のジャーニーの詳細を取得します。 |
| ジャーニーの可視化 | ジャーニーの構造とフローをレンダリングし、インタラクティブで視覚的な探索を行うことができます。 |
| `ajo_channel_configuration_list`, `ajo_channel_configuration_get` | 電子メール、SMS、プッシュ、または[!DNL WhatsApp] チャネルのサーフェスプリセットとブランド設定を表示します。 |
| `ajo_channel_configuration_resource_list`, `ajo_channel_configuration_resource_get` | プッシュ資格情報、メールサブドメイン、IP プール、SMS資格情報、および[!DNL WhatsApp]資格情報など、チャネル設定によって参照されるサポートされる設定リソースを一覧表示および取得します。 |
| `ajo_marketing_action_list` | データガバナンスポリシーの適用に役立つ、使用可能なマーケティングアクションを一覧表示します。 |

## サンプルプロンプト {#mcp-use-cases}

| 目標 | プロンプトの例 |
| --- | --- |
| キャンペーンの概要 | 「Journey Optimizerのキャンペーンをすべて見せてください」 |
| ステータス監査 | 「現在公開されているキャンペーンはどれですか？」 |
| キャンペーンの詳細 | 「キャンペーン `[campaign ID]`の詳細を確認してください。」 |
| ジャーニーの概要 | 「Journey Optimizerのすべてのジャーニーを表示する」 |
| ジャーニーの詳細 | 「分岐と条件を含む、ジャーニー`[journey ID]`の完全な詳細を取得します。」 |
| オーディエンスとターゲティング | 「キャンペーン `[campaign ID]`のどのオーディエンスがターゲットですか？」 |
| 日程・タイミング | 「キャンペーン `[campaign ID]`の実行スケジュールはいつですか？」 |
| トラブルシューティング | 「キャンペーン `[campaign ID]`の設定を確認し、考えられる問題をフラグします。」 |
| チャネル設定 | 「どのようなメールチャネル設定が可能ですか？」 |
| チャネル監査 | 「欠落または不完全なチャネル設定はどれですか？」 |
| ガバナンス | 「サンドボックスにはどのようなマーケティングアクションがありますか？」 |

## コンテンツ管理ツール {#mcp-content-management}

Journey Optimizerでは、上記の読み取り専用のツールに加えて、コンテンツテンプレート、フラグメント、ランディングページ、ジャーニーまたはキャンペーンのインラインメッセージコンテンツなど、コンテンツアセットを、自然言語プロンプトを使用してCX Coworkerから直接検索および管理できます。 この機能は、Journey Optimizer コンテンツの読み取りと書き込みが可能な個別のMCP ツールのセットを搭載しており、CX Coworkerにアクセスできるすべてのお客様が利用できます。

詳しくは、Adobe Journey Optimizer ドキュメントの[&#x200B; コンテンツ管理ツール &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/essentials/ajo-coworker-skills#content-management){target="_blank"}を参照してください。

コンテンツ管理ツールを活用すると、次のことが可能になります。

- コンテンツテンプレート、フラグメント、ランディングページを参照し、それらの構造、メタデータ、ステータスを取得します。
- ジャーニーまたはキャンペーンアクションノードで設定されたインラインメッセージコンテンツを取得します。
- あらゆるチャネルに対応したコンテンツテンプレートの作成と更新。
- フラグメントを作成、更新、複製、公開できます。
- ジャーニーまたはキャンペーンアクションノードのインラインメッセージでチャネルのバリエーションを置き換えます。

>[!IMPORTANT]
>
>上記の読み取り専用の製品ツールとは異なり、コンテンツ管理ツールは書き込み操作をサポートします。 テンプレートやフラグメント、テンプレートやフラグメントの検証、ランディングページの作成や公開、コンテンツテンプレート、フラグメント、ランディングページの削除などのフルテキスト検索はサポートされていません。

## 製品のコンテキストと権限 {#mcp-context}

照会するJourney Optimizer キャンペーン、ジャーニー、チャネル設定を表示するには、ユーザーアカウントに権限が必要です。 MCPは製品の権限をバイパスしません。

組織で複数のサンドボックスを使用している場合は、特定のサンドボックスの結果が必要な場合に、プロンプトでサンドボックスまたは環境コンテキストを指定します。

## 既知の制限事項 {#mcp-limitations}

| 制限事項 | 説明 | 回避策 |
| --- | --- | --- |
| 読み取り専用サーフェス | Journey Optimizer ツールは、取得操作のみを公開します。 キャンペーンやジャーニーを作成、更新、削除、開始、停止、公開することはできません。 | Journey OptimizerのUIまたはAPIを使用した書き込み操作。 |
| エンゲージメントやパフォーマンスに関する指標はない | ツールは、インプレッション、クリックスルー率、コンバージョン、配信統計などのレポートデータを返しません。 | Journey Optimizerのレポート、Customer Journey Analyticsのツール、Adobe Analyticsのツールをパフォーマンス指標に使用できます。 |
| キャンペーンリストのページネーションは制限されています | キャンペーンリストは、結果の最初のページを返します。最大50件のキャンペーンがアルファベット順に並べ替えられます。 オフセット値と制限値は適用されません。 | キャンペーン IDがわかっている場合は、`Get Campaign`を直接使用します。 Journey Optimizer UIを使用したフルブラウジングとフィルタリング。 |
| 日付、チャネル、スケジュール別にサーバーサイドのフィルタリングなし | キャンペーンリストは、ステータスのフィルタリングをサポートしていますが、公開日、スケジュール日、チャネル、キャンペーンタイプのフィルタリングはサポートしていません。 | Journey Optimizer UIのキャンペーンリストを使用して、ネイティブの日付とチャネルフィルタリングを実行できます。 |
| 商品ツールでメッセージコンテンツを取得できない | Message HTML、件名、パーソナライゼーショントークン、オファーコンテンツは、上記の読み取り専用ツールでは利用できません。 | [&#x200B; コンテンツ管理ツール &#x200B;](#mcp-content-management)を使用して、インラインメッセージコンテンツを取得および更新するか、Journey Optimizer UIで直接表示します。 |