# git / githubを学ぼう!!

## 学習前に

- **VScodeに入れておくと便利なもの**
[git-graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)

- PDFにイメージしやすいように図が載ってあります

- :rotating_light:*ここでは基本を押さえるだけで、margeは取り扱いません*

- :rotating_light:*分かりやすくするために、正式な名称と異なているかも。。。*

## git 設定
- usernameの設定
```bash
git config --global user.name 'githubのusername'
```

- emailの設定
```bash
git config --global user.email 'githubに登録してあるemail'
```

- 確認
```bash
git config user.name
```
```bash
git config user.email
```

## 基本1
1-1. githubでリポジトリを作成する

1-2. githubで作成したリポジトリを取得してくる
```bash
git clone -o <リモートリポジトリ名を指名(デフォルトはorigin)> <リポジトリのURL>
```

1-3. **取得してきたフォルダに移動する**
```bash
cd <cloneしてきたフォルダのパス> 
```

1-4. リモートリポジトリを確認
```bash
git remote -v
```

1-5. 作業フォルダに変更を加える

1-6. ステージングエリアに変更を教える

 ```bash
git add -A 
```

1-7. ステージングエリアに変更点を確定させる

```bash
git commit -m 'コメント'
```

1-8. ステージングエリアに挙げたものをgithubにあげる

```bash
git push <リモート名> <ブランチ名>
```

＊リモート名の確認方法
```bash
git remote -v
```
＊ブランチ名の確認方法
```bash
git branch --contains
```

> [!IMPORTANT]
> ### 基本1でpushしたgithubのリポジトリに誰が変更を加えた時 -> githubのリポジトリと情報を一致させる

> [!CAUTION]
> もし、githubのリポジトリに誰が変更を加えたまま、一致させないと...**競合が発生**してしまう <- めっちゃ直すのだるいから回避しよう!

2-1. **cloneしてきたフォルダに移動する**
```bash
cd <cloneしてきたフォルダのパス> 
```

2-2. リモートリポジトリを確認
```bash
git remote -v
```

2-3. **前にcloneしてきたフォルダに移動**し、githubのリポジトリの情報と一致させる
```bash
git pull
```

2-4. 以降は基本の1-5〜と一緒

