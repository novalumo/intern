# npm (Node Package Manager)

npm は Node Package Manager の略で、その名前の通りパッケージマネージャ。依存関係などを管理できる。

使用する前に、npm が使えるか以下のコマンドで確認する。バージョンが表示されていて、エラー等が出ていない場合は問題ない。

```bash
npm -v
```

また、npm に関してコマンドの使い方を知りたいときは、以下の方法で確認できる。

```bash
npm help コマンド名
```

## 基本的な使い方

### ローカル / グローバルインストール

npm にはローカルインストール（プロジェクト単位でインストール）、グローバルインストールの 2 種類がある。

```bash
# ローカルインストール
npm install jquery

# グローバルインストール
npm install -g typescript
```

グローバルインストールしたものに関しては、現在いる場所（ディレクトリ）に関係なく、インストールしたパッケージのコマンドを実行できる。

```bash
# npm install -g typescriptでTypeScriptをグローバルインストールした場合は以下のように実行できる
tsc index.ts
```

### インストールの種類

パッケージをインストールする際の種類は以下の通り。

- dependencies（`--saveは使用しても良いが不要`）
- devDependencies

主な違いは、_開発時に用いるか否か_ 。`devDependencies`としてインストールしたい場合は、`--save-dev`オプションを付けて`npm install`する。
