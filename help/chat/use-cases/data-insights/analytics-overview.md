---
title: Adobe Customer Journey Analyticsのデータを分析する（チャット）
description: Adobe CX Enterprise Coworker Chatを使用してAdobe Customer Journey Analyticsのデータを分析し、ファネルを構築して、カスタマージャーニーのどの段階で顧客が脱落しているのかを把握する方法を紹介します。
hold: true
product_v2:
  internal-label: CX Enterprise Coworker
feature_v2:
  internal-label: CX Enterprise Coworker
source-git-commit: 12ee914ed944c82694b9373f611e19cf040e2229
workflow-type: tm+mt
source-wordcount: '2332'
ht-degree: 0%
---

Adobe CX Enterprise Coworker Chatなら、自然言語を使ってAdobe Adobeのプロダクトタスクを自動化し、柔軟なプランニング、カスタマイズ可能なスキル、インテリジェントな実行によってアイデアをすばやくアクションに転換できます。 Coworkerの一般的な詳細については、[CX Enterprise Coworkerの概要](/help/home.md)を参照してください。

## 同僚とのチャットによるデータ分析

Coworker Chatは、以前はAnalysis Workspaceでのみ可能だった高度なデータ分析を実行できます。 Coworker Chatは、Customer Journey AnalyticsのデータビューやAdobe Analyticsレポートスイートからデータにアクセスし、そのデータを探索して自然言語プロンプトへの回答を得ることができます。

Coworker Chatで作成したビジュアライゼーションは、いつでも手動で開くことができます。

## 同僚チャットで分析を開始

最初に、知りたいことを分かりやすい言葉で説明しましょう。 Coworker Chatは分析計画を立て、データビューやレポートスイートのクエリを行い、ビジュアライゼーションや概要を作成します。

以下のユースケースは、その一例です。 アクセスする権限があるデータがあれば

### 主なユースケース

<!-- The following cards link to each of the stand-alone articles in this folder -->

<!--
CARDS

* https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/analytics-chat
  {title = Analyze Customer Journey Analytics and Adobe Analytics data}
  {description = Answers natural-language questions about your data views or report suites, builds funnels and other visualizations, and finds where customers drop off. You can open any visualization in Analysis Workspace for further analysis.}
  {cta = Read}
  {image = ../../assets/coworker-funnel-response-card.png}

* https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/root-cause-analysis
  {title = Explore trends and root causes}
  {description = Identifies trends in your Customer Journey Analytics and Adobe Analytics data and the factors that drive changes in performance, without manual queries.}
  {cta = Read}
  {image = ../../assets/data-validation-aa-cja/trend-line-card.png}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze Customer Journey Analytics and Adobe Analytics data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/analytics-chat" title="Customer Journey AnalyticsとAdobe Analyticsのデータを分析する">
                        <img class="is-bordered-r-small" src="../../assets/coworker-funnel-response-card.png" alt="Customer Journey AnalyticsとAdobe Analyticsのデータを分析する"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/analytics-chat" title="Customer Journey AnalyticsとAdobe Analyticsのデータを分析する">Customer Journey AnalyticsとAdobe Analytics データの分析</a>
                    </p>
                    <p class="is-size-6">データビューやレポートスイートに関する自然言語の質問に答え、ファネルやその他のビジュアライゼーションを構築し、顧客が離脱する原因を見つけ出します。 Analysis Workspaceで任意のビジュアライゼーションを開いて、さらに詳しく分析できます。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/analytics-chat" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">読み取り</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Explore trends and root causes">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/root-cause-analysis" title="トレンドと根本原因を探る">
                        <img class="is-bordered-r-small" src="../../assets/data-validation-aa-cja/trend-line-card.png" alt="トレンドと根本原因を探る"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/root-cause-analysis" title="トレンドと根本原因を探る"> トレンドと根本原因を探る</a>
                    </p>
                    <p class="is-size-6">Customer Journey AnalyticsとAdobe Analyticsのデータの傾向と、パフォーマンスの変化を促す要因を手動でのクエリなしで特定します。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/root-cause-analysis" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">読み取り</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

<!--
CARDS

* https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/implementation-guide
  {title = Plan your implementation}
  {description = Creates a personalized, step-by-step plan for implementing Customer Journey Analytics, upgrading from Adobe Analytics, or setting up Content Analytics, Marketing Campaign Analytics, or Streaming Media collection on the Edge. Plans include details such as owners, effort estimates, dependencies, and validation steps.}
  {cta = Read}
  {image = ../../assets/ui-guide-6.png}

