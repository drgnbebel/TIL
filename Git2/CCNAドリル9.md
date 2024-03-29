# CCNAドリル 問題.9

問題9.パラメータの調整

CCNA R&S 一問一答

問題
ダイナミックルーティングが有効な構成において、バックアップルートとしてスタティックルートを選択させたい場合には、どのパラメータを調整すればよいですか。選択肢の中から正しいものを1つ選びなさい。

① リンクのコスト
② リンクの遅延
③ アドミニストレーティブディスタンス
④ リンクの帯域幅
⑤ ホップカウント

- 解答

③ アドミニストレーティブディスタンス

- 解説

アドミニストレーティブディスタンスとは、ルート情報の信頼性を表す数値で、0～255までの数値で表現され、値が小さいほど信頼性が高く、優先してルーティングテーブルに挿入されます。デフォルトのアドミニストレーティブディスタンス値は、スタティックが1で、内部EIGRPが90、OSPFが110、RIPが120です。
各ルーティングプロトコルよりもスタティックルートの値の方が小さいため、ルーティングプロトコルを設定してダイナミックルーティングを有効にしている環境で、スタティックルートを設定すると、デフォルトではスタティックルートが優先されてルーティングテーブルに挿入されます。
そのため、スタティックルートをバックアップルートとして使用したい場合には、スタティックルートのアドミニストレーティブディスタンス値をルーティングプロトコルの値より大きくして、スタティックルートの優先度を下げます。