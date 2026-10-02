# ブランド検索(Webアプリ版)— Windows だけで iPhone に入れる方法

iPhone のホーム画面に追加すると、アプリのように全画面で起動します。
一度開いたあとは機内モードでも動きます。

## 1. GitHub Pages に置く(無料・10分ほど)
1. https://github.com でアカウントを作成
2. 右上の「+」→ New repository → 名前を `brand-search` などにして **Public** で作成
3. 「uploading an existing file」をクリックし、このフォルダのファイルをすべてドラッグ → Commit changes
   (index.html / manifest.json / sw.js / icon-180.png / icon-192.png / icon-512.png)
4. Settings → Pages → Branch を `main` / `(root)` にして Save
5. 1〜2分後、`https://ユーザー名.github.io/brand-search/` で開けるようになります

## 2. iPhone に入れる
1. iPhone の **Safari** で上の URL を開く
2. 共有ボタン → 「ホーム画面に追加」
3. ホーム画面のアイコンから一度起動(このときオフライン用に保存されます)

## データを更新するとき
1. Windows で Excel を編集
2. もう一度 Claude に Excel をアップロードして index.html を作り直してもらう
3. GitHub の index.html を上書きアップロードし、sw.js の `v1` を `v2` に変更
4. iPhone でアプリを開き直す(ネット接続中に2回起動すると新しいデータに切り替わります)

## 注意
- Public リポジトリは URL を知っている人なら誰でも見られます。社外秘のリストなら、
  Netlify(パスワード保護は有料)など公開範囲を制限できるサービスも検討してください。
