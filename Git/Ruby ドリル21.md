# Rubyドリル 問題 21 簡単な計算を行うRubyプログラムの作成

問題
二桁以上の整数を入力すると、十の位と一の位の数字の足し算、十の位と一の位の数字の掛け算をそれぞれ行い、最後に2つの結果を足し合わせて出力するプログラムをRubyで作成してください。

ヒント
・入力にはgetsメソッドを利用しましょう。数値型に変換することを忘れないようにしましょう。
・ある整数について、整数を10で割った計算結果の余りが1の位、整数を10で割ったものを更に10で割った計算結果の余りが10の位となります。

ターミナルでの入力例

sample.rb

> 二桁の整数を入力してください
> 15

# 1 + 5 と 1 × 5 をそれぞれ計算

> 足し算結果と掛け算結果の合計値は11です

- 解答

def addition(a, b)
  a + b
end

def multiplication(a,b)
  a * b
end

def slice_num(num)
  # 10の位
  tens_place = (num / 10) % 10
  # 1の位
  ones_place = num % 10
  return tens_place, ones_place
end

puts "二桁の整数を入力してください"
input = gets.to_i
X, Y = slice_num(input)
add_result = addition(X, Y)
multiple_result = multiplication(X, Y)
puts "足し算結果と掛け算結果の合計値は#{add_result + multiple_result}です"