---
title: ETag
slug: Web/HTTP/Headers/ETag
tags:
  - HTTP
  - Reference
  - ヘッダー
  - リファレンス
  - レスポンス
  - レスポンスヘッダー
translation_of: Web/HTTP/Headers/ETag
---
{{HTTPSidebar}}

**`ETag`** は HTTP のレスポンスヘッダーで、リソースの特定バージョンの識別子です。ウェブサーバーは、コンテンツが変更されていない場合はレスポンス全体を再送する必要がないので、キャッシュがより効率的になり通信帯域を節約することができます。加えて、 ETag はリソースが同時に更新されて互いを上書きすること ([「空中衝突」](#Caching_of_unchanged_resources)) を防ぐのに役立ちます。

指定された URL のリソースが変更された場合は、新しい `Etag` 値を生成する必要があります。したがって Etags はフィンガープリントに似ており、一部のサーバーでの追跡目的でも使用される可能性があります。これらを比較することで、リソースの 2 つの表現が同じかどうかを素早く判断できますが、トラッキングサーバーによって無限に保持されるように設定することもできます。

| ヘッダー種別                                                                         | {{Glossary("Response header", "レスポンスヘッダー")}} |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| {{Glossary("Forbidden header name", "禁止ヘッダー名")}} | いいえ                                                                               |

## 構文

    ETag: W/"<etag_value>"
    ETag: "<etag_value>"

## ディレクティブ

- `W/` {{optional_inline}}
  - : `'W/'` (大文字) は[弱いバリデーター](/ja/docs/Web/HTTP/Conditional_requests#Weak_validation)を使用することを示します。弱い ETag は生成が簡単ですが、比較にはあまり役立ちません。強力なバリデーターは比較には理想的ですが、効率的に生成するのはとても困難です。同じリソースを表現する 2 つの弱い `Etag` の値があった場合、意味的には同等ですが、バイト単位では同じではない可能性があります。すなわち、弱い ETag は[バイト範囲指定のリクエスト](/ja/docs/Web/HTTP/Headers/Accept-Ranges)が行われたときにキャッシュされませんが、強い ETag は範囲指定のリクエストもキャッシュします。
- "\<etag_value>"
  - : 要求されたリソースを一意に表すエンティティタグです。これは二重引用符で囲まれた ASCII 文字列であり、 `"675af34563dc-tr34"`のような形です。 `ETag` 値が生成される方法は指定されていません。コンテンツのハッシュ、最終更新タイムスタンプのハッシュ、単なるリビジョン番号などがよく使用されます。たとえば、 MDN は Wiki 記事コンテンツのハッシュを使用しています。

## 例

    ETag: "33a64df551425fcc55e4d42a148795d9f25f89d4"
    ETag: W/"0815"

### 空中衝突の回避

`ETag` と {{HTTPHeader("If-Match")}} ヘッダの助けを借りて、編集の空中衝突を検出することができます。

たとえば、 MDN を編集する場合、現在の Wiki コンテンツのハッシュが算出され、そのレスポンスで `Etag` に入れられます。

    ETag: "33a64df551425fcc55e4d42a148795d9f25f89d4"

Wiki ページに変更を保存 (データの投稿) するとき、 {{HTTPMethod("POST")}} リクエストには、 {{HTTPHeader("If-Match")}} ヘッダーに `ETag` 値を入れて、新しいかどうかをチェックします。

    If-Match: "33a64df551425fcc55e4d42a148795d9f25f89d4"

ハッシュが一致しない場合は、文書が途中で編集されたことを意味し、 {{HTTPStatus("412")}} `Precondition Failed` エラーが発生します。

### 変更されていないリソースのキャッシュ

もう一つの `ETag` ヘッダーの典型的な使用例として、変更されていないリソースをキャッシュすることがあります。ユーザーが (`ETag` が設定されている) 指定された URL を再度訪問した時、それが*古くなったもの* (古すぎて使用できない) であった場合、クライアントは {{HTTPHeader("If-None-Match")}} ヘッダー欄で `ETag` の値を送ります。

    If-None-Match: "33a64df551425fcc55e4d42a148795d9f25f89d4"

サーバーは、クライアントの `ETag` (`If-None-Match` で送信されたもの) を現在のバージョンの `ETag` と比較し、両方の値が一致する (つまりリソースは変更されていない) 場合、サーバーは {{HTTPStatus("304")}} `Not Modified` ステータスを本文なしで返送し、キャッシュされたレスポンスのバージョンがまだ使用可能 (新しい) であることをクライアントに通知します。

## 仕様書

| 仕様書                                   | 題名                                                         |
| ---------------------------------------- | ------------------------------------------------------------ |
| {{RFC("7232", "ETag", "2.3")}} | Hypertext Transfer Protocol (HTTP/1.1): Conditional Requests |

## ブラウザーの互換性

{{Compat("http.headers.ETag")}}

## 関連情報

- {{HTTPHeader("If-Match")}}
- {{HTTPHeader("If-None-Match")}}
- {{HTTPStatus("304")}}` Not Modified`
- {{HTTPStatus("412")}}` Precondition Failed`
- [W3C Note: Editing the Web – Detecting the Lost Update Problem Using Unreserved Checkout](https://www.w3.org/1999/04/Editing/)