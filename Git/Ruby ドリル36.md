# Rubyドリル 問題 36 損益計算アプリケーション1

問題
以下の仕様を満たすアプリケーションを作成してください。また、必ず注意書きを読んでから作成に取り掛かってください。

仕様
プログラムを実行すると、以下の3つの選択肢が表示され、直後にユーザーに対して値の入力を求めること。
[1] : 商品を登録する
[2] : 商品の一覧を確認する
[3] : アプリを終了する
[1]を選択した場合は、商品名、販売価格、仕入れ値を入力させ、保存する。
[2]を選択した場合は、保存された全ての商品情報（商品名・販売価格・仕入れ値）を商品ごとに一覧表示する。
[3]を選択した場合は、アプリケーションを終了する。
アプリケーションを終了するまで、処理を繰り返すこと。

注意
雛形を使用すること
引数は雛形で考慮していないため、必要に応じて引数を設定すること
正しく動作している箇所までが採点対象となるため、必ず動作確認しながら進めること
エラーはインターネットで調べるなどして解決すること
エラーが出たままその先の実装をしないこと

ヒント
必要な知識
ハッシュオブジェクト
式展開
配列オブジェクト
引数
each文
条件分岐

雛形
def register_item(registered_item)
  # 商品名・販売価格・仕入れ値の入力を促し、入力された値をハッシュオブジェクトで管理する
  puts "商品名を入力してください："
  puts "販売価格を入力してください："
  puts "仕入れ値を入力してください："
  line = "---------------------------"

  # 入力された値（ハッシュオブジェクトで管理している値）を表示する
  puts "商品名 : \n#{line}"
  puts "販売価格 : 円\n#{line}"
  puts "仕入れ値 : 円\n#{line}"
end

def check_items(registered_item)
  # 保存された全ての商品情報（商品名・販売価格・仕入れ値）を商品ごとに一覧表示する
  line = "---------------------------"
  puts "【商品一覧】\n#{line}"

  registered_item.each do |item|
    puts "商品名："
    puts "販売価格：円"
    puts "仕入れ値：円"
  end
end

def end_program
  exit
end

def exception
  puts "入力された値は無効な値です"
end

item_list = []         # 配列オブジェクトitem_listの生成

while true do
  # メニューの表示
  puts "商品数: #{item_list.length}"
  puts "[1]商品を登録する"
  unless item_list.empty?
    puts "[2]商品の一覧を確認する"
  end
  puts "[3]アプリを終了する"

  input = gets.to_i

  if input == 1 then
    item_list = register_item(item_list)  # register_itemメソッドの呼び出し
  elsif input == 2 then
    check_items(item_list)     # check_itemsメソッドの呼び出し
  elsif input == 3 then
    end_program     # end_programメソッドの呼び出し
  else
    exception       # exceptionメソッドの呼び出し
  end
end

- 解答

def register_item(registered_item)
  # 商品名・販売価格・仕入れ値の入力を促し、入力された値をハッシュオブジェクトで管理する
  item = {}
  puts "商品名を入力してください："
  item[:name] = gets.chomp
  puts "販売価格を入力してください："
  item[:selling_price] = gets.to_i
  puts "仕入れ値を入力してください："
  item[:cost_price] = gets.to_i
  line = "---------------------------"

  # 入力された値（ハッシュオブジェクトで管理している値）を表示する
  puts "商品名 : #{item[:name]}\n#{line}"
  puts "販売価格 : #{item[:selling_price]}円\n#{line}"
  puts "仕入れ値 : #{item[:cost_price]}円\n#{line}"

  # ハッシュを配列オブジェクトに追加する
  registered_item << item

  # registered_itemをメソッドの呼び出し元に返す
  return registered_item
end

def check_items(registered_item)
  # 保存された全ての商品情報（商品名・販売価格・仕入れ値）を商品ごとに表示する
  line = "---------------------------"
  puts "【商品一覧】\n#{line}"

  registered_item.each do |item|
    puts "商品名：#{item[:name]}"
    puts "販売価格：#{item[:selling_price]}円"
    puts "仕入れ値：#{item[:cost_price]}円\n#{line}"
  end
end

def end_program
  exit
end

def exception
  puts "入力された値は無効な値です"
end

item_list = []              # 配列オブジェクトitem_listの生成

while true do
  # メニューの表示
  puts "商品数: #{item_list.length}"
  puts "[1]商品を登録する"
  unless item_list.empty?
    puts "[2]商品の一覧を確認する"
  end
  puts "[3]アプリを終了する"

  input = gets.to_i

  if input == 1 then
    item_list = register_item(item_list)  # register_itemメソッドの呼び出し
  elsif input == 2 then
    check_items(item_list)          # check_itemsメソッドの呼び出し
  elsif input == 3 then
    end_program               # end_programメソッドの呼び出し
  else
    exception            # exceptionメソッドの呼び出し
  end
end