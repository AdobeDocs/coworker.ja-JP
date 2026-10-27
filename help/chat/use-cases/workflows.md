---
description: データインサイト、オーディエンス、ジャーニー、プラットフォーム運用をまたいで、エリア別に整理された同僚チャットのワークフローとサンプルプロンプトを参照できます。
title: 共同作業者チャットワークフロー
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: aa38c5009d3c61996406a73447f901d109314458
workflow-type: tm+mt
source-wordcount: '8465'
ht-degree: 8%
---
# 共同作業者チャットワークフロー {#use-cases}

共同作業チャットを使用すると、複数のUIを移動したり、手動でクエリを記述したりするのではなく、自然言語を使用して[!DNL Experience Platform] データをクエリ、分析、アクションできます。 このページでは、実務担当者が最も利用しているワークフローを、データインサイト、オーディエンス、ジャーニー、ロイヤルティ、基本要素、サンドボックスツールなどの作業領域ごとに分類して示します。 各エントリには、呼び出すスキル、使用するアプリケーション、コピーできるプロンプトのサンプル、独自のデータへの適応、会話による絞り込みなどがあります。

## スキルやワークフローについて

**スキル：** _スキル_&#x200B;は、共同作業者が実行できる単一の特定の機能またはアクションです。 たとえば、オーディエンスの作成、メールの送信、レポートの生成、キャンペーンの結果の分析などがあります。 各スキルは、特定の機能に焦点を当てています。

**ワークフロー：** _ワークフロー_&#x200B;は、より広範なビジネス目標を達成するために設計された一連の手順またはアクション（多くの場合、複数のスキルを含む）です。 ワークフローは、マーケティングキャンペーンの立ち上げ、新しい顧客セグメントのオンボーディング、キャンペーンパフォーマンスの低下の診断など、複雑なマルチステップのプロセスを完了するために、複数のスキルを論理的な順序で調整します。

## ブランド体験

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [AEM ページの更新](brand-visibility/author-web-pages.md) | コンテンツ要素の更新、削除、置き換え、追加などのアクションを実行し、エクスペリエンスを正確かつ最新の状態に保ちます。 入力には、自然言語またはPDFやスクリーンショットなどの視覚的な注釈を使用できます。 | `aem-sites-pages-update` | Adobe Experience Manager（AEM） - AEM Sites | &lt;URL>の見出しを「Hello World<br><br>」に更新し、&lt;URL>の「コーヒークイズを取る」ボタンをより魅力的なバージョンに変更します<br><br>添付された<br><br>に基づいて&lt;URL>を更新します。8月に実施しているコーヒーマシンを購入し、コーヒーフリーの2袋を入手するプロモーションについて、ページの下部に新しいティーザーセクションを追加したいと思います。 また、コーヒーを飲む友人の画像を見つけて、ティーザーでそれを使用することもできます |
| AEMの一括更新 | コンテンツ要素の削除、置き換え、追加など、複数のページをまたいで同時に一括アクションを実行し、エクスペリエンスを正確かつ最新の状態に保ちます。 | `aem-sites-pages-bulkreplace` | Adobe Experience Manager（AEM） - AEM Sites | &lt;aem path>で、コピー「MyBarista\」を含むすべてのページを「BrewPass」に更新します |
| Figmaからビジュアルコンテンツフラグメントへ | 自然言語を使用して、FigmaからAdobe Experience Managerにデザインを直接読み込みます。 このスキルにより、必要なコンテンツモデル、コンテンツフラグメント、アセット、ビジュアライゼーションテンプレートが自動的に作成されるため、ビジネスユーザーは手作業で設定しなくても、デザインからwebに対応したコンテンツを数分で作成することができます。 | `aem-sites-visualcontentfragments-create` | Adobe Experience Manager（AEM） - AEM Sites | &lt;Figma_URL>からインポート |

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| フォームを作成 | 新しいアダプティブフォームを、平易な説明、添付された概要、画像、またはPDFから生成します | `aem-forms-adaptiveform-create` | Adobe Experience Manager（AEM） - AEM Forms | 「従業員オンボーディングフォームの作成」 <br><br> 「添付された概要（画像またはpdf）を使用してフォームを作成」 <br><br> 「Create a &lt;form type> adaptive form」 |
| フォームの編集/更新 | 既存のフォームの変更 – フィールドの追加/編集、シンプルなレイアウトの調整、送信アクションの設定、添付されたガイドラインドキュメントからの変更の適用を行います | `aem-forms-adaptiveform-edit` | Adobe Experience Manager（AEM） - AEM Forms | 「姓フィールドの下にミドルネーム フィールドを追加」 <br><br> 「名フィールドと姓フィールドを2列のレイアウトに入れる」, 50/50&quot;<br><br> 「REST エンドポイントにデータを送信するフォームを設定」 <br><br> 「添付されたガイドライン ドキュメントに一致するようにこのフォームを更新」 <br><br> 「次に&lt; フィールド > フィールドを追加」 |
| ビジネスロジックの追加 | 他のフィールドの値に基づいてフィールドを表示または非表示にするなど、簡単なルールを作成できます | `aem-forms-adaptiveform-edit` | Adobe Experience Manager（AEM） - AEM Forms | 「従業員タイプが請負業者の場合にのみ会社フィールドを表示」 <br><br> 「他のフィールドが&lt;value>の場合にのみ&lt;field> フィールドを表示」 |
| 埋め込みフォーム | 既存または新しく作成したフォームを、指定したAEM Sites ページに配置します（Edge Delivery Services ページでのみサポート） | `aem-forms-adaptiveform-embed` | Adobe Experience Manager（AEM） - AEM Forms | 「このフォームをサイトのホームページに埋め込む」 <br><br> 「このフォームを&lt; ページパス >に埋め込む」 |

**関連情報**

