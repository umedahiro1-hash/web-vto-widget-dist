# web-vto-widget（配信用）

Web試着ウィジェットの**ビルド済みバンドルのみ**を配信するリポジトリです。
ソースコードは非公開リポジトリで管理しており、ここには置いていません。

## 埋め込み

ECサイトの任意の場所に、次の1行を入れるだけで動きます。ホスト側のHTML改変は不要です。

```html
<script src="https://umedahiro1-hash.github.io/web-vto-widget-dist/v0.4.0/vto-widget.js"
        integrity="sha384-I06qfzvDWEk6pPh0WLLS/lNTHU9AcHITbixTXRLz6zjhT1e7mVgraC1Ujfz0JQU/"
        crossorigin="anonymous" defer></script>
```

- **バージョンは固定されています。** URL にバージョン番号が入っているため、
  ここに置かれたファイルは今後差し替わりません。更新するときは新しいバージョンのURLに差し替えます。
- **`integrity` は必ず付けてください。** 配信元が万一改ざんされても、
  ハッシュが一致しなければブラウザが実行を拒否します。`crossorigin="anonymous"` は
  クロスオリジンで `integrity` を有効にするために必須です。

## 動作

- アパレル（衣類）の商品ページでのみ「Webで試着する」ボタンを挿入します。
  靴・バッグ・アクセサリー・時計・コスメなどのページでは**DOMに一切何も挿入せず静かに終了**します。
- サーバー通信は一切行いません。入力された身長・体重などはブラウザの localStorage にのみ保存され、
  外部に送信されることはありません。
- 判定理由を確認したいときは、URL に `?vtoDebug=1` を付けてコンソールを開いてください。
  通常時はコンソールに何も出力しません。

## バージョン

| バージョン | SRI |
|---|---|
| v0.4.0 | `sha384-I06qfzvDWEk6pPh0WLLS/lNTHU9AcHITbixTXRLz6zjhT1e7mVgraC1Ujfz0JQU/` |
| v0.3.0 | `sha384-YeNX7xrvD2S18sK8f7tP2AXD0zxoJZjSo+VDe8Z/DfU+RzKho3ptleJA4WmXT9PK` |
| v0.2.0 | `sha384-rFvb7y1EOyH4vtGNzQERQaiOd5ljXuwjAlpNjOEvz1NokmPnJ90QwBtUeWpJU9Sw` |
| v0.1.0 | `sha384-KJJsiyMXoQxR3uSxJQCYC4/OTOT78qzJ+wagow0w2B9W7g+fAFaYMSgwIyhWjiO3` |
