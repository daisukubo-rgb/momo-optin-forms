# MoMo オプトインフォーム

メルマガ登録用オプトインフォーム（Xserver設置用）

## 設置先

Xserver: `momo-gpt.com/email-newsletter/` 配下

| パス | 内容 |
|------|------|
| `prospect/index.html` | 見込み客向けフォーム |
| `prospect/thanks.html` | 見込み客 登録完了ページ |
| `customer/index.html` | 既存顧客向けフォーム |
| `customer/thanks.html` | 既存顧客 登録完了ページ |
| `agent/index.html` | パートナー向けフォーム |
| `agent/thanks.html` | パートナー 登録完了ページ |

## フロー

1. ユーザーがフォーム入力 → JS確認オーバーレイ
2. GAS Web App（doPost）に送信
3. スプレッドシートに「承認済み」で登録
4. タイプ別の自動返信メール送信
5. 完了ページにリダイレクト

## デプロイ

Xserverの `/public_html/email-newsletter/` にこのリポジトリの内容をそのまま配置する。
