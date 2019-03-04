# 2018/03/06

# 今月の目標
- PC(Windows)から正常にgithubにコマンド実行できる環境を作る
- Kotlinのコードをなんでもいいから書く

# やったこと
- GitBashのインストール・動作確認
- PreferenceManagerの使い方

  1. getDefaultSharedPrefarencesで共有プリファレンス取得
  2. putInt,putStringとかでデータを登録
  3. .apply()で保存
     ※2,3は「.」でつなげて記述できる
     
- 加速度センサーを利用したアプリ作成

# 気付き
- ラムダ式
```
fun test(x:Int, l:(Int) -> Int):Int{
 return l(x)
}
```
がKotlinだとreturnと{}が省略できて
```
fun test(x:Int,l:(Int) -> Int):Int = l(x)
```
になる。
戻り値の型が推測できるとさらに以下になる。
```
fun test(x:Int,l:(Int) -> Int) = l(x)
```
  - 結果
    - test(5,{it * 2}) → 10
    - test(5,{it + 1}) → 6
 
ラムダ式は{it*1}の部分？

https://qiita.com/sano1202/items/64593e8e981e8d6439d3  
`ラムダ式とはインターフェースを実装したインスタンスを生成する式`  
`ラムダ式で使用できるのは抽象メソッドが一つのインターフェースのみ`  

# 問題点(ハマったこと)
- SurfaceHolderのインスタンスが取得できない
  - 試したこと
  ```
  getHolder().addCallback(this);
  ```
  はじめてのAndroid書籍の7章のソース自体エラーになる...
  
# 次回目標
- 加速度センサーアプリの完成
