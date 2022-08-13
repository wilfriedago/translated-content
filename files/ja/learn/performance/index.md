---
title: ウェブパフォーマンス
slug: Learn/Performance
tags:
  - CSS
  - HTML
  - HTTP
  - JavaScript
  - Learn
  - Performance
  - Web Performance
translation_of: Learn/Performance
---
<p>{{LearnSidebar}}</p>

<p class="summary">ウェブサイトを構築するには、HTML、CSS、JavaScript が必要です。人々が使いたいと思うウェブサイトやアプリケーションを構築し、ユーザーを惹きつけ、維持するためには、優れた使い勝手を実現する必要があります。優れた使い勝手の一部は、コンテンツの読み込みが速く、ユーザーの操作に反応することです。これは<strong>ウェブパフォーマンス</strong>と呼ばれています。このモジュールでは、パフォーマンスの高いウェブサイトを作成するための基礎知識を学びます。</p>

<p class="summary">初心者向けの教材では、パフォーマンスや<a href="/ja/docs/Learn/Accessibility">アクセシビリティ</a>などのウェブのベストプラクティスをできるだけ忠実に再現するようにしていましたが、このようなテーマにも特に焦点を当てて、よく理解しておくとよいでしょう。</p>

<h2 id="Learning_pathway">学習経路</h2>

<p>多くのウェブパフォーマンスの改善提案を実施するためには、HTML、CSS、JavaScript の知識が必要ですが、ウェブパフォーマンスを理解し測定するためには、アプリケーションの構築方法を知っていることは必須条件ではありません。ただし、このモジュールに取り組む前に、少なくとも<a href="/ja/docs/Learn/Getting_started_with_the_web">ウェブ入門</a>モジュールを使ってウェブ開発の基本的な知識を身につけておくことをお勧めします。</p>

<p>また、以下のようなモジュールを使って、これらのトピックをもう少し深く掘り下げてみるのもよいでしょう。</p>

<ul>
 <li><a href="/ja/docs/Learn/HTML/Introduction_to_HTML">HTML 入門</a></li>
 <li><a href="/ja/docs/Learn/CSS/First_steps">CSS の第一歩</a></li>
 <li><a href="/ja/docs/Learn/JavaScript/First_steps">JavaScript の第一歩</a></li>
</ul>

<p>このモジュールに取り組んだ後は、ウェブパフォーマンスについてもっと深く知りたくなるでしょう。パフォーマンス API の概要、テストと分析ツール、パフォーマンスのボトルネックの問題など、<a href="/ja/docs/Web/Performance">MDN のウェブパフォーマンスの章</a>で多くの詳しい説明を見つけることができます。</p>

<h2 id="Guides">ガイド</h2>

<p>このトピックには、次のモジュールが含まれています。必ず最初のものから始めてください。</p>