* [AEMのAgentic Capabilities: Brand Experience - Experience Production - Sites](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/experience-production/use-cases#use-cases-sites)

* [AEMのエージェント機能：ブランドエクスペリエンス – エクスペリエンス制作 – Forms](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/experience-production/use-cases#use-cases-forms)

### 開発

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| Cloud Manager パイプラインの管理 | ログ、アーティファクト、変数、設定など、AEM Cloud Manager パイプラインを作成、実行、モニタリングします | `cloud-manager-pipeline-management` | Adobe Experience Manager（AEM） | 「プログラム 12345のパイプラインのリスト」 <br><br> 「最新のパイプラインのステータスは？」 |
| Cloud Manager環境の管理 | RDE、環境変数、ログ、バックアップなどのAEM Cloud Manager環境を作成、設定、管理します | `cloud-manager-environment-management` | Adobe Experience Manager（AEM） | &quot;プログラム 12345の環境を一覧表示&quot;<br><br>&quot;RDEをリセット&quot; |
| Cloud Manager プログラムの管理 | パイプラインと環境を含むAEM Cloud Manager プログラムの一覧表示、検査、削除 | `cloud-manager-program-management` | Adobe Experience Manager（AEM） | 「自分のCloud Manager プログラムを一覧表示」 <br><br> 「プログラム 12345の詳細を表示」 |
| AEM リリースアップデートスケジュールの管理 | 自動メンテナンス用に毎日のサイレントアワーとアップデート不要の期間を設定し、Adobeのグローバルコードフリーズウィンドウを表示します | `cloud-manager-release-management` | Adobe Experience Manager（AEM） | 「現在の休眠時間枠は何ですか？」 <br><br> 「12月20日から1月2日までの更新料無料の期間をスケジュールする」 |

**関連情報**

* [AEMのエージェント機能：ブランドエクスペリエンス – 開発](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/development/use-cases)

### オンボーディング

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| ガイド付きのエンドツーエンドのオンボーディング | 必要な特定のオンボーディングタスクがわからない場合は、オンボーディングライフサイクル全体、リポジトリ選択、フォルダーへの委任、タグ、メタデータ、インポート、検索サブスキルを調整します。 | `aem-onboarding-workflow` | Adobe Experience Manager（AEM） - AEM Assets | 「AEM Assetsへのオンボーディング」 <br><br> 「AEM DAM オンボーディングの手順」 |
| フォルダー階層の設計と作成 | ビジネスニーズやCSV入力に基づいて、AEM Assets（`/content/dam`以下）でスケーラブルなフォルダー構造を推奨および作成します。 | `aem-folder-management` | Adobe Experience Manager（AEM） - AEM Assets | 「ライフスタイルマーケティングアセットのフォルダー構造を推奨」 <br><br> 「このCSV ファイルに基づいてフォルダーを作成」 |
| タグのデザインと作成 | `/content/cq:tags`の下に制御されたタグ語彙をデザインして作成します。名前空間、階層タグ、バッチタグ操作です。 | `aem-tag-taxonomy` | Adobe Experience Manager（AEM） - AEM Assets | 「商品カテゴリの名前空間を使用したタグ分類の設計」 <br><br> 「このCSVからタグをインポート」 <br><br> 「AEMでこれらの階層タグを作成」 |
| メタデータフォームの作成と割り当て | カスタムメタデータフォームを設計および作成し、オーサリング UI コンテンツ作成者が使用するカスタムメタデータフォームは、CSV、テーブル、要件ドキュメントまたは説明から任意でフォルダーに割り当てられます。 | `aem-metadata-form` | Adobe Experience Manager（AEM） - AEM Assets | 「このフィールドのリストからメタデータフォームを作成する」 <br><br> 「このフォームを`campaigns` フォルダーに割り当てる」 |

**関連情報**

* [AEMのエージェント機能：ブランドエクスペリエンス – オンボーディング](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/onboarding/use-cases)

## Content Advisor

### コンテンツ発見

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| セマンティックテーマで検索 | AIを活用したセマンティックマッチングにより、コンセプト、ムード、ビジュアルテーマごとにアセットを検索できます。 | `aem-assets-discovery` | Adobe Experience Manager（AEM） - AEM Assets | &quot;Find me morning coffee lifestyle images&quot; |
| カスタムメタデータで検索 | カスタムメタデータフィールド（コーヒーブレンド、ブランド、ローストレベルなど）でアセットをフィルタリングします。 | `aem-assets-discovery` | Adobe Experience Manager（AEM） - AEM Assets | 「`Coffee Blend`が`Morning Muse`のアセットを検索する」 <br><br> 「ライセンスの有効期限が切れていないアセットを取得する」 <br><br> 「キャンペーン名が設定されていないアセットを検索する（適切な結果を得るには、プロパティにインデックスを付ける必要があります）」 |
| 承認ステータスで検索 | 承認ステータスに基づいてアセットをフィルタリングします。 たとえば、「承認済み」、「レビュー中」、「却下」、「ステータスが欠落している」などです。 | `aem-assets-discovery` | Adobe Experience Manager（AEM） - AEM Assets | 「`Campaign` フォルダー内のすべての承認済みアセットを表示する」 |
| フォルダー/パスで検索 | AEMのフォルダー名を参照する自然言語プロンプトを解釈して、アセットを識別できます。 リポジトリ内を手動で移動することなく、プロンプトでフォルダーについて説明するだけで、適切なコンテンツを見つけるために必要なクリック数を大幅に削減できます。 | `aem-assets-discovery` | Adobe Experience Manager（AEM） - AEM Assets | 「フォルダー`WKND`にsvgがありますか？<br><br>」「フォルダー`WKND`の2025年11月1日以降に変更されたアセットを表示」 |

**関連情報**

* [AEMのエージェント機能：Content Advisor - Content Discovery](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/content-advisor/discovery/use-cases)

### コンテンツの最適化

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| 高解像度レンディションの作成とチャネルに最適化されたレンディション | 指定された解像度と品質レベルでアセットの新しいレンディションを生成するので、手作業での編集なしでチャネルに対応したバリエーションを簡単に準備できます。 また、Instagram ストーリーなどのプラットフォーム固有の要件に合わせてレンディションを制作し、アセットが形式、比率、品質のガイドラインを自動的に満たすようにすることもできます。 | `aem-assets-content-optimisation` | Adobe Experience Manager（AEM） - AEM Assets | 「Create a `2000px` rendition as `JPEG` with `80% quality`」 <br><br> 「Create a rendition for an Instagram story」 |
| ブランドオーバーレイと複合生成 | 正確な配置で既存のアセットにプロモーショングラフィック、オーバーレイ、バッジを適用し、キャンペーンに対応したコンポジットの迅速な作成をサポートします。 | `aem-assets-content-optimisation` | Adobe Experience Manager（AEM） - AEM Assets | 「プロモーションバナーの上に`30%`個の割引グラフィックを配置し、中央から`100px`配置した画像をオーバーレイする」 |
| 画像の強化、背景色の調整、方向の変換 | ビジュアルの改善（シャープ画像）の適用、背景色の置き換え、方向変換の実行を行います。 | `aem-assets-content-optimisation` | Adobe Experience Manager（AEM） - AEM Assets | 「`PNG`の背景色を`#ff8932`に変更」 <br><br> 「画像をシャープにする」 <br><br> 「画像を水平方向にミラーリングする」 |

**関連情報**

* [AEMのエージェント機能：Content Advisor - Content Optimization](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/content-advisor/content-optimization/use-cases)

## ブランドガバナンス

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| ガイドラインとセグメントの検索 | セグメント、市場、カテゴリーごとに分類された詳細なブランドガイドラインを取得します | enterprise-context | Adobe Experience Manager（AEM） | 「このブランドのトーンオブボイスのガイドラインは何ですか？」 <br> 「ヘルスの垂直方向で使用される請求項カテゴリのリスト」 |
| ブランドガイドラインに照らし合わせたコンテンツの評価 | 設定されたブランドチェックに照らし合わせて、公開/編集されたページ、テキストブロック、画像を評価します | aem-governance | Adobe Experience Manager（AEM） | 「このランディングページをSecurBank ガイドラインに照らして評価する」 <br> 「このキャッチフレーズはトーンオブボイスのチェックに合格しますか？」 |
| AEM権限のデバッグ | 権限ポリシー、ACL、継承ルールをデバッグまたは理解します。 | aem-governance | Adobe Experience Manager（AEM） | 「プリンシパル管理者が`https://author/`に`/content/folder/us`を書き込むことができる理由？」 <br> 「なぜ`https://author`に`/content/dam`でサンプル オーサーを書き込むことができないのか」 |

**関連情報**

* [AEMのエージェント機能：ブランドガバナンス](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-governance/use-cases)

## 顧客理解とデータ活用

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [CJAおよびAA レポートと指標を取得](data-insights/analytics-chat.md) | CJAやAAにリアルタイムでクエリを実行し、指標、ディメンション、セグメント、データビュー、レポートスイートなどを取得できます | `cja`, `aa` | Customer Journey Analytics（CJA）、Adobe Analytics（AA） | 「過去30日間のページビューを表示」 <br> 「マスターデータビューの上位セグメントを一覧表示」 |
| 比較分析 | チャネル、期間、セグメントをまたいで指標を並べて比較できます | `cja-root-cause-analysis`, `cja`, `aa-root-cause-analysis`, `aa`, `dx-api`, `knowledge-graph` | Customer Journey Analytics（CJA）、Adobe Analytics（AA） | 「チャネル別の収益を月々比較」 <br> 「モバイルとデスクトップのコンバージョンは今四半期でどのように見えますか？」 |
| キャンペーンのパフォーマンス | 一定期間におけるキャンペーン、チャネル、web プロパティのパフォーマンスを測定。 | `cja`, `aa`, `dx-api`, `knowledge-graph` | | 「先月のAcrobat web キャンペーンのパフォーマンスはどうでしたか？」 |
| Funnel analysis | 各段階での離脱を防ぐための、マルチステップのコンバージョンファネルを順を追って説明します | `cja`, `aa` | Customer Journey Analytics（CJA）、Adobe Analytics（AA） | 「チェックアウト funnelの手順を説明」 <br> 「PDPから購入までのコンバージョン funnelの表示」 |
| 予測 | 過去のCJAまたはAA データに基づく将来の指標値のプロジェクト | `cja`, `aa` | Customer Journey Analytics（CJA）、Adobe Analytics（AA） | 「今後30日間のセッションを予測」 <br> 「売上目標を達成する予定ですか？」 |
| [根本原因分析](data-insights/root-cause-analysis.md) | 指標が変化した理由：低下、急上昇、異常を診断します | `cja-root-cause-analysis`, `aa-root-cause-analysis` | Customer Journey Analytics（CJA）、Adobe Analytics（AA） | 「先週、コンバージョンが低下した理由は何ですか？」 <br> 「1月15日の売上の急増の原因は何ですか？」 |
| エグゼクティブサマリーとKPI ダイジェスト | 関係者に提供可能なパフォーマンスの要約、処方レコメンデーション、スライドデッキの概要を作成します | `cja-executive-summary`, `cja-bacom-anomaly-tracker-v2`, `cja-cno-weekly-pulse`, `cja-reporting`, `cja`, `aa`, `dx-api` | Customer Journey Analytics（CJA）、Adobe Analytics（AA） | 「先月のエグゼクティブサマリーを教えてください」 <br> 「今四半期のデータからスライドデッキの概要を作成してください」 |
| [ コンテンツ分析](data-insights/ask-content-questions.md) | Content Analyticsのデータを利用して、コンテンツに関する一般的な質問や具体的な質問に回答します。優先すべきコンテンツ、エンゲージメントを促進する属性、売上を促進するアセットやエクスペリエンスなど、 | `analyze-content`, `cja` | Customer Journey Analytics（CJA） | 「どの種類のコンテンツを優先すればよいですか？」 <br> 「最もパフォーマンスの高い画像に共通する点は何ですか？」 |
| [AA ↔ CJA データ検証](data-insights/data-validation-aa-cja.md) | 特にAdobe AnalyticsからCustomer Journey Analyticsにアップグレードする場合は、Adobe AnalyticsとCustomer Journey Analytics間でデータを比較、監査、調整できます | `aa-cja-validation`, `cja`, `aa`, `dx-api` | ADOBE ANALYTICS + CJA | 「AA レポートスイートとCJA データビューの比較」 <br> 「AAとCJA間のページビューの検証」 |
| [ データセットとフィールドの品質を検証](data-insights/data-validation-aep.md) | Experience Platform データセットとフィールドに対して統計的およびセマンティック検証を実行し、実装後または継続的にデータ品質の問題を検出します<!--TODO: confirm skill ID(s) with engineering before publishing--> | `data-validation` | Adobe Experience Platform | 「データセット Electronics サンプル 1000の検証」 <br> 「Customers_2024 データセットの電子メールフィールドの検証」 |
| 運用時系列と因果関係分析 | オーディエンス、データセット、ジャーニーに関する過去の時系列データを、因果関係アトリビューションでクエリ、分析します | `operational-stats-causal-analysis` | すべての対象アプリケーション | 「過去90日間のオーディエンスサイズの傾向を表示」 <br> 「データセットの行数が3月3日に急増した理由を教えてください。」 |
| CJAのカスタムスキルの作成 | 分析パターンを、セッションをまたいで保持される、再利用可能で反復可能なスキルに変換します | `cja-skill-creator` | Customer Journey Analytics（CJA） | 「この週次売上分析を再利用可能なスキルに変換」 <br> 「これを月次funnel レポートのスキルとして保存」 |

## オーディエンス

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [自然言語からオーディエンスを作成](audiences/create-audience-from-natural-language.md) | 各段階で利用者の承認を得て、ステップバイステップのオーディエンス作成を連携できます | `audience-creation-flow` | Real-Time CDP（RTCDP） | 「過去30日間に購入したユーザーのオーディエンスを作成」 <br> 「カリフォルニア州の価値の高いロイヤルティメンバー向けのセグメントを作成」 |
| PQL定義の作成 | XDMのプロパティ、行動イベント、既存のオーディエンスからオーディエンス定義を組み立て、集計と時間ウィンドウをサポート | `segment-definition-assembly` | Real-Time CDP（RTCDP） | 「3つ以上の商品を閲覧したが購入しなかったユーザー向けにPQLを作成する」 <br> 「イベント条件に7日間の時間枠を追加する」 |
| オーディエンスの検索と発見 | ID、名前、セマンティック検索でオーディエンスを検索し、重複を検出して重複を分析 | `audience-search` | Real-Time CDP（RTCDP） | 「すべてのロイヤルティオーディエンスを検索」 <br> 「ホリデーショッパーのセグメントが重複していますか？」 |
| オーディエンスサイズの推定 | ポーリングを使用したAdobe Experience Platform Preview APIを使用して、PQL式のプロファイルリーチを推定します | `audience-size-estimate` | Real-Time CDP（RTCDP） | 「このオーディエンスの規模はどの程度ですか？」 <br> 「このPQL式のリーチを見積もる」 |
| オーディエンスサイズのウォーターフォール | PQLをサブ述語に分解し、各条件が最終的なオーディエンスサイズにどのように影響するかを示します | `audience-size-waterfall` | Real-Time CDP（RTCDP） | 「このPQLのウォーターフォールを表示する」 <br> 「各条件でオーディエンスが減少する方法を分類する」 |
| ターゲティング用のXDM フィールドの検索 | 名前、説明、データ値でフィールドを検索します。フィールドが存在する場所と、すでに使用されている場所を確認します | `field-discovery` | Real-Time CDP（RTCDP） | 「ロイヤルティ顧客のターゲティングに使用できるフィールドはどれですか？」 <br> 「購入履歴に関連するフィールドの検索」 |
| オーディエンスの公開/保存 | 命名規則とコンプライアンスチェックを使用して、Experience Platform Segmentation Serviceにオーディエンス定義を保持します | `audience-publish` | Real-Time CDP（RTCDP） | 「これを下書きとして保存」 <br> 「名前が「Spring Sale Buyers」のオーディエンスを公開」 |

## ジャーニー

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [自然言語からジャーニーを作成](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-create){target="_blank"} | テキストプロンプトやアップロードされた画像/フローチャートから、AJOでジャーニー作成を調整できます | `journey-create` | Adobe Journey Optimizer（AJO） | 「登録後にメールを送信し、3日間待ってからフォローアップを送信するウェルカムジャーニーを作成する」 <br> 「アップロードされたこのフローチャート画像からジャーニーを作成する」 |
| [ ジャーニーの競合を分析](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | オーディエンスの重複、スケジュールの競合、アクティブなジャーニー間の重複排除の問題を検出します | `journey-analyze-conflict` | Adobe Journey Optimizer（AJO） | 「カート放棄ジャーニーは他のジャーニーと競合しますか？」 <br> 「アクティブなジャーニー間のオーディエンスの重複をチェック」 |
| [ ジャーニーのフォールアウトを分析](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | ジャーニーの途中で顧客が離脱する場所や理由を特定し、離脱につながる行動パターンを検出します | `journey-analyze-fallout` | Adobe Journey Optimizer（AJO） | 「リエンゲージメントの過程で離脱したユーザーはどこにいますか？」 <br> 「ジャーニーXのどのノードのフォールアウトが最も高いか？」 |
| [ カスタムアクションエラーの分析](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | カスタムアクションが失敗しているか、ジャーニー内でエラー率が急増しているかを特定できます。<br> 障害が大規模な障害につながる前に、根本原因を診断します。 | `journey-analyze-custom-action` | Adobe Journey Optimizer（AJO） | 「ロイヤルティ登録ジャーニーでカスタムアクションが失敗するのはなぜですか？」 <br> 「ウェルカムジャーニーのカスタムアクション ExternalPushのエラー率を表示する」 |
| [ ジャーニーの異常値の検出](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | ジャーニーのエントリ、終了、過去のベースラインに対するカウントの送信において、予期しない急増、急減、フラットラインを検出して確認します。<br> 可能性の高い根本原因の特定： | `journey-analyze-anomaly` | Adobe Journey Optimizer（AJO） | 「昨日のウェルカムジャーニーのエントリが低下した理由は何ですか？」 <br> 「今週の買い物かごの放棄ジャーニーで、離脱が急増しましたか？」 |
| [ビジネスパフォーマンス分析](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | ジャーニーのパフォーマンスを分析し、パフォーマンスの低いジャーニーを最適化するための具体的な機会を特定します。<br> トレンド、ボトルネック、期待できる要因などを明らかにし、エンゲージメントとコンバージョンを向上させます。<br> ビジネスパフォーマンスのインサイトに基づいて、ジャーニーのデザイン、ターゲティング、メッセージ戦略を調整するための、実用的なレコメンデーションを取得します。 | ジャーニー分析 | Adobe Journey Optimizer（AJO） | 「ジャーニー[ジャーニー名]のパフォーマンスを分析し、最適化を推奨します。」 <br> 「ジャーニー[ジャーニー名]が先月と比較してパフォーマンスが低いのはなぜですか？」 <br> 「ジャーニー[ジャーニー名]のパフォーマンスを向上させるにはどうすればよいですか？」 <br> 「ジャーニーの[ジャーニー名]のどの部分が、コンバージョンまたはエンゲージメントを制限している可能性がありますか？」 |
| [ ジャーニーの健全性の分析](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | 設定の健全性の問題について、ジャーニーのインベントリを監査します。<br> 欠けている一般的な名前、古いドラフトまたはライブジャーニー、大規模なジャーニー、既存のクローズドジャーニー、類似のアクション名やイベント名などを検索できます。<br> 設定のクリーンアップとスタビライズに関する推奨事項を取得します。 | ジャーニー分析 | Adobe Journey Optimizer（AJO） | 「自分のジャーニー設定を監査します。」 <br> 「どのジャーニーが古くなっているか、またはクリーンアップが必要か？」 |
| [ ジャーニーのバージョンを比較](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | 2つのジャーニーバージョンを比較し、ノード、接続、ジャーニーレベルのプロパティ変更の構造化された差分を確認します | `journey-analyze-version-comparison` | Adobe Journey Optimizer（AJO） | 「ウェルカムジャーニーのバージョン 2と3を比較」 <br> 「これら2つのジャーニーバージョン間で何が変更されたか？」 |
| [ ジャーニーを通じてプロファイルを追跡](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#trace-journey-profile){target="_blank"} | 公開されたジャーニーの読み取り専用プロファイルレベルの実行データを取得します。<br> 各ノードに入ったプロファイルの数と、分岐の分割方法を確認できます。<br> エラーが発生したプロファイルとその理由を検索するか、単一のプロファイルのノードごとのパスに従います。 | トレースジャーニープロファイル | Adobe Journey Optimizer（AJO） | 「[ジャーニー名]を通じてプロファイルをトレースします。」 <br> 「過去7日間に[ジャーニー名]でエラーが発生したプロファイル、その理由は何ですか？」 <br> 「プロファイル [IDまたは電子メール ]の[ジャーニー名]経由のパスを表示する」 |
| [ ジャーニー実行タイムラインの分析](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-execution-timeline){target="_blank"} | オーディエンス読み込みジャーニーのバッチのエンドツーエンドのタイムラインを取得します。<br> オーディエンスの書き出し、ジャーニーの実行、配信の開始と終了にかかる時間を確認できます。<br> 入力、終了、または実行時間について、プロファイルレベルのP95およびP99を取得します。 | ジャーニーの実行タイムライン | Adobe Journey Optimizer（AJO） | 「オーディエンスの読み取りジャーニー[ジャーニー名]が実行されるまでにどのくらいの時間がかかりましたか？」 <br> 「[ジャーニー名]のオーディエンスのエクスポート、ジャーニーの実行、配信のタイムラインをバッチで表示します。」 <br> 「どの[ジャーニー名]のバッチが最も時間がかかり、どの段階で遅延が発生しましたか？」 |

**関連情報**

* [AIの操作](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-features#cx-coworker-skills){target="_blank"}では、Adobe Journey Optimizerの共同作業者と利用可能なスキルの概要を提供します。

## Journey Optimizer コンテンツ管理


| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [ ブランドガイダンスの適用](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | キャンペーンの声、ライティング、画像、用語、法的ガイダンス用の承認済みブランドガイドラインを検索、選択、適用できます。 | `brand-lookup` | Adobe Journey Optimizer（AJO） | 「Acme ブランドの書き込みおよびビジュアルガイドラインを取り寄せてください。」 |
| [ コンテンツの準備状況を確認](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | キャンペーンのコンテンツを見直して、ブランドボイス、編集品質、エンゲージメント、明瞭性、準備状況を確認します。 | `check-content-readiness` | Adobe Journey Optimizer（AJO） | 「このメールのコピーは送信準備ができていますか？ ブランドの声、明瞭性、アクセシビリティ、コンプライアンスを確認してください。」 |
| [ コンテンツオーサリングの調整](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | サポートされているチャネルをまたいでキャンペーンコンテンツを計画、作成、レビュー、分析、保存します。 | `orchestrate-content-authoring` | Adobe Journey Optimizer（AJO） | 「この概要からFall Saleのメールキャンペーンのフルコンテンツオーサリングを実行し、最終的なHTMLを確認して保存します。」 |
| [ コンテンツデザインの評価](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | ビジュアル実装の分析、レイアウトとデザインのギャップの特定、階層、間隔、イメージ、CTAの改善の提案が可能です。 | `assess-content-design` | Adobe Journey Optimizer（AJO） | 「このメールの見た目はどうですか？ 階層、間隔、密度、画像、CTAを確認してください。」 |
| [Figma](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"}からメールを作成 | コピーの出荷準備が整った時点で、ライブ Figma フレームから最終的なメール HTMLを作成します。別のレイアウトプランは必要ありません。 | `build-email-from-figma` | Adobe Journey Optimizer（AJO） | 「この Figma フレームから最終的なメール HTML を作成してください。デザインのコピーは発送する必要があります。」 |
| [ コンテンツ戦略を探る](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 顧客接点、チャネル、オーディエンス、メッセージのテーマをまたいでキャンペーン戦略を比較し、執筆前に各メッセージを計画します。 | `explore-content-strategy` | Adobe Journey Optimizer（AJO） | 「単一のウィンバックメールと 3 タッチメールおよび SMS プログラムを比較してください。」 |
| [ コンテンツを生成](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 電子メールやSMS、プッシュ通知、WhatsApp、ランディングページなど、対応しているチャネル向けに、制約のある新しいマーケティングメッセージを作成したり、作成したりできます。 | `generate-content` | Adobe Journey Optimizer（AJO） | 「承認済みのキャンペーンの方向性に基づき、メール、プッシュ通知、SMS のブランドに即したローンチコピーを作成してください。」 |
| [ コンテンツ概要の作成](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 承認済みのキャンペーンの方向性を、オファー、トーン、キーメッセージ、チャネル、ロケール、バリエーション、必要なコンテンツの要件に変換します。 | `content-brief` | Adobe Journey Optimizer（AJO） | 「この概要を、米国の購読を中断したユーザー向けの親しみやすいウィンバックメールの作成要件に変換してください。内容には、日曜日まで 20％ オフを含め、KPI は CTR とします。」 |
| [画像の生成](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | ヒーロー画像、切り抜き、オーバーレイ、バリエーション、署名済みアセットなど、承認済みプレースメントのキャンペーンビジュアルを作成または変換します。 | `generate-image` | Adobe Journey Optimizer（AJO） | 「承認済みのブランドの指示に従って、この春のセールのメール用のプレミアムなヒーロー画像を生成してください。」 |
| [ チャネルコンテンツを保存](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 承認されたキャンペーンコンテンツをドラフトアセットとして保存するか、AJOなどのサポートされているアクションソリューションでソーステンプレートに入力します。 | `save-channel-content` | Adobe Journey Optimizer（AJO） | 「承認済みのコンテンツをソーステンプレートに入力し、レビューの準備を整えてください。」 |
| [ コンテンツの修正と再生成](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 文言、トーン、翻訳、件名、CTA、レビュー結果など、既存のキャンペーンコンテンツに変更を加えて調整できます。 | `revise-regenerate-content` | Adobe Journey Optimizer（AJO） | 「承認済みのオファーと CTA を維持しながら、より暖かみのあるトーンにしてください。」 |

**関連情報**

* [AIの操作](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-features#cx-coworker-skills){target="_blank"}では、Adobe Journey Optimizerの共同作業者と利用可能なスキルの概要を提供します。

## マーケティングプログラム

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| プログラムの作成 | 既存のプログラムテンプレートを新しいプログラムに適応し、平易な言語の説明やアップロードされた概要から生成されたスマートキャンペーン、スケジューリング、プレースホルダーメールを活用します | `build-programs` | Adobe Marketo Engage | 「8月の製品デモ用にウェビナー登録プログラムを作成する」 <br><br> 「リードが50点に達したときにトリガーするプログラムを作成する」 <br><br> 「非アクティブな90日間のリードの3通のメール再エンゲージメントシリーズを作成する」 |
| ブリーフからプログラムを立ち上げる | 平易な言葉で作成した概要やアップロードしたキャンペーンドキュメントを、作業中のプログラムに変換できます。最も近いテンプレートを複製し、スマートキャンペーンやトークンを引き継ぎ、イベントの詳細を更新します。 新しいスマートキャンペーンはレビュー用に非アクティブのままになります | `build-programs` | Adobe Marketo Engage | 「9月10日にシカゴでウェビナーを開催します。 プログラムを自分で設定する&quot;<br><br>&quot;この概要から来月のロードショープログラムを設定し、イベント トークンを更新する&quot; |
| 既存のプログラムの複製と調整 | 新しい都市、四半期、地域の以前のプログラムをコピーし、日付、トークン、命名を更新します。 子スマートキャンペーンは、アクティベートするまで引き継がれ、非アクティブのままになります | `build-programs` | Adobe Marketo Engage | 「ニューヨークの前四半期のイベントプログラムを複製して、10月17日に停止し、日付とトークンを更新します」 <br><br> 「英国のオーディエンス向けにシカゴのロードショープログラムを複製します」 |
| 選定ロジックを使用したスマートキャンペーンの構築 | トリガーまたはバッチ方式のスマートキャンペーンの作成、フォームへの入力やリーチのスコアなどのスマートリストルールの追加、メールの送信などのフローステップの設定 | `build-programs` | Adobe Marketo Engage | 「リードがお問い合わせフォームに入力したときにウェルカムメールを送信するトリガーキャンペーンを作成する」 <br><br> 「スコアが50に達したリードのバッチキャンペーンを作成し、メール送信手順を追加する」 |

## ロイヤルティ

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [ ロイヤルティに関する課題の作成、編集、管理](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/loyalty-challenges/loyalty-coworker-skills#loyalty-challenge-management){target="_blank"} | ロイヤルティプログラム管理を簡素化し、迅速化したい | `loyalty` | Adobe Journey Optimizer（AJO） | 「会員に新しい季節の飲み物を試すように促すチャレンジを作成する」 <br> 「最も高い会員の脱落レートでロイヤルティのチャレンジを表示する」 |
| [ ロイヤルティプログラムのパフォーマンスを分析](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/loyalty-challenges/loyalty-coworker-skills#loyalty-data-insight){target="_blank"} | 自然言語を使用して、ロイヤルティポイント、メンバー層、引き換え、収益指標をクエリし、分析します | `loyalty-insights` | Adobe Journey Optimizer（AJO） | 「2026年8月に付与されたロイヤルティポイント数はいくつですか？」 <br> 「2026年8月の期間中のロイヤルティプログラムの総収益を日別に示してください。」 |
| [ ロイヤルティの機会の検索](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/loyalty-challenges/loyalty-coworker-skills#loyalty-opportunities){target="_blank"} | ロイヤルティプログラムのトレンドやパフォーマンスデータにもとづいて特定のチャレンジの機会をリクエストし、それを実際のチャレンジに変えます | ロイヤルティの機会 | Adobe Journey Optimizer（AJO） | 「会員の支出額を増やす可能性があるロイヤルティの機会は何ですか？」 <br> 「非アクティブなメンバーを取り戻す機会を表示する」 |

**関連情報**

* [AIの操作](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-features#cx-coworker-skills){target="_blank"}では、Adobe Journey Optimizerの共同作業者と利用可能なスキルの概要を提供します。

## 決定

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [決定ルールの生成、説明、シミュレーション、最適化](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/experience-decisioning/experience-decisioning-coworker-skills#rules-ranking){target="_blank"} | 自然言語を使って適格性ルールやランキング式を作成し、平易な英語の説明を得ることができます。<br> 最大3つのプロファイルに対してテストします。<br> PQLの構文を手作業で記述することなく、PQLのサイズ制限に合わせて書き換えます。 | 決定ルールワークフロー | Adobe Journey Optimizer（AJO） | 「ティア 2以上のロイヤルティメンバーを対象とした実施要件ルールを作成します。」 <br><br> 「このルールを自然言語で説明します。」 <br><br> 「テストプロファイルでこのルールをシミュレートします。」 <br><br> 「このPQL ルールを自分に合わせて最適化します。」 |

**関連情報**

* [Coworker for Decisioning](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/experience-decisioning/experience-decisioning-coworker-skills){target="_blank"}は、Adobe Journey Optimizerの意思決定スキルに関する詳細なガイダンス、ユースケース、プロンプトのベストプラクティスを提供します。

## チャネル

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [ チャネル設定の調査](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/channels-coworker-skills#channel-operation){target="_blank"} | メール、SMS、プッシュ、ダイレクトメール、アプリ内、webなどの標準チャネルの読み取り専用チャネル設定（プリセット）と資格情報を表示、リスト化、検索、検査できます。<br> また、プッシュ資格情報、メールサブドメイン、SMSおよびWhatsApp資格情報、ファイルルーティング、LINE チャネル設定、ライブアクティビティレジストリなどの関連リソースも参照します。 | チャネル操作 | Adobe Journey Optimizer（AJO） | 「サンドボックスで使用できるチャネルプリセットは何ですか？」 <br> 「メールチャネルの設定をすべて表示する」 <br> 「マーケティングメール設定に設定されている送信者アドレスと返信先は何ですか？」 |
| [ カスタムチャネルの作成と管理](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/channels-coworker-skills#channel-builder){target="_blank"} | カスタムのアウトバウンドチャネルを手動セットアップ、curl コマンド、またはAPI ドキュメントリンクから作成、テスト、更新、リスト化、取得、削除します。<br> チャネルの設定、認証、スロットリング、ペイロードの定義について解説します | チャネルビルダー | Adobe Journey Optimizer（AJO） | 「SMS プロバイダーの新しいカスタム チャネルの作成を支援してください。」 <br> 「このAPI リファレンスからカスタムチャネルを作成：[link]。」 <br> 「カスタムチャネルをリストアップする」 |

**関連情報**

* [Coworker for channels](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/channels-coworker-skills){target="_blank"}は、Adobe Journey OptimizerのChannel OperationおよびChannel Builder スキルに関する詳細なガイダンス、ユースケース、サンプルプロンプトを提供します。

## Journey Optimizerでのコンテンツ制作

Adobe Workfront Chatを使用して、キャンペーンメッセージのコピーやAdobe HTMLを計画、生成、評価、調整し、承認されたコンテンツをJourney Optimizerに直接保存または引き渡します。

### メッセージのコピー

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [ マーケティング概要のキャプチャ ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | キャンペーン戦略をキャプチャし、クリエイティブ概要をシードします。 | `capture-marketing-brief` | Adobe Journey Optimizer（AJO） | 「季節ごとの製品発売のためのマーケティング概要を作成する」 <br> 「このキャンペーン戦略をマーケティング概要に変換する」 |
| [ クリエイティブの概要をキャプチャ ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | コピー実行仕様を構造化し、コンテンツプランマトリックスを構築します。 | `capture-creative-brief` | Adobe Journey Optimizer（AJO） | 「この承認済みマーケティング概要からクリエイティブ概要を作成する」 <br> 「メールとSMS キャンペーンのコンテンツ プラン マトリックスを作成する」 |
| [ コンテンツ戦略を計画](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | コピーを生成する前に、メッセージマップ、物語の円弧、チャネルの役割をブレインストーミングします。 | `plan-content-strategy` | Adobe Journey Optimizer（AJO） | 「電子メールとプッシュ通知で製品発売のメッセージ戦略を計画する」 <br> 「ウェルカムキャンペーンの物語の展開を提案する」 |
| [ コピーを生成](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 電子メール、SMS、プッシュ通知、WhatsApp、ソーシャル広告、バナー用に、ブランドに即した最新のコピーを生成。 | `generate-copy` | Adobe Journey Optimizer（AJO） | 「新しいシーズンコレクションを告知するブランドに即したメールを作成する」 <br> 「カートを放棄した顧客にSMS リマインダーをドラフトする」 |
| [画像の生成](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | Fireflyを使用して、キャンペーン画像を生成、切り抜き、オーバーレイ、バリエーション、署名します。 | `generate-image` | Adobe Journey Optimizer（AJO） | 「季節限定キャンペーンメールのヒーロー画像を生成」 <br> 「この承認済みキャンペーン画像からバナーバリエーションを作成」 |
| [ コピーを評価](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | ブランドおよびチャネル基準に照らして、既存のコピーを評価およびスコアリングします。 | `evaluate-copy` | Adobe Journey Optimizer（AJO） | 「このメールコピーをブランドガイドラインに照らして評価する」 <br> 「このプッシュメッセージが当社のチャネル標準を満たしているかどうかを確認する」 |
| [ コピーを編集](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 既存のコピーをインプレースで編集できます。評価修正、言い換え、翻訳、修正が必要です。 | `edit-copy` | Adobe Journey Optimizer（AJO） | 「この電子メールコピーを修正して評価フィードバックに対応する」 <br> 「この承認済みSMS コピーをフランス語に翻訳する」 |
| [ キャンペーンコンテンツを展開](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | ファンは承認済みのコンテンツプランマトリックスを、チャネル、ロケール、オーディエンス、バリエーションをまたいでユニットごとのコピーに変換します。 | `expand-campaign` | Adobe Journey Optimizer（AJO） | 「この承認済みコンテンツプランの各チャネルのコピーを生成する」 <br> 「このキャンペーンを各オーディエンスの英語とフランス語のバリエーションに展開する」 |
| [ ビジュアル HTMLの分析](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | HTMLのコピーをスクリーンショットにレンダリングして、視覚的な検査を行います。 | `analyze-visual-html` | Adobe Journey Optimizer（AJO） | 「このメールをHTMLでレンダリングして、レイアウトを調べることができます」 <br> 「このキャンペーンのHTMLのスクリーンショットを表示する」 |
| [ コンテンツを保存](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 承認されたコンテンツを、Adobe Journey Optimizer、Adobe Campaign v8、またはMarketoに保存します。 | `save-content` | Adobe Journey Optimizer（AJO） | 「この承認済みメールコンテンツをJourney Optimizerに保存」 <br> 「承認済みSMS コピーをJourney Optimizerに保存」 |

### メールデザイン

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [電子メールを作成](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | マーケティング目標やブランド入力に基づいて、ブロック構造とスタイルを設定できます。 | `compose-email` | Adobe Journey Optimizer（AJO） | 「ブランドガイドラインに従って、製品リリース用のメールレイアウトを計画する」 <br> 「ヒーローセクション、製品ハイライト、call to actionを含むウェルカムメールを作成する」 |
| [電子メールを作成](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | レイアウトプラン、スクリーンショット、Figma デザインリンクからメールHTMLを作成、適応、編集、改良します。 | `build-email` | Adobe Journey Optimizer（AJO） | 「この承認済みレイアウトプランからメール HTMLを作成」 <br> 「このFigma デザインリンクからメールを作成」 |
| [ デザインシステムを維持](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | トークン、レイアウトパターン、ブランド言語といった、ブランドの再利用可能なメールデザインシステムを維持する。 | `maintain-design-system` | Adobe Journey Optimizer（AJO） | 「承認済みのブランドカラーでメールデザインシステムを更新する」 <br> 「この再利用可能な製品レイアウトをメールデザインシステムに追加する」 |
| [ コンプライアンスのレビュー](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | ブランドやチャネルのガイドラインや配信品質の基準に照らして、組み立てられた電子メールを監査。 | `review-compliance` | Adobe Journey Optimizer（AJO） | 「この電子メールをブランドおよびチャネルのガイドラインに照らして確認する」 <br> 「ハンドオフ前に配信品質の問題についてこの電子メールを監査する」 |
| [ デザインのレビュー](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 階層、間隔、物語の流れ、ブランドフィットに関する主観的なデザインフィードバックを提供します。 | `review-design` | Adobe Journey Optimizer（AJO） | 「このメールの視覚的な階層と間隔を確認してください」 <br> 「このメールのデザインがブランドに合っているかどうかを評価してください」 |
| [ アクセシビリティのレビュー](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | WCAG 2.1 AA アクセシビリティ監査を実行します。 | `review-accessibility` | Adobe Journey Optimizer（AJO） | 「このメールをWCAG 2.1 AA アクセシビリティの問題について監査する」 <br> 「このメールのカラーコントラストと画像の代替テキストを確認する」 |
| [電子メールの引き継ぎ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 承認されたHTMLを書き出して、Adobe Journey OptimizerまたはAdobe Campaignに配信します。 | `handoff-email` | Adobe Journey Optimizer（AJO） | 「この承認済み電子メールをHTMLからJourney Optimizerにエクスポート」 <br> 「承認済み電子メールをJourney Optimizerに渡す」 |

**関連情報**

* [Coworker for content management](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"}では、Adobe Journey Optimizerのコンテンツ管理ツールと利用可能なスキルについて詳しく説明しています。

## Campaign v8

共同作業チャットを使用すると、Adobe Campaign v8での配信の検索と更新、アセットの管理、データモデルの調査、ワークフローの検査、検証、トラブルシューティングを行うことができます。

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| 配信の検索と検査 | 名前、フォルダー、チャネル、ステータスで配信を検索し、チャネルコンテンツやSMTP設定を含む配信の詳細を取得し、再利用可能なメールコンテンツテンプレートを参照し、組み込みの配信レポートを確認します | `find_delivery`, `describe_delivery`, `find_content_template`, `read_delivery_indicator` | Adobe Campaign v8 | 「名前に「ニュースレター」が含まれるメールコンテンツテンプレートを検索します。」 ・ 「下書きメール配信を表示する」 ・ 「今月失敗した配信の数は？」 ・ 「この配信で使用する件名と送信者は何か？」 |
| 配信の作成と更新 | チャネルテンプレートと名前付きコンテンツから配信またはテンプレートを作成し、既存の配信のラベルとチャネルごとのメッセージコンテンツを編集します | `create_delivery`, `update_delivery` | Adobe Campaign v8 | 「ニュースレターのコンテンツテンプレートを使用してメールを作成する」 ・ “ Change the subject of the Summer Launch email.” ・ “ Replace the HTML content of this delivery.” |
| 配信を送信せずに配信を準備 | 配信をブロードキャストせずにターゲットを解決し、パーソナライゼーションをレンダリング | `prepare_delivery` | Adobe Campaign v8 | 「サマーローンチ配信の準備」 ・ 「この配信で準備を実行しますが、送信しないでください。」 |
| メール SMTPおよびweb分析設定の設定 | メール配信のSMTP ヘッダー設定、およびweb分析アカウントとトラッキングタグを設定します | `update_email_smtp_config`, `update_email_web_analytics` | Adobe Campaign v8 |  |
| アセットと添付ファイルの管理 | アセットとしてファイルをアップロードし、そのメタデータと公開URLを読み取り、プライベートアセットを公開し、アセットを実際の添付ファイルとして配信にリンクします | `upload_asset`, `get_asset_url`, `publish_asset`, `attach_asset` | Adobe Campaign v8 | 「この画像をアップロードして、メールで使用できるようにします。」 ・ 「アップロードした画像のパブリック URLを教えてください。」 ・ 「私がアップロードしたPDFをサマーローンチの配信に添付します。」 |
| キャンペーンの調査 | キャンペーンとテンプレートを検索し、子ワークフローや配信を含むキャンペーンの詳細を確認できます | `find_campaign`, `describe_campaign` | Adobe Campaign v8 |  |
| ワークフローの把握と検証 | ワークフローを検索し、ワークフローを要約したり、ワークフローのアクティビティと配信のタッチポイントをドリルダウンしたり、ワークフロー定義を静的に検証したりできます | `find_workflow`, `describe_workflow`, `validate_workflow` | Adobe Campaign v8 | 「ようこそ」ワークフローについて説明します。 ・ 「このワークフローで使用されている配信はどれですか？」 ・ 「ようこそワークフローを検証します。」 |
| ワークフローの制御 | ライフサイクルコマンド（開始、一時停止、停止、再開、またはウェイクアップ）を使用してワークフローを駆動し、ワークフロー内の配信アクティビティを再設定します | `control_workflow`, `update_workflow_delivery_activity` | Adobe Campaign v8 | 「ようこそワークフローを開始します。」 ・ 「このワークフローを一時停止します。」 |
| ワークフローのトラブルシューティング | ワークフローの実行時、実行ジャーナル、現在のタスク、保留中のエンジンコマンドなど、多くのワークフローの正常性を一度に確認できます | `read_workflow_health`, `read_workflow_history`, `read_workflow_logs`, `read_workflow_tasks`, `read_workflow_jobs` | Adobe Campaign v8 |  |
| データモデルの探索と拡張 | スキーマカタログを参照し、スキーマの構造を調べ、スキーマから行を読み取り、新しいスキーマを作成し、物理SQL テーブルを作成または変更します | `find_schema`, `describe_schema`, `read_schema_entity`, `create_schema`, `update_database_structure` | Adobe Campaign v8 | 「受信者に関連するスキーマを検索」 ・ 「受信者スキーマの説明」 ・ 「ロイヤルティ設定のカスタムスキーマを作成する」。 |

**関連情報**

* [Adobe Campaignの基本を学ぶ](https://experienceleague.adobe.com/ja/docs/campaign/campaign-v8/new/get-started){target="_blank"}では、Adobe Campaign v8の概要を説明しています。

## 最適化

Adobe Workfront Chatを使用すれば、エクスペリエンスの閲覧、分析、計画をおこない、Adobe Adobe Targetのアクティビティ、オーディエンス、レコメンデーションの作成、実行、トラブルシューティングをおこなえます。

### 実験の分析と戦略

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| 実験を参照および探索 | 実験の概要、リスト、カウント、生の結果、インサイト、機会などを検索できます | `experiment-explorer` | Adobe Target/Adobe Journey Optimizer | 「自分の実験を表示」 ・ 「アクティブなテストのリスト」 ・ 「実行している実験の数」 |
| 実験パフォーマンスを分析 | CJAのデータを拡充することで、ポートフォリオのランダウン、1回限りの実験によるヘルスチェック、エグゼクティブブリーフ、各実験間のレポートを指標とともに取得できます | `experiment-analysis` | Adobe Target/Adobe Journey Optimizer | 「A/B テストのパフォーマンスはどうか？」 ・ 「CJA指標を使用して、自分のアクティビティに関するレポートを生成する」 ・「このテストは正常ですか？」 |
| 実験の計画と設計 | 実行する次に最も効果の高いテスト、名前付きトピックのデザイン、目標から指標への翻訳、失敗したテストの回復ガイダンス、シーケンス付きのマルチテストロードマップを取得します | `experiment-strategist` | Adobe Target/Adobe Journey Optimizer | 「次に何を調べればいいんですか？」 ・ 「チェックアウトコンバージョンを改善するための実験の設計を支援」 ・「第3四半期のテストロードマップの構築」 |
| 実験履歴を検索 | 過去の実験から仮説、学習、結果、処理を取得したり、トピックごとに以前の実験を見つけたり、外部CSVを取り込んで結果を充実させることができます | `experiment-knowledge-base` | Adobe Target/Adobe Journey Optimizer | 「実験Xについて何を知っていますか？」 ・ 「この仮説を以前にテストしたことがありますか？」 ・ 「このCSVを取り込む」 |

### ターゲットアクティビティとオーディエンス

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| ターゲットエンティティを参照 | アクティビティ、オファー、オーディエンス、mbox、プロパティ、ワークスペース、AT.js設定、応答トークン、リビジョン履歴を検索、検査、カウントします。 また、アクティビティが強制したエクスペリエンスのスクリーンショットをキャプチャすることもできます | `target-browse` | Adobe Target | 「自分のA/B テストのリスト」 ・ 「今月のアクティビティの数は？」 ・ 「アクティビティ 12345の詳細を表示」 |
| アクティビティパフォーマンスの分析 | 1つのアクティビティのコンバージョン率、上昇率、信頼区間、売上、露出の数を取得します。 事実だけを述べ、決して勝者を宣言しない | `target-analyze` | Adobe Target | 「アクティビティ Xのパフォーマンスはどうですか？」 ・ 「コンバージョンリフトを表示する」 ・ 「チェックアウトテストのAOVは何ですか？」 |
| 船を取得するか、判決を停止 | 未処理カウントと構成欠陥チェックの2つの比率の有意性から計算された、アクティビティのSHIP、WAIT、STOP、またはFIXの推奨事項を取得します | `target-activity-verdict` | Adobe Target | 「このテストは発送すべきですか？」 ・ 「どのバリエーションが勝ちましたか？」 ・ 「これはまだ重要なことですか？」 |
| アクティビティの作成と設定 | アクティビティ、オファー、応答トークンの作成、更新、設定、QA プレビューURLの生成、オファーコンテンツのオーサリングまたは最適化 | `target-design` | Adobe Target | 「ホームページのA/B テストを作成」 ・ 「トラフィック分割を更新」 ・ 「このオファーのJSを最適化」 |
| Visual Experience Composer アクティビティの作成 | Visual Experience Composer （VEC）アクティビティを作成および編集し、ライブページ URLに対するDOM修正としてバリエーションをオーサリングし、それらをスコープするページ配信オーディエンスを作成します | `target-vec` | Adobe Target | 「ホームページ用にVEC A/B テストを作成する」 ・ 「ビジュアルエディターでヒーローの見出しを変更する」 |
| 完全なテストをゼロから設定する | A/B、XT、VEC テスト用のガイド付きエンドツーエンドのアクティビティ作成では、要件収集、前提条件、作成、スケジューリングと優先度、QA リンク、オプションのアクティベーションなどをカバーしています | `target-setup` | Adobe Target | 「完全なA/B テストの設定を説明する」 ・ 「Targetが初めてなので、最初のテストを作成する際に役立つ」 |
| 監査プログラムの正常性 | リスクと衝突の検出、誤った設定による結果、オーディエンスとオファーの健全性、迅速な対応に関する推奨事項など、プログラム全体の健全性監査を実施します | `target-intelligence` | Adobe Target | 「Target アクティビティの監査」 ・ 「危険なテストまたは誤った設定のテストを見つける」 ・ 「クリーンアップする必要があるものは何か？」 |
| 成功パターンを見つける | パターンの勝者、効果的な戦略、パフォーマンスの高いオーディエンスやコンテンツなど、ターゲットの履歴を調べ、独自のデータにもとづいて次にテストすべき内容をレコメンデーションします | `target-strategist` | Adobe Target | 「何がうまくいっているんですか？」 ・ 「自分の勝利パターンを見せてください」 ・ 「過去の結果に基づいて次にテストすべきことは何ですか？」 |
| サンプルサイズとデュレーションの計算 | A/B/n サンプルサイズ、テスト時間、コンバージョン率と訪問者あたりの売上の指標に対する検出可能なリフトをBonferroni補正で計画します | `target-test-calculator` | Adobe Target | 「A/B テストを実行するには、どのくらいの時間が必要ですか？」 ・ 「どのサンプルサイズが必要ですか？」 ・ 「テストの電源はまだ入っていますか？」 |
| プログラムレベルのパフォーマンスロールアップを取得 | 概要パネル、最近のローンチ表、すべてのアクティビティの勝者/損失/上昇率の総国勢調査、シングルアクティビティのトレンドとモメンタムリードを確認できます | `target-portfolio-report` | Adobe Target | 「Target プログラムのヘルスチェックを受ける」 ・ 「最も高いテストと最低のテストはどれですか？」 ・ “活動Xは勝利に向かって傾向がありますか？” |
| 自然言語からオーディエンスを作成 | 自然言語の説明、明示的なルール条件、インラインまたはアップロードされた値リストなどから、ターゲットネイティブオーディエンスを作成または編集します。 リクエストをルール文法にマッピングし、書き込む前にルールツリーを検証します | `target-audience-composer` | Adobe Target | 「カリフォルニアからの再訪問者のオーディエンスを作成」 ・ 「これらの郵便番号からオーディエンスを作成」 ・ 「再訪問者にオーディエンス Xを絞り込む」 |

### レコメンデーション

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| Recommendations エンティティを参照 | Recommendationsの基準、コレクション、デザイン、プロモーション、除外、カタログ、フィードを参照および検査し、さらにクリーンアップのアドバイスとカタログ属性のガイダンスを取得します | `target-recs` | Adobe Target | 「推奨事項の基準を一覧表示」 ・ 「どのようなデザインを持っていますか？」 ・ 「どの領域をクリーンアップできるか？」 |
| Recommendationsの問題の診断 | アクティビティ、基準、フィード、コレクション、デザインチェーンをトレースして、レコメンデーションが空であるか、古いか、表示されない理由を説明します | `target-recs-diagnose` | Adobe Target | 「なんで僕の推薦状は空っぽなんだい？」 ・ “ Why has my recs activity been ‘results not ready’ for 48 hours?” 「なぜ私のレック活動は48時間も“結果が出ない”のですか？」 |
| オーサーのレコメンデーション | レコメンデーションの基準、コレクション、デザイン、除外、プロモーション、フィード、およびレコメンデーションアクティビティを作成および更新します。これには、多くのアクティビティをまたいだゲーテッドバルク操作が含まれます | `target-recs-design` | Adobe Target | 「最も閲覧された」基準を作成する」 ・ 「50 ドル未満の在庫商品のコレクションを作成する」 ・ 「すべてのセールアクティビティでブラックフライデーの日付を適用する」 |

## 基本要素

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| 製品情報とドキュメント | Adobeの公式ドキュメントで、ハウツー、概念、トラブルシューティング、ベストプラクティスに関する質問に回答します | `product-knowledge` | すべての対象アプリケーション | 「ストリーミング宛先を設定するにはどうすればよいですか？」 <br> 「バッチセグメントとストリーミングセグメントの違いは何ですか？」 |
| Experience Platform / Journey Optimizer エンティティのクエリ | プラットフォームエンティティに関する質問の主要なエントリポイントとして機能し、必要に応じてKG、フィールドディスカバリー、またはAPIにルーティングできます | `operational-insights` | すべての対象アプリケーション | 「データセットはいくつありますか？」 <br> 「アクティブなすべてのジャーニーを表示」 <br> 「宛先を一覧表示」 |
| ナレッジグラフクエリ | 単一のSQL クエリを使用したカウントの集計、エンティティ間の結合、関係検索、メタデータの検索 | `knowledge-graph` | すべての対象アプリケーション | 「どのオーディエンスがこのデータセットを使用しますか？」 <br> 「スキーマとデータセット間の関係を表示」 |
| Experience Platform/Journey Optimizer/Customer Journey Analytics APIの操作 | ナレッジグラフにない突然変異、リアルタイム状態チェック、およびエンティティタイプに対して、直接API ゲートウェイを提供します | `cxo-api` | すべての対象アプリケーション | 「データセット Xを削除」 <br> 「バッチ取り込みジョブのステータスを確認」 |
| エンティティの解決とリンク | セマンティック検索と字句検索を使用して、実際のExperience Platform エンティティに対するエンティティのメンションを解決し、XDM フィールドを検出します | `entity-linking` | Adobe Experience Platform | 「実際のオーディエンスに&#39;Holiday Shoppers&#39;を解決する」 <br> 「購入履歴に関連するフィールドを検索する」 |
| カスタムスキルの管理 | 再利用可能なユーザー所有スキルを保存、変更、削除できます。これらのスキルは、セッションをまたいで保持されます | `manage-skill` | すべての対象アプリケーション | 「そのワークフローをスキルとして保存」 <br> 「週次レポートスキルを削除」 <br> 「これを再利用可能なスキルに変換」 |
| ストリーミング容量とデータ侵害の監視 | サンドボックスをまたいで、現在および過去のストリーミング利用状況、キャパシティ、侵害ステータスを確認できます | `observability-streaming-capacity`, `observability-streaming-usage`, `observability-capacity-breaches` | Adobe Experience Platform | 「現在のサンドボックスの現在のストリーミング容量は何ですか？」 <br> 「私の現在のサンドボックスは、先週の容量制限に違反していますか？」 |
| [ ヘルスチェックの評価結果を表示](https://experienceleague.adobe.com/en/docs/experience-platform/run-and-operate/health-checks/overview) | サンドボックスの最新のヘルスチェック評価を表示し、失敗したチェックをドリルダウンして、影響を受けるエンティティを確認します | `rao-view-latest-health-checks-assessment` | Adobe Experience Platform | 「サンドボックスの何が問題ですか？」 <br> 「最新のヘルスチェック評価について教えてください」 <br> 「カスタム名前空間説明チェックの問題は何ですか？」 |
| ヘルスチェックの問題を修正 | 変更が行われる前に承認を得て、フラグ付きのID名前空間、結合ポリシー、スキーマの問題をチャットから直接修正します | `rao-remediate-identity-namespace-description`, `rao-remediate-merge-policy-duplicate-name`, `rao-remediate-missing-audit-field-group`, `rao-remediate-default-merge-policy-naming` | Adobe Experience Platform | 「ID名前空間の説明を修正」 <br> 「重複する結合ポリシー名を修正」 <br> 「監査フィールドグループが欠落しているスキーマを修正」 <br> 「デフォルトの結合ポリシーの名前付けを修正」 |

## データ管理

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [最適化またはクリーンアップに値するデータを見つける](./data-management/manage-data-lake-retention.md#find-data-worth-optimizing) | 最大のデータセット、使用頻度の低いデータセット、忘れられたデータセットを、クリーンアップやデータレイクの保持ポリシーの候補として表面化することで、エクスペリエンスイベントのデータを最適化できるかどうかを把握できます | `List datasets` | Adobe Experience Platform | 「データを最適化できる気がする」 <br> 「データの値の理解を支援」 <br> 「サンドボックスデータの最適化」 <br> 「サンドボックスデータセットのクリーンアップ」 |
| [ データセットの使用状況を調査し、保持を管理](./data-management/manage-data-lake-retention.md#check-how-actively-a-dataset-is-used) | データセットを詳細に分析し、そのデータセットがどのように使用されているかを確認したら、データレイクの潜在的な保持ポリシーの影響をモデル化し、何か変更する前にレビューと承認を行いながら、そのポリシーを設定、変更、削除します | `Analyze dataset usage`, `Analyze dataset retention`, `Manage dataset retention` | Adobe Experience Platform | 「Web イベントデータセットはどの程度積極的に使用されていますか？」 <br> 「このデータセットに60日間の保持期間を設定した場合、どのような影響があるでしょうか？」 |

## サンドボックスツール

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [ サンドボックス間でオブジェクトを移動](/help/chat/use-cases/sandbox-tooling/sandbox-tooling.md) | 依存関係を自動解決し、スキーマ、オーディエンス、その他のオブジェクト設定をサンドボックス間でシームレスに移行できます | `sandbox-tooling-workflow` | Adobe Experience Platform | 「スキーマ Luma Loyalty Members Platinumを現在のサンドボックスから実稼動サンドボックスに移動」 <br> 「米国ゴールドロイヤルティメンバーのオーディエンスをステージに昇格させる」 |

## 顧客アラート

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| アラート購読の管理 | 自然言語の会話を通じて、アラート購読を表示および管理します。 | `alerts-subscribe` | Adobe Experience Platform | 「どのアラートを購読していますか？」 <br><br> 「このアラートを購読してください」 <br><br> 「このアラートの購読を解除してください」 |
| アラートアクティビティのレビュー | 指定した期間の現在のアラートステータスと過去のアラートアクティビティを確認します。 | `alerts-list` | Adobe Experience Platform | 「過去24時間に何が発生しましたか？」 <br><br> 「過去24時間にトリガーされたアラートは何ですか？」 <br><br> 「過去7日間のアクティブなアラートを表示します。」 |
| 繰り返し発生するアラートパターンの特定 | アラート履歴を分析して、頻繁にトリガーされるアラートのタイプと運用傾向を特定します。 | `alerts-list` | Adobe Experience Platform | 「トリガーされるアラートタイプの上位3つを表示してください」 <br><br> 「今月に最も頻繁に発生したアラートタイプはどれですか？」 <br><br> 「過去7日間にどのようなアラートパターンが見られますか？」 |
| 優先度の高い課題に注力する | アラートのアクティビティを重大度でフィルタリングし、調査活動の優先順位を決定できます。 | `alerts-list` | Adobe Experience Platform | 「重要度の高いアラートのみを表示します。」 <br><br> 「今週トリガーされた重要なアラートはどれですか？」 <br><br> 「過去30日間の重要なアラートを表示します。」 |
| アラートの影響半径を把握 | アラートの影響を最も受けるオブジェクトを特定し、調査を開始する場所を決定します。 | `alerts-list` | Adobe Experience Platform | 「影響を受ける上位5つのオブジェクトは何ですか？」 <br><br> 「最も重大度の高いアラートに関連付けられているオブジェクトはどれですか？」 |
| 影響を受けるオブジェクトへのアラートタイプの接続 | アラートタイプと影響を受けるリソースの関係を分析する。 | `alerts-list` | Adobe Experience Platform | 「最も頻繁にこのデータセットに影響を与えるアラートタイプはどれですか？」 <br><br> 「アラートタイプと影響を受けるオブジェクトの関係を表示します」 <br><br> 「最も影響を受けるオブジェクトに最も影響を与えるアラートタイプはどれですか？」 |
| 自分のアラートに集中 | 購読し、監視を担当するアラートを分析します。 | `alerts-list` | Adobe Experience Platform | 「購読している重要度の高いアラートを表示します。」 <br><br> 「今週トリガーされたアラートのアラートは？」 <br><br> 「購読しているアラートに注意が必要ですか？」 |

## ワークフローとプランニング

| ワークフロー | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| プランニングワークスペースの管理 | Workfront Planningのワークスペース、セクション、レコードタイプ、フィールドを構築および進化させて、プログラムを整理し、作業を追跡できます | `manage-workfront-planning`, `wf-planning-solution-architect` | Workfront Planning | 「MKG Hubというワークスペースを作成し、地域ごとにプログラムを追跡するためのレコードタイプを設定する」 <br> 「チャネルと地域をまたいでMKG プログラムを追跡するために必要なレコードタイプと関係を設定する」 |
| プランニングレコードの管理 | ワークスペース内でプランニングレコード（キャンペーン、ブリーフ）とそのフィールド値を作成および更新します | `manage-workfront-planning` | Workfront Planning | 「目標、ターゲットオーディエンス、およびキーメッセージを使用して、秋のブランド立ち上げキャンペーンの概要を作成する」 <br> 「予算とプライマリチャネルを使用して秋のブランド立ち上げ概要を更新する」 |
| プロジェクトの作成と管理 | スピンアップとプロジェクトの構成：テンプレートの適用、優先順位と予算の設定、タスクの順序付け、フェーズと依存関係の追加、人物や役割の割り当て | `manage-workfront-workflow` | Workfront Workflow | 「Spring キャンペーンを作成し、20万ドルの予算で優先度を高く設定し、タスクを並べ替える」 <br> 「プロジェクト テンプレート [から[ プロジェクト名]という名前のWorkfront プロジェクト計画を作成する」 <br> 「秋のローンチのプロジェクト計画を作成する：Social Campaignとコンセプト、デザイン、コピー、レビューのタスク」 <br> 「新しいメールマーケティングタスクを追加してRachel Smithに割する」] |
| レビューと承認を迅速化 | 多段階の承認の設定、承認テンプレートの適用、承認者の追加と削除、リマインダーの送信、一括更新をおこないます | `manage-workfront-workflow` | Workfront Workflow | 「多段階の承認（コピー、デザイン、法務）を作成し、承認していない人にリマインドする」 <br> 「開いているすべての承認からChris Smithを削除し、Jane Francisに置き換える」 |
| タスクと作業ステータスの更新 | タスクの完了をマークし、完了率を更新して、作業を終了します | `manage-workfront-workflow` | Workfront Workflow | 「秋の起動時に「キーアートの作成」タスクを完了としてマーク」 <br> 「秋の起動時のコピータスクを100%で閉じる」 |
| 作業のインサイトの獲得 | 探索的な質問をすることで、リスクのある作業、未割り当てのタスク、未解決のイシュー、プロジェクトをまたいだステータスなどを見つけることができます | `query-workfront` | Workfront Workflow | 「誰にも割り当てられていない現在のプロジェクトで、今週中に期限が切れる不完全なタスクを検索する」 <br> 「現在のプロジェクトに含まれている未解決の問題の数は？」 |
| プロジェクトとタスクの概要 | プロジェクト、タスク、イシュー、割り当てのリスト、テーブル、カウントを取得する | `query-workfront` | Workfront Workflow | 「プロジェクト名、タスクの期日、割り当てられたユーザーを含む、開始準備が整ったタスクのテーブルを表示する」 <br> 「ユーザー名]に割り当てられたすべてのタスクを取得する」[ |
| 承認とポートフォリオのステータスを追跡 | 承認のステータスを確認し、ポートフォリオごとに不完全な作業をロールアップします | `query-workfront` | Workfront Workflow | 「自分の承認のステータスを表示する」 <br> 「不完全な問題を含むテーブルを表示します。これは、[Portfolio name] ポートフォリオの一部です」 |
