# メモ

* アダプターと呼ばれるクラス群でコード量を少なくできることを体験。
  * MouseMotionAdapter, WindowAdapterの2つのアダプタークラスの動作を確認した。
  * 参照先) java言語で学ぶデザインパターン入門 第3版 p413 Commandパターンの解説
  * 参照先) java言語で学ぶデザインパターン入門 第3版 p413 Commandパターン　練習問題22-3
  * Javaの無名クラス（匿名クラス）という機構を組み合わせてアダプターを使っているとのこと

* Javaで手軽、簡単なGUIのつくりかた
  * 参照先) java言語で学ぶデザインパターン入門 第3版 p399 Commandパターンサンプルプログラム お絵描きソフト
    * マウスドラッグで赤で描画する。ボタン押下で描画をクリアする
  * 参照先) java言語で学ぶデザインパターン入門 第3版 p345 Stateパターンサンプルプログラム 金庫警備システム
    * ボタン押下した際の時刻により、テキストボックスへの表示がかわる。昼、夜の状態により挙動がかわる。

* クラス名を書かずに、外部から与えられたに文字列でインスタンス生成する（リフレクション）
  * 参照先) java言語で学ぶデザインパターン入門 第3版 p112 Abstract Factory 抽象的な工場 : Factoryクラス, 練習問題21-1 本の回答例

* スレッドセーフなメソッドにするには?
  * synchronizedキーワードをつける
    * java言語で学ぶデザインパターン入門 第3版 練習問題20-3 本の回答例

* ラムダ式の使い方
  * java言語で学ぶデザインパターン入門 第3版 練習問題19-1 本の回答例

* ファイルの読み、書き
  * java言語で学ぶデザインパターン入門 第3版 練習問題18-4 本の回答例

* java.nio.fileパッケージには、Visitorパターンを使ってファイルシステム中のディレクトリやファイルを訪問するクラスライブラリがある
  *  (参考) [java言語で学ぶデザインパターン入門第3版 Visitorパターン](https://github.com/grace2riku/design_patterns_java_copy/blob/main/ch_13_Visitor/Exercises/13_3/13_3.md)
