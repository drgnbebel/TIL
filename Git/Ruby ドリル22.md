# Rubyドリル 問題 22 末尾の文字列を3回出力するプログラムの実装

概要
本ドリルでは、対象の文字列の末尾に位置する文字を取得し、それらを任意の回数繰り返して出力するプログラムを実装します。

問題
以下の要件を満たすextra_endメソッドを実装しましょう。

対象の文字列から末尾にある2文字を取得すること
取得した2文字を3回繰り返して出力すること

雛形
def extra_end(str)
  # 処理を記述
end

# 呼び出し例
extra_end('Hello') 
出力例：
extra_end('Hello') → 'lololo'
extra_end('ab') → 'ababab'
extra_end('Hi') → 'HiHiHi'

ヒント
sliceメソッドを使いましょう。

 sliceメソッド
sliceメソッドとは、配列や文字列から指定した要素を取り出すことができるメソッドです。

# 配列を作成します
array = [0,1,2,3,4,5,6]

# 配列から引数で指定した要素を取得します
ele1 = array.slice(1)
puts ele1
#=> 1

# 配列番号-4から4つ分の要素をsliceします
ele2 = array.slice(-4,4)
puts ele2
#=> 3, 4, 5, 6

# 配列はもとのままです
puts array 
#=> [0,1,2,3,4,5,6]
slice!メソッドの詳細は公式ドキュメントを確認しましょう。

- 解答

def extra_end(str)
  right2 = str.slice(- 2, 2)
  puts right2 * 3
end

# 呼び出し例
extra_end('Hello') 