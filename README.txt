株式会社クリエイト・レント LP — サーバー設置用データ
====================================================

【同梱ファイル】
  index.html      … LP本体（静的HTML1枚）
  assets/         … 使用画像5点
  README.txt      … 本ファイル

【設置手順】
  1. index.html と assets/ フォルダを、同じ階層のままサーバーにアップロードします。
     例）/public_html/index.html, /public_html/assets/...
  2. これだけで表示されます（PHP等の必須要件はありません）。
  3. 画像パスは相対指定（assets/...）です。フォルダ構成は変えないでください。

【お問い合わせフォームについて】
  <form action="contact.php" method="post"> で送信する設定にしてあります。
  送信処理（メール送信）のPHPは含まれていません。以下のいずれかで対応してください。
    a) contact.php を用意し、POSTされた値をメール送信する
    b) 既存のフォーム設置サービスの送信先URLを action="" に差し替える
  送信される項目名（name属性）:
    name       … お名前（必須）
    company    … 会社名・団体名
    tel        … 電話番号（必須）
    email      … メールアドレス（必須）
    use_date   … 利用希望日
    place      … 会場・設置場所
    services[] … 希望サービス（複数選択）
    message    … お問い合わせ内容（必須）

【外部読み込み】
  ・Google Fonts（Oswald / Noto Sans JP / JetBrains Mono）
  ・Google マップ埋め込み（会社案内の3拠点）
  いずれもインターネット接続が必要です。

【SEO・OG】
  title / description / og:* を index.html の <head> に記載済みです。
  独自ドメインが決まったら og:image を絶対URL（https://…/assets/hero-buffet-2.jpg）に
  書き換えることを推奨します。
