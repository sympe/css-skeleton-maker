css-skeleton-maker
--
cssのスケルトンを自動生成するパッケージ

### 目的
cssの無駄な肥大化。これらはHTMLが大きくなればなるほどcssも大きくなりどこにどのセレクタがあるのかわからなくなってしまい、作業の非効率化を招きます。肥大化する原因はネスト構造が考慮しきれなかったり、HTML内では消したタグがcssの方では残っているなど様々な場合が考えられます。css-skeleton-makerはcssの無駄を省き、多くのcssに悩む開発者を助けます。

### 機能
　css-skeleton-makerには以下の機能があります。
  1. **セレクタの自動生成**　HTMLファイルを開いた状態でcss-skeleton-makerを起動するとHTMLを解析してcssのスケルトンを自動で作成します。これによってセレクタをいちいち書く手間が省けます。自動生成なのでセレクタを書く際のスペルミスもありません。セレクタ自動生成については同等の機能を持つ多くのWebサービスがありますが、エディタ内でできるという点が強みです。

  2. **cssのスケルトンを編集しながら使える**　css-skeleton-makerでcssのスケルトンを作成したあとに、cssのセレクタ内にスタイルを書いて、その後にHTMLを編集することもあると思います。その際は、もともと書いてあったスタイルはそのままに、あたらしく追加したHTMLタグがある場合は対応するセレクタを追加し、HTMLタグを削除した場合はセレクタを削除して、cssを常に一番無駄のない状態に保ちます。

  3. **ネストも考慮する**　HTMLのネスト構造を考慮したcssセレクタを作ります。これによってどの要素がどの要素と親子関係であるというのがcssを見ながらわかります。

### 使い方
　1. HTMLファイルのある__フォルダ__をATOMエディタで開きます。**(注意)**　HTMLファイルのみ開くと動作しません。HTMLファイルしか作成していない場合は、フォルダを作成しその中にHTMLファイルを入れて、必ずHTMLを含む__フォルダ__をATOMエディタで開いてください。

　2. HTML内の`<head>`内にcssファイルを指定している`<link>`があるか確認してください。以下の例のように記述すると、フォルダ内のHTMLファイルと同じ場所にcssフォルダを作成し、**style.css** というcssファイルを作成します。
```html
<link rel="stylesheet" type="text/css" href="css/style.css">
```
　上記の例のようなcssの指定がない場合、HTMLファイルと同じ場所に**example.css**という名前のcssファイルを作成します。

　3. cssを作成したいHTMLファイルを開いた状態で、右クリックかメニューバーの`pacakges`から`CSS Skeleton Maker`を選択すると、cssが作成されます。HTML以外を開いた状態では動作しないので注意してください。

### その他注意
1. 1つのhtmlファイルに関連するcssファイルは1つとする
2. html内にコメントがある場合はコメントの箇所は無視する
3. 閉じタグが要らないhtmlタグには閉じタグをつけない **(`<br>`を`<br />`と記述しない)**

　閉じタグの要らないHTMLタグ

　```
<br>,<img>,<hr>,<meta>,<input>,<embed>,<area>,<base>,<col>,<keygen>,<param>,<source>
　```

　上記以外の閉じタグの必要なHTMLタグには必ず閉じタグをつける

### ショートカットキー
`ctrl + alt + l`
