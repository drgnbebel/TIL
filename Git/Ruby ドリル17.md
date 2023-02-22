# Rubyドリル 問題 17 if,else問題

問題
概要
本ドリルでは、指定された範囲の数値によって処理が異なるプログラムを実装します。

問題
以下の要件を満たすparrot_troubleメソッドを実装しましょう。

最近、あなたはオウムを飼いはじめました。しかし、近隣から「夜にオウムの鳴き声がうるさい」と苦情がくるようになりました。あなたはこれをシステムで解決しようと考え、次のようなプログラムの要件を考えました。

第一引数にオウムが鳴く場合はtrueを指定し、鳴かないfalseを指定する
第二引数には時間を指定する（ただし、「分」は考えないものとする）
20時から翌朝7時までの間にオウムが鳴いた場合は「NG」と出力する（20時と7時は含まれない）
上記以外の場合は「OK」と出力する

雛形
def parrot_trouble(talking, hour)
  # ここに条件式を実装する
end

# 呼び出し例
parrot_trouble(true, 6)
出力例
parrot_trouble(true, 6) → NG
parrot_trouble(true, 7) → OK
parrot_trouble(false, 6) → OK
parrot_trouble(false, 7) → OK

- 解答

def parrot_trouble(talking, hour)
  if talking && (hour < 7 || hour > 20)
    puts "NG"
  else
    puts "OK"
  end
end

# 呼び出し例
parrot_trouble(true, 6)