花房 UC銀行 GitHub Pages 本番版

配置:
  index.html
  .nojekyll

Supabase接続:
  Project URL と publishable key は index.html に設定済みです。
  service_role / secret key は含まれていません。

公開後:
  1. GitHub Pages の公開URLを確認
  2. Supabase Authentication > URL Configuration
  3. Site URL に公開URLを設定
  4. Redirect URLs に同じ公開URLを追加
  5. 新規登録 / ログイン / パスワード再設定 / 持出 / 持込を本番URLで確認

実装済み:
  - Email/Passwordログイン
  - 新規登録
  - パスワード再設定
  - ユーザー/管理者のrole分岐
  - wallets / profiles / transactions / events_public 読込
  - withdraw_uc による BANK -> VRC 持出
  - HNB1スクランブルコード生成
  - VRC -> BANK コード復号と deposit_uc 実行
  - profile は display_name / vrc_name のみ更新

未実装/今後:
  - 管理者UC手動補正RPC
  - 口座凍結/解除RPC
  - アラート自動生成ロジック
  - VRC UdonSharp側のコード生成/復号
