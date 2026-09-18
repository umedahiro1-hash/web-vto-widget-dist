# web-vto-widget（配信用）

Web試着ウィジェットの**ビルド済みバンドルのみ**を配信するリポジトリです。
ソースコードは非公開リポジトリで管理しており、ここには置いていません。

## 埋め込み

ECサイトの任意の場所に、次の1行を入れるだけで動きます。ホスト側のHTML改変は不要です。

```html
<script src="https://umedahiro1-hash.github.io/web-vto-widget-dist/v0.9.0/vto-widget.js"
        integrity="sha384-DUkDUO+FrmevvE7wtdJjk/sbtblZVes2bzS+F2skZCSv/gxtQ2wyRCFlwJULz3OS"
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
| v0.9.0 | `sha384-DUkDUO+FrmevvE7wtdJjk/sbtblZVes2bzS+F2skZCSv/gxtQ2wyRCFlwJULz3OS` |
| v0.8.0 | `sha384-6YdWgy5UeACFyEXNC3LVbZohnqB1djyY1PKIlEr72o/HP2K0GACl0pQq3bFMCquo` |
| v0.7.0 | `sha384-5aN30fKtBOd7jptRZuMTGq0WTkyGivdXu0WiXsJ68gOOrXZV3r9BZGnQa/s+amQ9` |
| v0.6.1 | `sha384-kvQbZlAZ8Qo1yNzQ5GnWXI3QQpR46aY3RnZ5E5aXFp1sIRrmg6az9or5YVMRtn14` |
| v0.6.0 | `sha384-VeZlgqmE/A5Z47my2Jk4IT1+2pYgJuEHIPy/wfpMzPiZYKBF7gpUh7z/OXe+Sfv3` |
| v0.5.2 | `sha384-Jn+lJ0dHPXoO8hrYVwqPvJVJdTMFF+fo7qU1zsJc8mSnvkhoEHkKiUPSqFMEPjfZ` |
| v0.5.1 | `sha384-1y/RT+7BON/V+naLVI+5iQ08tfvbjvg3gHMLOHzV/XkQCoHwUuDAAp5J6oeyrili` |
| v0.5.0 | `sha384-1y/RT+7BON/V+naLVI+5iQ08tfvbjvg3gHMLOHzV/XkQCoHwUuDAAp5J6oeyrili` |
| v0.4.1 | `sha384-qpGyuVclRJ8UjpCtZLJJ8bWLQUh3rI46bBEiW4KBlsKlYvnc9uDRkoB0HJ1+erZz` |
| v0.4.0 | `sha384-I06qfzvDWEk6pPh0WLLS/lNTHU9AcHITbixTXRLz6zjhT1e7mVgraC1Ujfz0JQU/` |
| v0.3.0 | `sha384-YeNX7xrvD2S18sK8f7tP2AXD0zxoJZjSo+VDe8Z/DfU+RzKho3ptleJA4WmXT9PK` |
| v0.2.0 | `sha384-rFvb7y1EOyH4vtGNzQERQaiOd5ljXuwjAlpNjOEvz1NokmPnJ90QwBtUeWpJU9Sw` |
| v0.1.0 | `sha384-KJJsiyMXoQxR3uSxJQCYC4/OTOT78qzJ+wagow0w2B9W7g+fAFaYMSgwIyhWjiO3` |
