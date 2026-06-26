# 03.conflict

Tips

> コンフリクトとは？  
> ファイルの変更履歴が競合していること  
> つまりコンフリクトを起こすには, 同じファイルの同じ箇所を同時に変更する必要がある

## 03.01

mainブランチに戻り, そこからgit-conflict-practiceブランチを切って移動してください.  
そこで先ほど作業したブランチ(git-practice)をマージすることでコンフリクトが発生するようなプログラムを書いコミットしてください.  
つまりgit-conflict-practiceブランチに、git-practiceで変更した箇所に別の変更を加える。
例：

### git-practiceブランチ

hello.py

```python
print("Hello World!")
```

### git-conflict-practiceブランチ

```python
print("Hello World!!!!!!!!")
```

その後マージを行いコンフリクトが発生することを確認してください.
こんな感じで表示できればOK.

<img width="551" alt="スクリーンショット 2023-04-20 16 10 57" src="https://user-images.githubusercontent.com/106364533/233288283-1be79d00-cad5-4ae3-9960-92dc0f884273.png">

Tips

> マージとは？  
> 2つのブランチの変更履歴を統合すること  
> これを使うことで他者の開発したプログラムを自分のプログラムに取り入れることができる

## 03.02

コンフリクトを解消してください.どのように解消するかはお任せします.  
以下のようにマージコミットを表示できればOK.

<img width="948" alt="スクリーンショット 2023-04-20 16 31 09" src="https://user-images.githubusercontent.com/106364533/233293168-bdd8283e-7169-41cb-afb9-dfc22c1fb701.png">
