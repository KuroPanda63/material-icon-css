# 要約
これはGoogleが開発しているMaterial IconsをFont Awesomeのように使いやすくするものです。<br>
普通に書くと気になる人には気になる問題が結構あるので、それを改善するためのものです。<br>

詳しくは概要を見てください。(長文です)<br>
速く使いたい場合は<b>セットアップ</b>か<b>使い方</b>まで飛ばしてください。<br>

# 概要
これはGoogleが開発しているMaterial IconsをFont Awesomeのように使いやすくするものです。<br>
通常Material Iconsは、`<i class="material-icons">3d_rotation</i>`という風に書きます。<br>

しかしこれでは、フォントを読み込めなかったときに中の文字が見えたり、aタグに挟んだとき文字が表示される(Chromeの場合)など、いろいろな問題があります。<br>

これを解決するには、直接文字コードを挿入しなければいけません。<br>
直接文字コードを挿入するには、HTMLとCSSで2種類の方法があります。<br>
HTMLでは、&amp;#xe84d;(e84dが文字コード)と書き、CSSの場合はセレクターの特定のクラス名に:before(`.target:before`)を付けたし、宣言にcontent: '\\e84d'を追加します。<br>
(Material Iconsのそれぞれの文字コードはここに書かれています ⇒ https://github.com/google/material-design-icons/blob/master/iconfont/codepoints)<br>

しかし、これではいちいちサイトで文字コードを確認して設定…と、手間がかかります、HTMLでアイコンをバンバン使いたい人にとってはちょっと使いにくい部分があります。<br>
そのため、その問題を解決するために作りました。<br>
注意点として、少しCSSの容量が少し(58KB)あるので、その辺が気になる場合はやめた方が良いかな。<br>

# セットアップ
そのままmaterial-icons.min.cssを使うと、Google Fontsからフォントが下ろされます。
もしダウンロードしている場合は、material-icons.cssを編集し、コンパイルしなおしてください。
（コンパイルしなくてもいいけど、容量が多いからした方が良いと思います。）

material-icons.min.cssをHTMLまたはCSSから読み込みます。
```html
<link rel="stylesheet" href="material-icons.min.css">
```
または
```css
@import url(material-icons.min.css);
```

# 使い方
まずは公式サイトの<a href="https://material.io/resources/icons/" target="_blank">アイコン一覧表</a>から、使いたいアイコンを選びます。<br>
例えば、一番最初にある3d_rotationというものを使いたい場合は、<br>
アイコンを置きたい場所に、`<i class="mi-3d-rotation"></i>`と書くと、表示されます。<br>
（アンダーバーはハイフンに変えてください）<br>
