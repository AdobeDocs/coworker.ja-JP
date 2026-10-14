---
source-git-commit: e5bf2a0a2ee55513b32442f70d01dc5825ac9d6a
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%
---
# CX Enterprise Coworker ドキュメント

Adobe CX Enterprise Coworker用Source ドキュメントセット。

## 公開設定

`.github/workflows/`の共有記事の検証とミラーリング ワークフローを使用します。
プルリクエストの検証ワークフローが実行され、`main`にプッシュされます。
`main`にプッシュすると、ミラーリングワークフローが実行されます。

Markdown ルールの上書きに`markdownlint_custom.json`を使用し、URL除外に`linkcheckexclude.json`を使用します。
`pipeline.opts` ファイルは、`cx-enterprise-ai.en`のリンクチェック設定に従っています。
`source,dest`列を使用して、URL リダイレクトを`redirects.csv`に追加します。
