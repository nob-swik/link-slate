## HUGOでつくったサイトをGitHub Pagesのプロジェクトページで公開する手順
1. GitHubでリポジトリを作成しておく
2. HUGOのインストール
3. `$ hugo new site [サイト名]`
4. テーマとか変えて内容をつくる
5. ローカルホストで確認
6. config.tomlのbaseURLを"https://<アカウント名>.github.io/<リポジトリ名>/"に変更しておく
7. `$ hugo`でビルド -->  publicフォルダができる
8. docsフォルダを自分でつくる(最新版ではいらなさそう)
9. publicフォルダの中身をdocsフォルダにコピー  `$ cp -p -f -R public/* docs` (最新版ではいらなさそう)
10. gitで管理させる(空フォルダ対策必要かも？) `$ git init`     `$ git add .`
11. commit  `$ git commit -m "Initial commit"`
12. `$ git remote add origin https://github.com/<アカウント名>/<リポジトリ名>.git`でリモートリポジトリの追加
13. `$ git push -u origin master`
14. GitHub Pagesの設定 作成したリポジトリ → Settings → GitHub Pages → Source 「master baranch /docs folder」を選択
15. "https://<アカウント名>.github.io/<リポジトリ名>/"に接続して表示されていれば成功



### 更新時

1. 変更
2. `hugo`でビルド
3. `$ git commit -am "comment"`
4. `$ git push -u origin master`
5. (反映までちょっとかかる？)

