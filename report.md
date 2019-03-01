# 2018/03/06

# 今月の目標
- PC(Windows)から正常にgithubにコマンド実行できる環境を作る
- Kotlinのコードをなんでもいいから書く

# やったこと
- GitBashのインストール・動作確認
- PreferenceManagerの使い方

  1. getDefaultSharedPrefarencesで共有プリファレンス取得
  2. putInt,putStringとかでデータを登録
  3. .appky()で保存
     ※2,3は「.」でつなげて記述できる
     
- 加速度センサーを利用したアプリ作成

# 気付き
- ラムダ関数
  

# 問題点(ハマったこと)
- SurfaceHolderのインスタンスが取得できない
  - 試したこと
  ```
  getHolder().addCallback(this);
  ```
  はじめてのAndroid書籍の7章のソース自体エラーになる...
  
# 次回目標
- 加速度センサーアプリの完成
