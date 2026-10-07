---
title: Coworker プロジェクトでの実装チェックリストの生成
description: Coworker Projectsが、実装ガイド計画から事前入力された実装チェックリストを生成する方法と、割り当てて追跡できる手順について説明します。
hold: true
source-git-commit: 2bf31c1348054a16ba7e7c0c26c0ff913634aa27
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%
---

# Coworker Projectsを使用した実装チェックリストの生成

Adobe CX Enterprise Coworkerでは、Coworker プロジェクトで実装チェックリストプロジェクトを生成できます。このプロジェクトには、Customer Journey Analyticsの実装ガイド計画、Adobe AnalyticsからCustomer Journey Analyticsへのアップグレード、Content Analytics（ACA）、Marketing Campaign Analytics（MCA）、またはStreaming Mediaの順序付き手順が事前に入力されています。 Coworkerは、技術的に可能な限り多くのステップを自動化または支援するため、実装を進めるための追跡可能な単一の場所を用意します。

導入を主導している場合、技術的なステップを実行している場合、または進捗状況を可視化する必要がある場合は、このチェックリストを使用して、同僚を離れることなく、作業の割り当て、ステータスの追跡、チームとの共同作業を行うことができます。

>[!NOTE]
>
>次の点に留意してください。
>
>* この機能は、カスタム実装またはアップグレード手順（[Coworker](./implementation-guide.md)を使用した実装の計画を参照）、実装（このチェックリスト）、検証（例：[Adobe AnalyticsからCustomer Journey Analyticsへのアップグレードの検証](./data-validation-aa-cja.md)または[Streaming Mediaの実装の検証](./streaming-media-validation.md)）という、より大規模でオプションのワークフローの一部です。 3つの段階すべてを実施する必要はありませんが、このチェックリストを作成するには、実装ガイドの包括的な計画が必要です。
>* Coworkerが自動的に実行または支援するステップには、信頼性または検証信号が含まれます。 これらのステップを完了する前に確認する – 共同作業者は、自動化された結果を検証済みの事実として提示しません。

このチェックリストを使用して、以下を行います。

* プランを手動で組み立てる代わりに、製品パスの順序付けされた事前入力された一連のステップを使用して、実装または移行を開始します。

* 実装リードに直接尋ねることなく、ブロックされている点や次に何が起こるかなど、実装中のステータスを確認できます。

* 単一の直線ではなく、複数のプラットフォームまたは複数の地域にステップを並行または段階的に実行する実装を計画します。

* Adobe AnalyticsとCustomer Journey Analyticsの設定の間で検証チェックを実行するなど、可能な限り直接ステップを実行できます。

* チームが先に進む前に承認が必要なステップについて、承認ゲートを導入します。


## 始める前に

<!-- FLAG: Open question — release note confirms a "predefined playbook" transforms the guide plan into a Coworker Project, but it's unconfirmed whether Coworker runs that playbook automatically or the user has to trigger/follow it manually. Written below as if Coworker does it automatically; verify before publishing. Exact UI mechanics also unconfirmed since Coworker Projects platform documentation doesn't exist yet. -->

### 必要な情報

実装チェックリストを生成するには、次のものが必要です。

* 製品パスに合わせて完成した実装ガイドの会話。 [同僚との実装計画](./implementation-guide.md)を参照してください。 Coworkerは、この計画を自動的にCoworker Projectに変換し、事前に定義されたプレイブックを使用します。自分で何かを書き出す必要はありません。

* 組織内の同僚プロジェクトへのアクセス。

### 制限事項

この機能を使用する前に、次の点に注意してください。

* **ガイドのコンテンツを所有していません**：この機能は、実装ガイドのスキルからプランを消費します。 Aiは基礎となるコンテンツを作成したり、維持したりしません。
* **同期動作はまだ完全に定義されていません**: チェックリストは、実装ガイド計画の更新と同期を維持することを目的としていますが、正確な同期メカニズムはまだ定義されています。 実装が長いタイムラインにまたがる場合は、ガイドプランの更新を手動で確認します。
* **Coworker Projects**&#x200B;が必要です。この機能は、組織で利用可能なCoworker Projects プラットフォームによって異なります。

## チェックリストを生成

<!-- FLAG: Best guess, not confirmed by source docs. Coworker Projects UI isn't documented in this repo yet — verify exact navigation and UI labels once available. -->

1. Coworkerにログインします。

1. ナビゲーションパネルで「[!UICONTROL **プロジェクト**]」を選択します。

1. [!UICONTROL **新しいプロジェクト**]&#x200B;を選択し、実装ガイド計画に一致する定義済みプレイブックを選択します。

   Coworkerは、パスの順序付きステップがあらかじめ入力されたプロジェクトにプランを変換します。

## 結果を見る

Coworkerは、自分とチームが作業できるCoworker プロジェクトとして、実装チェックリストを生成します。

**プロジェクトビュー**

プロジェクトは、計画から順序付けされた実装手順をグループ化します。 各ステップでは、次のことができます。

* 所有者の割り当て
* 進捗状況や完了などの更新ステータス
* ステップに「該当しない」マークを付けるか、実装に適用されない場合はスキップします
* コメントを追加し、チームと共同作業を行う
* 承認が必要なステップについては、ステップが完了したと見なされる前に承認を必要とします

**自動化および支援された手順**

Coworkerは、技術的に実現可能な場合、Adobe AnalyticsやCustomer Journey Analyticsからの設定やステータスデータの表示など、ステップを直接実行または支援します。 これらのステップには、前述のように、信頼性または検証シグナルが含まれます。

**書き出し**

チェックリストまたは概要レベルの進捗状況をJira、Workfront、Excelにエクスポートして、既存のプロジェクト管理ワークフローに組み込むことができます。

**複数のチェックリスト**

複数のレポートスイート、地域、ブランドなど、複数の同時実装を管理している場合は、1つに制限されるのではなく、複数の実装チェックリストプロジェクトを管理できます。
