PWA起動しない時の修正ファイル（manifest / SW）
==============================================
この2ファイルをGitHubのリポジトリ直下に上書き→Vercelで自動デプロイ→再インストールで解決します。

1) 置き換えるファイル
   - manifest.webmanifest（start_urlを"."、scopeを"/"に修正）
   - service-worker.js（CACHE_NAMEを keiba-pwa-ja-v4 に更新）

2) 手順
   a. GitHubのリポジトリページを開く（例：specialweek0423/JRA）
   b. 右上「Add file」→「Upload files」
   c. この2ファイルをドラッグ&ドロップしてアップロード→「Commit changes」
   d. 数十秒でVercelが自動デプロイ
   e. スマホでサイトを開き 5秒待つ→再読み込み
   f. 既存のホームアイコンを削除→もう一度「ホーム画面に追加」

3) 確認
   - https://YOUR-DOMAIN/manifest.webmanifest がJSONで開ける
   - https://YOUR-DOMAIN/service-worker.js が開ける
   - ホームアイコンから起動すると全画面表示になる
