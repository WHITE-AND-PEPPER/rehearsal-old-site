# rehearsal-old-site

ドメイン移行リハーサル用の「旧サイト」。GitHub Pages で公開し、練習用ドメインの apex を向ける。

練習用ドメイン: **wp-rehearsal.xyz**（お名前.com で取得・自動更新オフ）

## 公開手順
1. GitHub の WHITE-AND-PEPPER 組織に `rehearsal-old-site` を作り、このフォルダの中身を push（済）
2. Settings → Pages → Branch: main / (root) で公開
3. Custom domain に `wp-rehearsal.xyz` を入力（CNAME ファイルが自動で作られる）
4. お名前.com の DNS レコード設定（TTL 300）

   | ホスト名 | TYPE | VALUE |
   |---|---|---|
   | （空欄＝apex） | A | 185.199.108.153 |
   | （空欄＝apex） | A | 185.199.109.153 |
   | （空欄＝apex） | A | 185.199.110.153 |
   | （空欄＝apex） | A | 185.199.111.153 |
   | www | CNAME | white-and-pepper.github.io |

5. DNS が通ったら「Enforce HTTPS」をオン
6. 確認: https://wp-rehearsal.xyz/ と https://www.wp-rehearsal.xyz/ で「旧サイト」が出る

※ IP と CNAME の値は GitHub の公式ドキュメントで最新を確認すること。

## ページ（本番の旧URLの形に合わせてある）
- /
- /about/introduction/
- /admission/
- /information/topics/
- /index.php/download_file/view/5443/1/

`redirects.csv` は 12/31 の 301 練習用（旧URL,新URL）。新URL側は練習用の仮の値。

リハーサルが終わったらリポジトリと Pages を削除する。
