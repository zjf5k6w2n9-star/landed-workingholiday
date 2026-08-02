# LANDED

トロントでワーキングホリデー(IEC)ビザ滞在中の日本人が、同じくワーホリで来る日本人向けに提供する
「生活立ち上げサポート」個人ビジネスのランディングページ。

- 本体: [`index.html`](index.html)(単一HTMLファイル)
- プロジェクト背景・料金・法的な注意点など: [`docs/PROJECT_CONTEXT.md`](docs/PROJECT_CONTEXT.md)

## デプロイ

Netlifyにこのリポジトリを連携し、`main` ブランチへのpushで自動デプロイされる構成です。
ビルドステップは無く、リポジトリルートをそのまま公開します(`netlify.toml` 参照)。

## お問い合わせフォーム

`index.html` 内の `#contact-form` は [Netlify Forms](https://docs.netlify.com/manage/forms/setup/) を利用しています。
Netlifyへのデプロイ後、追加設定なしでフォーム送信をNetlify管理画面上で受信できます(通知メール設定はNetlify側で別途行ってください)。

## モニター残り枠の更新

`index.html` 内 `<script>` の先頭にある `SLOTS` オブジェクトの `remaining` の数字を書き換えるだけで、
料金セクションの残り枠表示とバーが自動的に更新されます。

## OGP画像

`docs/assets/og-image-src.html` にOGP画像(1200x630)のデザインソースがあります。
まだ実際のJPG/PNGとして書き出せていないため、`index.html` の `og:image` は仮のパス(`/og-image.jpg`)を指しています。
書き出し後、リポジトリルートに `og-image.jpg` として配置してください。
