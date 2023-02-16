# Rubyドリル 問題 12 インスタンスの生成

問題
クラスFruitを以下の仕様で定義してください。

インスタンス
インスタンス名  名前       価格
apple         リンゴ     120
orange        オレンジ   200
strawbery     イチゴ     60

インスタンス変数
name
price

クラスメソッド
メソッド名    処理
fresh      「採れたて新鮮な果実です」と表示

インスタンスメソッド
メソッド名   処理
initialize 引数で名前と価格を渡し、インスタンス変数nameとpriceに代入
introduce 「【名前】は【価格】円です」と表示

実行結果は以下のようになります。

採れたて新鮮な果実です
リンゴは120円です
オレンジは200円です
イチゴは60円です

雛形
作ってもらうプログラムのひな形は以下です。

class Fruit
 def クラスメソッド
   # 正しくメソッドを定義した上で、ここに処理を記入してください
 end

 def initialize
   # ここに処理を記入してください
 end

 def インスタンスメソッド
   # 正しくメソッドを定義した上で、ここに処理を記入してください
 end
end

# 3つのインスタンスを生成してください

# クラスメソッドを呼び出し、「採れたて新鮮な果実です」と表示してください
# インスタンス毎にインスタンスメソッドを呼び出し、「【名前】は【価格】円です」と表示してください

- 解答
class Fruit

 def self.fresh
   puts "採れたて新鮮な果実です"
 end

 def initialize(name, price)
   @name = name
   @price = price
 end

 def introduce
   puts "#{@name}は#{@price}円です"
 end
end

apple = Fruit.new("リンゴ", 120)
orange = Fruit.new("オレンジ", 200)
strawberry = Fruit.new("イチゴ", 60)

Fruit.fresh
apple.introduce
orange.introduce
strawberry.introduce