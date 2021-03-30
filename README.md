# LitElement TypeScript starter

このプロジェクトには、TypeScriptでLitElementを使用するサンプルコンポーネントが含まれています。

## Setup

依存関係をインストール:

```bash
npm i
```

## Build

このサンプルでは、​​TypeScriptコンパイラを使用して、最新のブラウザで実行されるJavaScriptを生成します。

ビルド:

```bash
npm run build
```

ファイルが変更されたときに再構築するビルド:

```bash
npm run build:watch
```

TypeScriptコンパイラとlit-analyzerは、どちらも非常に厳密に構成されています。 `tsconfig.json`を変更して、厳密さを緩和することをお勧めします。

## Testing

このサンプルでは、​​Karma、Chai、Mocha、およびopen-wcテストヘルパーをテストに使用します。詳細については、[open-wcテストのドキュメント](https://open-wc.org/testing/testing.html)を参照してください。

テスト実行:

```bash
npm test
```

## Dev Server

このサンプルでは、​​open-wcの[es-dev-server](https://github.com/open-wc/open-wc/tree/master/packages/es-dev-server)を使用して、追加のビルド手順なしでプロジェクトをプレビューします。 ES開発サーバーは、ブラウザーでサポートされていないノードスタイルの"bare"インポート指定子の解決を処理します。また、JavaScriptを自動的に変換し、古いブラウザーをサポートするためにポリフィルを追加します。

開発サーバーを実行:

```bash
npm run serve
```

`/dev/index.html`に開発HTMLファイルがあり、 http://localhost:8000 で表示できます。

## Editing

VS Codeを使用する場合は、[lit-plugin拡張機能](https://marketplace.visualstudio.com/items?itemName=runem.lit-plugin)を強くお勧めします。これにより、lit-htmlテンプレートで非常に便利な機能がいくつか有効になります。

  - Syntax highlighting
  - Type-checking
  - Code completion
  - Hover-over docs
  - Jump to definition
  - Linting
  - Quick Fixes

プロジェクトは、VS Codeユーザーがまだインストールしていない場合、lit-pluginを推奨するように設定されています。

## Linting

TypeScriptファイルのリンティングは、ESLintおよび[TypeScript ESLint](https://github.com/typescript-eslint/typescript-eslint)によって提供されます。さらに、[lit-analyzer](https://www.npmjs.com/package/lit-analyzer)は、lit-pluginと同じエンジンとルールでlit-htmlテンプレートのタイプチェックとリントを行うために使用されます。

これらのルールは、ほとんどの場合、各プロジェクトで推奨されるルールですが、LitElementの使用を容易にするためにオフになっているものもあります。推奨されるルールはかなり厳格なので、`.eslintrc.json`と`tsconfig.json`を編集してルールを緩和することをお勧めします。

lint実行:

```bash
npm run lint
```

## Formatting

[Prettier](https://prettier.io/)はコードのフォーマットに使用されます。これは、Polymer Projectのスタイルに従って事前構成されています。これは.`.prettierrc.json`で変更できます。

Prettierは、ファイルをコミットするときに実行するように構成されていませんが、これはHuskyおよびかなり迅速に追加できます。手順については、[prettier.io](https://prettier.io/)サイトを参照してください。

## Static Site

このプロジェクトには、11個の静的サイトジェネレーターで生成された単純なWebサイトと、`/docs-src`内のテンプレートとページが含まれています。サイトは`/docs`に生成され、GitHubページが[マスターブランチの`/docs`から](https://help.github.com/en/github/working-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)サイトを提供できるようにチェックインすることを目的としています。

サイトを有効にするには、GitHub設定に移動し、GitHub Pagesの"Source"設定を"master branch /docs folder"に変更します。

サイトをビルドして実行:

```bash
npm run docs
```

サイトをローカルで提供:

```bash
npm run docs:serve
```

実行(自動的に再構築):

```bash
npm run docs:watch
```

このサイトは通常 http://localhost:8000 で提供されます。

## Bundling and minification

このスタータープロジェクトには、バンドルやミニファイなどのビルド時の最適化は含まれていません。 コンポーネントを最適化されていないJavaScriptモジュールとして公開し、アプリケーションレベルでビルド時の最適化を実行することをお勧めします。 これにより、ビルドツールは、コードの重複排除、デッドコードの削除などを行うための最良の機会を得ることができます。

LitElementコンポーネントを含むアプリケーションプロジェクトのビルドについては、LitElementサイトでの[本番用のビルド](https://lit-element.polymer-project.org/guide/build)を参照してください。

## More information

詳細については、LitElementサイトの[Get started](https://lit-element.polymer-project.org/guide/start)を参照してください。
