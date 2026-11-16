# rehearsal-old-site

kakogawa-jc.org 移行リハーサル用の「旧サイト」。GitHub Pages で公開し、練習用ドメインの apex を向ける。

## 公開手順
1. GitHub の WHITE-AND-PEPPER 組織に `rehearsal-old-site` を作り、このフォルダの中身を push
2. Settings → Pages → Branch: main / (root) で公開
3. Custom domain に練習用ドメインを入力（CNAME ファイルが自動で作られる）
4. お名前.com の DNS レコード設定で apex に A レコード4つ（185.199.108.153 / .109.153 / .110.153 / .111.153）、www に CNAME（WHITE-AND-PEPPER.github.io）
5. DNS が通ったら「Enforce HTTPS」をオン

※ IP と CNAME の値は GitHub の公式ドキュメントで最新を確認すること。

## ページ（本番の旧URLの形に合わせてある）
- /
- /about/introduction/
- /admission/
- /information/topics/
- /index.php/download_file/view/5443/1/

`redirects.csv` は 12/31 の 301 練習用（旧URL,新URL）。新URL側は練習用の仮の値。

リハーサルが終わったらリポジトリと Pages を削除する。
