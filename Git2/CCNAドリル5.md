# CCNAドリル 問題.5

問題5.R1ルーターとR2ルーターが通信できていない原因

CCNA R&S 一問一答

問題
現在、R1ルーターとR2ルーターが通信できていないため、システム管理者がR1/R2でshow int s0/0/0 で状況を確認しました。通信ができない原因を、次の選択肢の中から1つ選びなさい。

① カプセル化タイプの設定誤り
② リンクの信頼性が低すぎる
③ IPアドレスの設定誤り
④ 帯域幅設定が不足している
⑤ サブネットマスクの誤り
⑥ loopbackが設定されていない

- 解答

① カプセル化タイプの設定誤り

- 解説

Serialインターフェイスが正常に動作しているかは、show interfaceコマンドやshow ip interface briefコマンドで表示される StatusとProtocolによって判断できます。 ログを見ると、「Serial0/0/0 is up， line protocol is down」となっているため、次の原因が考えられます。

・ローカルとリモートのルータの設定が誤っている（カプセル化の不一致、レイヤ2認証設定などの不一致）

・ケーブル上のタイミングの問題（CSU/DSU からクロック信号を受信できていない。

・ローカルかリモートの CSU/DSU の障害

・専用回線その他のキャリア サービスの問題：ノイズの多い回線、あるいは、交換機で誤設定による障害が発生している。

なお、それ以外の状態と主な原因、状況は次のようになります。

Serial x is up， line protocol is up

これは正常な状態です。

Serial x is down， line protocol is down

ルータでCD(Carrier Detect)信号を検出できていません。主な原因にはDSU/CSUのハードウェア障害、通信会社の回線がダウン、ケーブル接続の障害などがあります。

Serial x is administratively down， line protocol is down

ルータのSerialインターフェイス設定で shutdown コマンドが設定されています。