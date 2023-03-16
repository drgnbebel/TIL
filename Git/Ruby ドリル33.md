# Rubyドリル 問題 33 閏年問題

問題
西暦の年数および月を入力し、その月の日数を求めるプログラムを書きます。
その場合、閏年について考慮する必要があります。

閏年は以下の判断基準で決まります。

①その西暦が4で割り切れたら閏年である
②ただし、例外として100で割り切れる西暦の場合は閏年ではない
③ただし、その例外として400で割り切れる場合は閏年である

つまり、西暦2000年は閏年であり、西暦2100年は閏年ではありません。
これらに対応できるように、出力例と雛形をもとに実装しましょう。

出力例
1990年2月 =>"1990年2月は28日間あります"
2000年2月 =>"2000年2月は29日間あります"
2100年2月 =>"2100年2月は28日間あります"
2000年3月=>"2000年3月は31日間あります"

雛形
def get_days(year, month)
  month_days = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
  # ここに処理を書き加えてください
end

puts "年を入力してください："
year = gets.to_i
puts "月を入力してください："
month = gets.to_i

days = get_days(year, month)
puts "#{year}年#{month}月は#{days}日間あります"

- 解答

def get_days(year, month)
  month_days = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
  if month == 2
    if year % 4 == 0
      if year % 100 == 0 && year % 400 != 0
        days = 28
      else
        days = 29
      end
    else
      days = 28
    end
  else
    days = month_days[month - 1]
  end

  return days
end

puts "年を入力してください："
year = gets.to_i
puts "月を入力してください："
month = gets.to_i

days = get_days(year, month)
puts "#{year}年#{month}月は#{days}日間あります"