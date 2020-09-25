# ネコメシの Git 運用方針について

- [コミットメッセージの書き方](##コミットメッセージの書き方)
- Pull Request の書き方
- Issue の書き方

## コミットメッセージの書き方

### 良いコミットメッセージとは？

- コミットログが見やすいこと
- チーム開発の理解の助けになること
  - なぜそのようなコードを書いているかわかること
- レビューがしやすいこと
- コミットメッセージは個人の作業ログではなく、製品の変更履歴であるべき

### フォーマット

```
[Prefix]: [Subject]

[Body]

[Issue ID]
```

#### Prefix

プレフィックスの種別については[AngularJS](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#type)の開発ルールを参照

| 種別     | 用途                                                             |
| -------- | ---------------------------------------------------------------- |
| feat     | 機能開発                                                         |
| fix      | バグ修正                                                         |
| docs     | ドキュメントの変更。README など                                  |
| style    | 機能に影響のないコードの整形（スペース、インデント、セミコロン等 |
| refactor | 機能の変更のないコードの修正                                     |
| perf     | パフォーマンスを改善するコードの修正                             |
| test     | テストコード関連                                                 |
| chore    | 製品に関係のないビルドタスクやジェネレートツール関連             |

#### Subject

何を変更したのかを短い文章に。
変更内容を端的に表せると Good

- feat: TOP ページ作成
- fix: コンテキストメニューの表示座標のズレを修正
- chore: 画像の圧縮タスクを追加

#### Body

なぜ変更したのかを文章に。

- 変更が必要だった理由
- どうしてそのように変更したのか（修正方針
- どのように（コードの実装や動作）は重要ではない
- タイトルで完結してしまったら書かなくて良い

⭕️GOOD

```
fix: コンテキストメニューの表示座標のズレを修正

表示する親要素に包含ブロックを指定していなかったため、モーダル内ではズレが発生したので、テーブルコンポーネントを包含ブロックに修正
```

❌BAD

```
fix: コンテキストメニューの表示座標のズレを修正

position: relative;を指定
```

#### Issue

関連する Issue ID があれば記載

```
fix: コンテキストメニューの表示座標のズレを修正

表示する親要素に包含ブロックを指定していなかったため、モーダル内ではズレが発生したので、テーブルコンポーネントを包含ブロックに修正

Issue #48
```
