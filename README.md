# ZEN大学公開リポジトリ
## GitHubのSSH公開鍵を作成する（別アカウント用）
```
	# 1. 公開鍵の生成
	ssh-keygen -t ed25519 -C "xxx@example.com" -f ~/.ssh/example_ed25519
```
```
	# 2. 公開鍵をコピーする(クリップボード)
	pbcopy < ~/.ssh/example_ed25519.pub
```
```
	# 3. 接続テスト
	ssh -i ~/.ssh/example_ed25519 -T git@github.com
```
* Hi [github username]! You've successfully authenticated, but GitHub does not provide shell access.
と表示されたら、OK.
1. sshの鍵を生成する。（公開鍵のパスワード設定は任意だがセキュリティ考慮なら要設定。）
2. クリップボードにコピーされた公開鍵を任意のgithubアカウントに公開鍵を貼り付ける。(New SSH Key)
　　(https://github.com/settings/keys)
3. 接続テストをおこなう。
4. リポジトリを作り公開する。

--- 

## github pageを作成する
1. ディレクトリ（ローカル）：[username].github.comを作成する
2. リポジトリ（リポート）：[username].github.comを作成する
3. ローカルにコンテンツ生成、リポジトリにデプロイ。

### Jekyllを使う。
```
	brew install rbenv
	rbenv install <ruby version>
	gem install bundler jekyll
	jekyll new ungen-aygm.github.com
```

--- 

## GitHub Educationに申し込み手順
1. https://github.com/educationにアクセスし、[Join GitHub Education]に移動
2. 学校の役割（学生）を選択、学校名を入力し、Continueで次へ
3. 在籍している学生証などの写真を提出する。（学生証が一番良い）(1024×768 以上、100kb〜1MB以内の画像ファイル)
4. 申請結果を待つ。

---

