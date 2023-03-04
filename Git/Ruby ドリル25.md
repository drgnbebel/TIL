# Rubyドリル 問題 25 FizzBuzz問題

FizzBuzz問題
非常に有名なプログラミングの問題です。1〜100までの数字をターミナルに出力してください。ただし、「3の倍数」のときは数字の代わりに文字列でFizzと、「5の倍数」のときはBuzz、3と5の倍数である「15の倍数」のときはFizzBuzzと出力してください。

作ってもらうプログラムのひな形は以下です。

question1.rb

def fizz_buzz
  # ここに処理を書き加えてください
end

fizz_buzz
ヒント
① 問題文で与えられている仕様を整理すると以下のようになります

数字の1~100を出力する
値が3の倍数のときだけ、"Fizz"という出力に置き換える
値が5の倍数のときだけ、"Buzz"という出力に置き換える
値が3と5の倍数のときだけ、"FizzBuzz"という出力に置き換える
②「〇〇の倍数」を導き出す時は剰余演算子を用いましょう

③条件を指定して繰り返し処理をする場合は、whileというメソッドを使いましょう

- 解答

question1.rb

def fizz_buzz
  num = 1
  while num <= 100 do
    if num % 3 == 0    # 3の倍数のとき
      puts "Fizz"
    elsif num % 5 == 0    # 5の倍数のとき
      puts "Buzz"
    else    # それ以外のとき
      puts num
    end

    num = num + 1
  end
end

fizz_buzz