* https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/intelligent-checklist
  {title = Generate an implementation checklist}
  {description = Turns your Customer Journey Analytics implementation plan into a checklist in Coworker Projects, where your team can assign steps, track status, and add approval gates.}
  {cta = Read}
  {image = ../../assets/data-validation-aa-cja/date-detail.png}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Plan your implementation">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/implementation-guide" title="Adobe Experience Manager Sites導入計画">
                        <img class="is-bordered-r-small" src="../../assets/ui-guide-6.png" alt="Adobe Experience Manager Sites導入計画"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/implementation-guide" title="Adobe Experience Manager Sites導入計画">実装の計画</a>
                    </p>
                    <p class="is-size-6">Customer Journey Analyticsの実装、Adobe Analyticsからのアップグレード、EdgeでのContent Analytics、Marketing Campaign Analytics、ストリーミングメディアコレクションの設定などについて、パーソナライズされたステップバイステップの計画を作成します。 計画には、所有者、労力の見積もり、依存関係、検証手順などの詳細が含まれます。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/implementation-guide" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">読み取り</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Generate an implementation checklist">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/intelligent-checklist" title="実装チェックリストの生成">
                        <img class="is-bordered-r-small" src="../../assets/data-validation-aa-cja/date-detail.png" alt="実装チェックリストの生成"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/intelligent-checklist" title="実装チェックリストの生成">実装チェックリストを生成</a>
                    </p>
                    <p class="is-size-6">Customer Journey Analyticsの導入計画をCoworker Projectsのチェックリストに変換し、手順の割り当て、ステータスの追跡、承認ゲートの追加を可能にします。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/intelligent-checklist" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">読み取り</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

<!--
CARDS

* https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/data-validation-aa-cja
  {title = Validate data when upgrading from Adobe Analytics to Customer Journey Analytics}
  {description = Compares dimensions, metrics, and trends between your Adobe Analytics report suites and Customer Journey Analytics data views, then recommends fixes to support your upgrade.}
  {cta = Read}
  {image = ../../assets/data-validation-aa-cja/trend-bar-card.png}

* https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/streaming-media-validation
  {title = Validate your Streaming Media implementation}
  {description = Checks your datastream, schema, dataset, data view, and session data to confirm that streaming media tracking is configured and collecting data correctly.}
  {cta = Read}
  {image = ../../assets/ui-guide-8.png}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Validate data when upgrading from Adobe Analytics to Customer Journey Analytics">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/data-validation-aa-cja" title="Adobe AnalyticsからCustomer Journey Analyticsにアップグレードする際のデータの検証">
                        <img class="is-bordered-r-small" src="../../assets/data-validation-aa-cja/trend-bar-card.png" alt="Adobe AnalyticsからCustomer Journey Analyticsにアップグレードする際のデータの検証"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/data-validation-aa-cja" title="Adobe AnalyticsからCustomer Journey Analyticsにアップグレードする際のデータの検証">Adobe AnalyticsからCustomer Journey Analyticsへのアップグレード時にデータを検証</a>
                    </p>
                    <p class="is-size-6">Adobe Analytics レポートスイートとCustomer Journey Analytics データビュー間のディメンション、指標、傾向を比較し、アップグレードをサポートするための修正を推奨します。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/data-validation-aa-cja" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">読み取り</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Validate your Streaming Media implementation">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/streaming-media-validation" title="ストリーミングメディア実装の検証">
                        <img class="is-bordered-r-small" src="../../assets/ui-guide-8.png" alt="ストリーミングメディア実装の検証"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/streaming-media-validation" title="ストリーミングメディア実装の検証"> ストリーミングメディア実装の検証</a>
                    </p>
                    <p class="is-size-6">データストリーム、スキーマ、データセット、データビュー、セッションデータを確認して、ストリーミングメディアトラッキングが設定され、データが正しく収集されていることを確認します。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/streaming-media-validation" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">読み取り</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

<!--
CARDS

* https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/validate-dataset-quality-for-cja
  {title = Validate dataset quality for Customer Journey Analytics}
  {description = Identifies the datasets that feed your Customer Journey Analytics reporting, then checks schemas, identity quality, and field quality so you can resolve issues before you build dashboards.}
  {cta = Read}
  {image = ../../assets/data-validation-aep/dataset-validation.png}

