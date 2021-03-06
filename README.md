Webサイト制作テンプレート
==
概要
--
静的なWebサイトや、CMS用のテンプレートを制作する上でベースとなるファイルセットです。

テンプレート
--
テンプレートエンジンとしてEJSを利用しています。

各ページのtitleやdescription等は`app/sitemap.json`に記載します。

EJSファイルは_templateディレクトリ以下に保存。


CSS
--
SASSで記載しています。クラス名の命名規則はBEMをベースに、Atomic DesignやModular Designを取り入れたファイル構成としています。

atomsやmodules等はほぼ空の状態です。サイト毎に結局指定しなおすことになると思うので、お好きに書きやがれください。よく出てくる要素は記載用のファイルを用意していますので、そこに記載していけばいいんじゃないかと思います。

Bootstrap等は含めていないので、必要に応じてbower等でインストールしてください。

始め方
--
リポジトリをcloneした後に、Nodeモジュールとbower管理のライブラリをインストールする必要があります。

    $ git clone git@github.com:oceant/site-template.git
    $ npm install
    $ bower install


基本的な開発方法
--

ブラウザでライブプレビューしながらEJSとSASSが自動コンパイルされます。

    $ gulp serve

納品（サイトアップ）はビルドしたファイルを用います。

    $ gulp build

ビルドファイルのJSやCSS、画像の圧縮等は`gulpfile.babel.js`で設定を変更します。

yeomanのwebappジェネレータをベースとしていますので、testもやればできるはずです。Webサイト制作で必要かはどうかは微妙ですが。
