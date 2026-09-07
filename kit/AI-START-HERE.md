# AIエージェントへ（このファイルを最初に読ませてください）

あなたはこれから、Docker が動くサーバー上に **Alaveteli（情報公開請求の公開プラットフォーム）** を日本語で構築します。利用者はプログラマーではありません。専門用語で確認を求めず、あなたが判断して進めてください。

## 進める順番

1. `01-構築手順書.md` を最初から最後まで読む
2. `docker compose version`・空きメモリ・ポート（既定 3000。本キットの override は 18383）を確認する
3. `./docker/setup` を実行する（イメージ構築・gem・DB。10〜20分）
4. `config/general.yml`（実体は `config/general-alavetelitheme.yml`）の `AVAILABLE_LOCALES: 'ja en'` `DEFAULT_LOCALE: 'ja'` `SITE_NAME` `DOMAIN` を設定する
5. `./docker/server` で起動し、トップが**日本語で**表示されることを画面で確認する。英語のままなら `docker compose restart app sidekiq`
6. 管理画面（`/admin`）で行政機関（public body）を1件以上登録し、`/select_authority` から請求フォームに進めることを確認してから完了報告する
7. メール（請求の送信・回答の受信）は SMTP/IMAP の設定と MX が要る。開発環境の smtp コンテナはダミーなので、その旨を明記して報告する

## 絶対に守ること

- 管理者パスワード・SMTP の認証情報を、報告文・チャットログに貼らない
- 「たぶん動く」で完了報告しない。画面と `docker compose ps` の実測で確認する
- 本家 Alaveteli・mySociety のサポート窓口に、このキットの質問を送らない（非公式キットです）