<dl>
 <dt><a href="/ja/docs/Learn/Performance/why_web_performance">ウェブパフォーマンスの「なぜ」</a></dt>
 <dd>この記事では、ウェブパフォーマンスがなぜアクセシビリティ、ユーザーエクスペリエンス、ビジネスの目的に重要であるかを解説します。</dd>
 <dt><a href="/ja/docs/Learn/Performance/What_is_web_performance">ウェブパフォーマンスとは</a></dt>
 <dd>ウェブパフォーマンスが重要であることは分かりましたが、ウェブパフォーマンスとは何でしょうか？この記事では、ウェブページの読み込みとレンダリングから、コンテンツがどのようにユーザーのブラウザーに表示されるかを含め、パフォーマンスの構成要素を紹介します。</dd>
 <dt><a href="/ja/docs/Learn/Performance/perceived_performance">ユーザーはパフォーマンスをどう知覚するのか</a></dt>
 <dd>ユーザーがサイトの速さをどのように知覚するかということは、ウェブサイトの速さをミリ秒単位で示すことよりも重要です。 この認識は、実際のページの読み込みロード時間、アイドリング、ユーザー操作への応答性、スクロールやその他のアニメーションのスムーズさに影響されます。この記事では、様々な読み込みの指標、アニメーション、応答性の指標と、実際の時間よりもユーザーの認識を改善するためのベストプラクティスについて説明します。</dd>
 <dt><a href="/ja/docs/Learn/Performance/Measuring_performance">パフォーマンスの計測</a></dt>
 <dd>パフォーマンス指標のいくつかを理解したところで、パフォーマンスツール、指標、API について深く掘り下げ、パフォーマンスをウェブ開発のワークフローの一部にする方法を考えてみます。</dd>
 <dt><a href="/ja/docs/Learn/Performance/Multimedia">マルチメディア: 画像</a></dt>
 <dd>ウェブパフォーマンスの中で最も身近な位置にあるのは、メディアの最適化です。ユーザーエージェントの能力、大きさ、ピクセル密度に応じて、異なるメディアファイルを提供することが可能です。この記事では、画像がパフォーマンスに与える影響と、画像ごとに送信されるバイト数を削減する方法について説明します。</dd>
 <dt><a href="/ja/docs/Learn/Performance/video">マルチメディア: 動画</a></dt>
 <dd>ウェブパフォーマンスの中で最も身近な位置にあるのは、メディアの最適化です。この記事では、動画コンテンツがパフォーマンスに与える影響について説明し、バックグラウンドの動画からオーディオトラックの削除など、パフォーマンスを向上させるためのヒントを紹介します。</dd>
 <dt><a href="/ja/docs/Learn/Performance/JavaScript">JavaScript パフォーマンスのベストプラクティス</a></dt>
 <dd>JavaScript は、適切に使用すれば、インタラクティブで没入感のあるウェブ体験を実現できますが、ダウンロード時間、レンダリング時間、アプリ内のパフォーマンス、バッテリー寿命、ユーザー体験を大きく損なう可能性があります。この記事では、複雑なコンテンツであっても可能な限りパフォーマンスを向上させるために考慮すべき、 JavaScript のベストプラクティスを紹介します。</dd>
 <dt><a href="/ja/docs/Learn/Performance/HTML">HTML のパフォーマンス特性</a></dt>
 <dd>マークアップの属性やソースの順序によっては、ウェブサイトのパフォーマンスに影響を与えることがあります。 DOM ノードの数を最小限に抑え、スタイル、スクリプト、メディア、サードパーティのスクリプトなどのコンテンツを最適な順序と属性を使用して含めることで、ユーザーエクスペリエンスを劇的に向上させることができます。この記事では、最大限のパフォーマンスを確保するために HTML をどのように使用すればよいかを詳しく見ていきます。</dd>
 <dt><a href="/ja/docs/Learn/Performance/CSS">CSS パフォーマンス特性</a></dt>
 <dd>CSS は、パフォーマンス向上のための最適化の焦点としてはあまり重要ではないかもしれませんが、パフォーマンスに影響を与える CSS の特性がいくつかあります。この記事では、パフォーマンスに影響を与えるいくつかの CSS プロパティと、パフォーマンスに悪影響を与えないためのスタイルの処理方法を提案します。</dd>
 <dt><a href="/ja/docs/Learn/Performance/Fonts">フォントとパフォーマンス</a></dt>
 <dd>外部フォントを含める必要があるかどうか、含める場合には、サイトのパフォーマンスへの影響を最小限に抑えながら、デザインに必要なフォントを含める方法について説明します。</dd>
 <dt><a href="/ja/docs/Learn/Performance/Mobile">モバイルパフォーマンス</a></dt>
 <dd>モバイル端末でのウェブアクセスはとても人気があり、すべてのモバイルプラットフォームには本格的なウェブブラウザーが搭載されていますが、帯域幅、CPU、バッテリーの寿命が限られている可能性があるため、これらのプラットフォームでのウェブコンテンツのパフォーマンスを考慮することが重要です。この記事では、モバイルに特化したパフォーマンスの考慮点について説明します。</dd>
 <dt><a href="/ja/docs/Learn/Performance/business_case_for_performance">パフォーマンスの重視</a></dt>
 <dd>パフォーマンスを向上させるために開発者ができることは数多くありますが、どれくらいの速度があれば十分なのでしょうか。このような努力の重要性を権限を持った人に納得させるにはどうすればよいでしょうか。最適化した後、肥大化したパフォーマンスが戻らないようにするにはどうすればよいでしょうか。この記事では、経営陣の説得、パフォーマンス文化とパフォーマンス予算の策定、コードベースにリグレッションが潜り込まないようにする方法を紹介します。</dd>
</dl>

<h2 id="See_also">関連情報</h2>

<dl>
 <dt><a href="/ja/docs/Learn/Performance/Web_Performance_Basics">ウェブパフォーマンスのリソース</a></dt>
 <dd>HTML、CSS、JavaScript、メディアファイルなどのフロントエンドの構成物に加えて、アプリケーションを遅くする機能と、主観的・客観的にアプリケーションを速くする機能があります。ウェブパフォーマンスに関連する API、開発者ツール、ベストプラクティス、バッドプラクティスは数多くあります。ここでは、これらの機能の多くを基本的なレベルで紹介し、それぞれのトピックについて、パフォーマンスを向上させるためのより深い考察へのリンクを提供します。</dd>
 <dt><a href="/ja/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images">レスポンシブ画像</a></dt>
 <dd>この記事では、画面サイズや解像度などが大きく異なる端末でも動作する画像、すなわちレスポンシブ画像の概念を学び、それを実現するために HTML が提供するツールを紹介します。これにより、異なる端末間でのパフォーマンスを向上させることができます。レスポンシブ画像は、<a href="/ja/docs/Learn/CSS/CSS_layout/Responsive_Design">レスポンシブデザイン</a>の一部であり、今後の CSS のテーマとなります。</dd>
 <dt><a href="/ja/docs/Web/Performance">MDN のウェブパフォーマンスの章</a></dt>
 <dd>ウェブパフォーマンスの章 — ここでは、パフォーマンス API の概要、テストと分析ツール、パフォーマンスのボトルネックの問題など、ウェブパフォーマンスに関するより詳細な情報をご覧いただけます。</dd>
</dl>