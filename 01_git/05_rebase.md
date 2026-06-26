# 05.rebase

### ゴール

実際によく使うrebaseオプションを使えるようになる

## どういうときに使うのか

- コミット名を間違えてしまったとき
- コミットA に コミットB の変更内容をまとめたいとき
- コミットを削除したいとき

### rebase の使い方

今回はコミットIDを使用して rebase します。
以下のコマンドを使用してください。

```
git rebase -i <commit_id>
```

### 事前準備

1. 05_rebaseフォルダーを作成してください
2. 作成したフォルダー内に profile.txt を作成して 名前 を追加し `プロフィール` というコミットを作成してください。
3. 同じフォルダー内に以下のtxtファイルを作成し `rebaseオプション` というコミットを作成してください。  
   reword.txt  
   edit.txt  
   squash.txt  
   fixup.txt  
   drop.txt
4. 同じフォルダー内に helloWorld.txt ファイルを作成して `helloWorld` というコミットを作成してください。
   <img width="378" height="230" alt="スクリーンショット 2026-01-15 12 12 25" src="https://github.com/user-attachments/assets/98ac5f83-ed3f-44b7-a1ee-51ef3912ae80" />

## 05.01 fixup

1. 事前準備3 で作成したファイル名は rebase のオプション名になっています。
   それぞれのオプションで何ができるのかを調べ、ファイルに記述し `オプション説明` というコミットを作成してください。
2. fixup オプションを使用して、1で作成した コミット と 事前準備3 で作成した コミット をまとめてください。
   <img width="378" height="238" alt="スクリーンショット 2026-01-15 12 15 51" src="https://github.com/user-attachments/assets/9cd377a8-1f00-4beb-97f2-405869b1bf1a" />

## 05.02 drop

事前準備4 で作成した コミットを drop してください。  
<img width="371" height="156" alt="スクリーンショット 2026-01-15 12 16 52" src="https://github.com/user-attachments/assets/07a48d7f-d22b-483f-803a-94d62a01121e" />

## 05.03 edit

事前準備2 で作成したコミットに edit オプションを使い、profile.txt に好きな食べ物を追加して コミット してください。
<img width="515" height="189" alt="スクリーンショット 2026-01-15 12 31 58" src="https://github.com/user-attachments/assets/e0bf361b-acc7-43c9-90cf-1f58da97c1f9" />

## 05.04 reword

業務では追加されるコードを 他者 が確認する工程があります。
事前準備3で追加したコミット名では何をしたのかがわからないので reword オプションを使い何をしたのかがわかりやすいように変更してください。

> わかりやすいコミット名とは？  
> 何をしたのか が分かればいい  
> コミット名の先頭に、add や feat などをつけたり、〇〇した などをコミット名にするとわかりやすい。

## 05.05 squash

1. profile.txt に 趣味 を追加して `趣味の追加` というコミットを作成してください。
2. squash オプションを使い、1で追加した コミット と 事前準備2 で作成した コミットをまとめてください。  
   コミット名は 05.04 を参考にしてください。
