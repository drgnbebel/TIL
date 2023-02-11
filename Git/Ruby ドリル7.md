# Rubyドリル 問題 7 配列を利用したrubyプログラムの作成

- 概要
本ドリル問題では、任意の数字が配列の中の何番目に格納されているかを確認できるプログラムを実装します。

問題
以下の配列から任意の数字を探して何番目に含まれているかという結果を返すsearchメソッドを、each_with_indexを用いて作成しましょう。

input = [3, 5, 9 ,12, 15, 21, 29, 35, 42, 51, 62, 78, 81, 87, 92, 93]
雛形
以下の雛形のコードを参考に解答しましょう。

def search(target_num, input)
# 処理を記述
end

input = [3, 5, 9 ,12, 15, 21, 29, 35, 42, 51, 62, 78, 81, 87, 92, 93]
# 呼び出し例
search(11, input)
出力例
search(5, input) → 2番目にあります
search(12, input) → 4番目にあります
search(7, input) → その数は含まれていません

- ヒント
 each_with_index
each_with_indexは、Rubyに標準で組み込まれているメソッドの1つです。要素の繰り返し処理と同時に、その要素が何番目に処理されたのかも表すことができます。

以下のように書きます。

配列名.each_with_index  do |item, i|

end
具体的には以下のように使うことができます。

fruits = ["メロン", "バナナ", "アップル"]

fruits.each_with_index do |item, i|
 puts "#{i}番目のフルーツは、#{item}です。"
end
これを実行すると、以下のような出力結果が得られます。

0番目のフルーツは、メロンです。
1番目のフルーツは、バナナです。
2番目のフルーツは、アップルです。

def search(target_num, input)

  input.each_with_index do |num, index|
    if num == target_num
      puts "#{index + 1}番目にあります"
      return
    end
  end
  puts "その数は含まれていません"
end

input = [3, 5, 9 ,12, 15, 21, 29, 35, 42, 51, 62, 78, 81, 87, 92, 93]
search(11, input)