* https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/data-validation-aep
  {title = Validate data after ingestion into Experience Platform}
  {description = Runs statistical and semantic checks on Experience Platform datasets and fields to find data quality issues, such as invalid values or mapping problems.}
  {cta = Read}
  {image = ../../assets/data-validation-aep/null-values.png}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Validate dataset quality for Customer Journey Analytics">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/validate-dataset-quality-for-cja" title="Customer Journey Analyticsのデータセット品質の検証">
                        <img class="is-bordered-r-small" src="../../assets/data-validation-aep/dataset-validation.png" alt="Customer Journey Analyticsのデータセット品質の検証"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/validate-dataset-quality-for-cja" title="Customer Journey Analyticsのデータセット品質の検証">Customer Journey Analyticsのデータセット品質を検証</a>
                    </p>
                    <p class="is-size-6">Customer Journey Analyticsレポートに使用するデータセットを特定し、スキーマ、ID品質、フィールド品質をチェックすることで、ダッシュボードを構築する前に問題を解決できます。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/validate-dataset-quality-for-cja" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">読み取り</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Validate data after ingestion into Experience Platform">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/data-validation-aep" title="Experience Platformに取り込んだ後のデータの検証">
                        <img class="is-bordered-r-small" src="../../assets/data-validation-aep/null-values.png" alt="Experience Platformに取り込んだ後のデータの検証"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/data-validation-aep" title="Experience Platformに取り込んだ後のデータの検証">Experience Platformに取り込んだ後のデータの検証</a>
                    </p>
                    <p class="is-size-6">Experience Platformのデータセットとフィールドに対して統計チェックとセマンティックチェックを実行し、無効な値やマッピングの問題などのデータ品質の問題を見つけます。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/data-validation-aep" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">読み取り</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

