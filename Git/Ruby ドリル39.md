# Rubyドリル 問題 39 バブルソート問題2

概要
本ドリルでは、配列の要素である数値を、大きい順に並べ替えて出力するプログラムを実装します。

問題
以下の要件を満たすbubble_sortメソッドを実装しましょう。

要素が数値である配列を受け取り、数値の大きい順に並べ替えること
大きい順に並べ替えた結果を出力すること

雛形
def bubble_sort(data)
  # 配列の数を数える処理を記述
  length = 

  # for文を2つ使用する
  # 先頭から隣の数同士の大きさを比べる
  # 先頭側の要素の方が小さい場合は、配列の位置を隣同士で交換する
end

# 呼び出し例
number = [1,23,4,6,12,45,79]
bubble_sort(number)
puts number
出力例
79
45
23
12
6
4
1

- 解答

def bubble_sort(data)
  length = data.length 
  for i in 0..(length-1) 
    for j in 1.. (length-i-1) 
      if data[j-1] < data[j] 
        data[j-1],data[j] = data[j],data[j-1] 
      end
    end
  end
end

number = [1,23,4,6,12,45,79]

bubble_sort(number)

puts number