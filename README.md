# auto-css-skeleton

htmlにリンク付けしたcssのスケルトンを自動生成するパッケージ
#### memo
1. 1つのhtmlファイルに関連するcssファイルは1つとする
2. headタグ内のlinkタグにcssファイルがあるものとする
3. 閉じタグが要らないhtmlタグには閉じタグをつけない、また閉じタグが必要なものには閉じタグを必ずつける
4. ネストにも対応しているが表示方法は並べるだけとなっている
5. 1つのオブジェクトに複数クラスを指定した場合も対応している