これらのユースケース（使用するスキルやサンプルプロンプトなど）について詳しくは、[ データインサイトのユースケース ](/help/chat/use-cases/overview.md#data-insights)を参照してください。

### 基本を学ぶ

Coworker Chatでは、次のような機能も利用できます。

* **パフォーマンスを比較**: チャネル、期間、またはセグメント間で指標を並べて比較します。
* **キャンペーンのパフォーマンスを測定**：特定の期間におけるキャンペーン、チャネル、web プロパティのパフォーマンスを確認します。
* **ファネルの分析**: マルチステップのコンバージョンファネルを順を追って説明し、各ステージでの離脱を確認します。
* **予測指標**：売上目標の達成に向けて順調に進んでいるかどうかなど、過去のCustomer Journey AnalyticsまたはAdobe Analytics データから将来の指標の値を予測します。
* **エグゼクティブ サマリーとKPI ダイジェストを作成**：関係者に対応したパフォーマンス サマリー、レコメンデーション、スライド デッキの概要を作成します。
* **運用上の傾向と原因を分析**: オーディエンス、データセット、ジャーニーに関する過去の時系列データをクエリし、変更の原因を特定します。
* **カスタム Customer Journey Analytics スキルを作成**：繰り返し使用する分析を、セッション間で保持される再利用可能なスキルに変換します。

<!--
CARDS

* https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/analytics-chat
  {title = Analyze data with Coworker Chat}
  {description = Ask questions in natural language to build funnels, create visualizations, and find where customers drop off in the journey.}
  {cta = Read}
  {image = ../../assets/coworker-funnel-response-card.png}

* https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/root-cause-analysis
  {title = Explore trends and root causes}
  {description = Investigate changes in your Customer Journey Analytics data and uncover what drives them, without writing manual queries.}
  {cta = Read}
  {image = ../../assets/data-validation-aa-cja/trend-line-card.png}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze data with Coworker Chat">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/analytics-chat" title="Coworker Chatでデータを分析">
                        <img class="is-bordered-r-small" src="../../assets/coworker-funnel-response-card.png" alt="Coworker Chatでデータを分析"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/analytics-chat" title="Coworker Chatでデータを分析">同僚チャットでデータを分析</a>
                    </p>
                    <p class="is-size-6">自然言語で質問することで、ファネルを構築し、ビジュアライゼーションを作成し、カスタマージャーニーのどの段階で顧客が脱落しているのかを把握できます。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/analytics-chat" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">読み取り</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Explore trends and root causes">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/root-cause-analysis" title="トレンドと根本原因を探る">
                        <img class="is-bordered-r-small" src="../../assets/data-validation-aa-cja/trend-line-card.png" alt="トレンドと根本原因を探る"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/root-cause-analysis" title="トレンドと根本原因を探る"> トレンドと根本原因を探る</a>
                    </p>
                    <p class="is-size-6">Customer Journey Analyticsデータの変更点を調査し、手作業でクエリを記述することなく、その要因を明らかにします。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/root-cause-analysis" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">読み取り</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

<!--
CARDS

* https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/validate-dataset-quality-for-cja
  {title = Validate Customer Journey Analytics data}
  {description = Check dataset quality with the data validation skill and resolve issues before you build dashboards.}
  {cta = Read}
  {image = ../../assets/data-validation-aep/dataset-validation.png}

* https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/data-validation-aa-cja
  {title = Validate data during your upgrade}
  {description = Compare Adobe Analytics and Customer Journey Analytics data to confirm that your upgrade is on track.}
  {cta = Read}
  {image = ../../assets/data-validation-aa-cja/trend-bar-card.png}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Validate Customer Journey Analytics data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/validate-dataset-quality-for-cja" title="Customer Journey Analytics データの検証">
                        <img class="is-bordered-r-small" src="../../assets/data-validation-aep/dataset-validation.png" alt="Customer Journey Analytics データの検証"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/validate-dataset-quality-for-cja" title="Customer Journey Analytics データの検証">Customer Journey Analytics データの検証</a>
                    </p>
                    <p class="is-size-6">ダッシュボードを構築する前に、データ検証スキルでデータセットの品質を確認し、問題を解決します。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/validate-dataset-quality-for-cja" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">読み取り</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Validate data during your upgrade">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/data-validation-aa-cja" title="アップグレード中にデータを検証する">
                        <img class="is-bordered-r-small" src="../../assets/data-validation-aa-cja/trend-bar-card.png" alt="アップグレード中にデータを検証する"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/data-validation-aa-cja" title="アップグレード中にデータを検証する"> アップグレード中にデータを検証</a>
                    </p>
                    <p class="is-size-6">Adobe AnalyticsとCustomer Journey Analyticsのデータを比較し、アップグレードが順調に進んでいることを確認します。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/data-insights/data-validation-aa-cja" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">読み取り</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->



## 主要なユースケースのテーブルレイアウト

<!-- The following table are links to each of the stand-alone articles in this folder -->

| ユースケース | 説明 |
| --- | --- |
| [Customer Journey AnalyticsとAdobe Analytics データの分析](/help/chat/use-cases/data-insights/analytics-chat.md) | データビューやレポートスイートに関する自然言語の質問に答え、ファネルやその他のビジュアライゼーションを構築し、顧客が離脱する原因を見つけ出します。 Analysis Workspaceで任意のビジュアライゼーションを開いて、さらに詳しく分析できます。 |
| [ トレンドと根本原因を探る](/help/chat/use-cases/data-insights/root-cause-analysis.md) | Customer Journey AnalyticsとAdobe Analyticsのデータの傾向と、パフォーマンスの変化を促す要因を手動でのクエリなしで特定します。 |
| [実装の計画](/help/chat/use-cases/data-insights/implementation-guide.md) | Customer Journey Analyticsの実装、Adobe Analyticsからのアップグレード、EdgeでのContent Analytics、Marketing Campaign Analytics、ストリーミングメディアコレクションの設定などについて、パーソナライズされたステップバイステップの計画を作成します。 計画には、所有者、労力の見積もり、依存関係、検証手順などの詳細が含まれます。 |
| [実装チェックリストを生成](/help/chat/use-cases/data-insights/intelligent-checklist.md) | Customer Journey Analyticsの導入計画をCoworker Projectsのチェックリストに変換し、手順の割り当て、ステータスの追跡、承認ゲートの追加を可能にします。 |
| [Adobe AnalyticsからCustomer Journey Analyticsへのアップグレード時にデータを検証](/help/chat/use-cases/data-insights/data-validation-aa-cja.md) | Adobe Analytics レポートスイートとCustomer Journey Analytics データビュー間のディメンション、指標、傾向を比較し、アップグレードをサポートするための修正を推奨します。 |
| [ ストリーミングメディア実装の検証](/help/chat/use-cases/data-insights/streaming-media-validation.md) | データストリーム、スキーマ、データセット、データビュー、セッションデータを確認して、ストリーミングメディアトラッキングが設定され、データが正しく収集されていることを確認します。 |
| [Customer Journey Analyticsのデータセット品質を検証](/help/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md) | Customer Journey Analyticsレポートに使用するデータセットを特定し、スキーマ、ID品質、フィールド品質をチェックすることで、ダッシュボードを構築する前に問題を解決できます。 |
| [Experience Platformに取り込んだ後のデータの検証](/help/chat/use-cases/data-insights/data-validation-aep.md) | Experience Platformのデータセットとフィールドに対して統計チェックとセマンティックチェックを実行し、無効な値やマッピングの問題などのデータ品質の問題を見つけます。 |

これらのユースケース（使用するスキルやサンプルプロンプトなど）について詳しくは、[ データインサイトのユースケース ](/help/chat/use-cases/overview.md#data-insights)を参照してください。

