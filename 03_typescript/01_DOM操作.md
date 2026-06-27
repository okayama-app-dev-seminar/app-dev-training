# 01.DOM操作（TypeScript）

01.01 が完了したら、このディレクトリのブラウザ表示で使った html と css ファイル、`index.ts` のみを PR で提出してください.

## この章の目標

- DOM 操作を理解する
- 基本的な TypeScript の型付けがわかる
- null チェックの必要性がわかる

## TypeScript の型の概念（要点）

TypeScript は「値の形（型）」をコードに明示することで、実行前に不一致を検出します
型は「この値は何を持ち、何ができるか」の契約として振る舞います

- プリミティブ型: `string`, `number`, `boolean`
- オブジェクト型: `type` / `interface` で形を定義
- ユニオン型: `string | null` のように複数の可能性を表現
- ジェネリクス: `Array<T>` や `Promise<T>` で「中身の型」を表現

## どうして型が大事なのか💡

- 早期発見: 実行前に「nullの可能性」「キーの誤り」などが分かる
- 変更に強い: データ構造が変わった時に影響範囲が型エラーで分かる
- 自己文書化: 「何を期待しているか」がコードから読み取れる
- 補完が強い: エディタの補完でミスが減る

## ルール📌

この課題では `any` と `as` を使わず、型で意図を表現してください

## 01.01

作った HTML の article body 部分の内容を `index.ts` から挿入できるようにしてください
以下のような感じで表示できれば OK です

<img width="1512" alt="スクリーンショット 2023-05-01 10 34 58" src="https://user-images.githubusercontent.com/106364533/235389509-616fc876-6787-428a-9453-0b9d14cd7f8c.png">

### ヒント💡

- DOM取得は `HTMLElement | null` になるため, nullチェックで型を絞り込む
- `querySelector` には適切なジェネリクスを指定する
  例: `document.querySelector<HTMLElement>('.article-body')`
- 挿入するデータの型を `type` または `interface` で定義する
  例: `type Article = { title: string; body: string }`
- 設計方法
  - HTML は構造を作る
  - CSS は見た目を整える
  - JavaScript (今回は TypeScript) はデータ取得や状態制御を担当する
