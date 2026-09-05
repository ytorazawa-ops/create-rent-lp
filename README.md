# 株式会社クリエイト・レント LP モックアップ

イベント・フードイベント向け「仮設厨房／厨房機器レンタル」サービスサイトLP（1枚もの）のモックアップです。
ファーストビューの写真が異なる2案を同一リポジトリに収めています。

| ファイル | 内容 |
| --- | --- |
| `index.html` | **A案** ファーストビュー＝厨房（職人）写真 |
| `index-b.html` | **B案** ファーストビュー＝宴会会場写真 |
| `assets/` | ロゴ・写真（両案で共用） |

FV以外の内容は2案で同一です。各ページ上部のバーからもう一方の案へ移動できます。

## GitHub Pages で公開する

1. このフォルダの中身をリポジトリのルートに置いて push
2. Settings → Pages → Source を `Deploy from a branch`、Branch を `main` / `/ (root)` に設定
3. 公開URL
   - A案: `https://<user>.github.io/<repo>/`
   - B案: `https://<user>.github.io/<repo>/index-b.html`

`.nojekyll` を同梱しているため、Jekyll の処理は行われずそのまま静的配信されます。

## 仕様

- 静的HTML1枚（ビルド不要・PHP不要）。画像は相対パス `assets/...`
- レスポンシブ対応（PC／タブレット／スマホ）。スマホでは下部に電話／お問い合わせの固定バーを表示
- スクロールで各セクションがフェードイン（`prefers-reduced-motion` 時は無効）
- 外部読み込み：Google Fonts（Oswald / Noto Sans JP / JetBrains Mono）、Google マップ埋め込み（3拠点）

## お問い合わせフォーム

`<form action="contact.php" method="post">` で送信します。**送信処理のPHPは含まれていません**（モックアップのため）。
本番では `contact.php` を用意するか、フォームサービスの送信先URLを `action` に設定してください。

送信項目（name属性）

| name | 項目 | 必須 |
| --- | --- | --- |
| `name` | お名前 | ○ |
| `company` | 会社名・団体名 | |
| `tel` | 電話番号 | ○ |
| `email` | メールアドレス | ○ |
| `start_date` | 利用開始希望日 | ○ |
| `end_date` | 利用終了希望日 | ○ |
| `place` | 会場・設置場所 | |
| `services[]` | 希望サービス（複数選択） | |
| `message` | お問い合わせ内容 | ○ |

## 素材について

- 写真・ロゴはクライアント支給素材です。取り扱いにご注意ください
- ロゴは背景透過（SVG推奨）データがあると、あらゆる背景色でより綺麗に表示できます
- 公開ドメイン確定後は `og:image` を絶対URLに変更してください
