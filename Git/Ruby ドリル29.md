# Rubyドリル 問題 29 配列に格納された数値の合計値を算出するプログラムの実装

概要
本ドリル問題では、配列に格納された3つの数値の合計を算出するプログラムを実装します。

問題
以下の要件を満たすlone_sumメソッドを実装しましょう。

配列に格納された3つの数値の合計を出力する
ただし、同じ数値が2つ以上含まれている場合、その数値は合計する要素に含めない

雛形
def lone_sum(ary)
  # 処理を記述
end

# 呼び出し例
lone_sum([1, 2, 3])
出力例
lone_sum([1, 2, 3]) → 6
lone_sum([3, 2, 3]) → 2
lone_sum([3, 3, 3]) → 0

- 解答

def lone_sum(ary)
  # 配列から、重複しない要素のみ取り出す
  uniq_nums = []
  ary.each do |num|
    count = 0
    ary.each do |i|
      if num == i
        count += 1
      end
    end
    if count < 2
      uniq_nums << num
    end
  end

  # uniq_nums配列内の合計
  sum = 0
  uniq_nums.each do |unique_num|
    sum += unique_num
  end
  puts sum
end

# 呼び出し例
lone_sum([1, 2, 3])