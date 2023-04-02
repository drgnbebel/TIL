# CCNAドリル 問題.4

問題4.デバッグメッセージにミリ秒単位でタイムスタンプを表示

CCNA R&S 一問一答

問題
デバッグメッセージにミリ秒単位でタイムスタンプを表示させるためのコマンドを、次の選択肢の中から1つ選びなさい。

① service timestamps log datetime msec
② service timestamps log datetime localtime
③ service timestamps debug datetime msec
④ service timestamps debug datetime localtime

- 解答

③ service timestamps debug datetime msec

- 解説

インターフェイスのシャットダウンを解除した時やOSPFのネイバーがダウンした時など、様々な場面でコンソールに表示されるメッセージをコンソールログと呼びます。解説の図1はコンソールログのサンプルです。

debug ip icmpなどのdebugコマンドを入力した後、該当の通信や状態変化が発生した時に表示されるメッセージをデバッグメッセージと呼びます。

解説の図2はデバッグメッセージのサンプルです。コンソールログやデバッグメッセージの先頭にはタイムスタンプ（日時もしくは起動してからの時間）を表示することができ、日時の場合は更にどの単位まで表示させるかもコマンドで変更することができます。

コンソールログのタイムスタンプをミリ秒単位で表示させるには、以下のコマンドを使用します。

service timestamps log datetime msec

デバッグメッセージのタイムスタンプをミリ秒単位で表示させるには、以下のコマンドを使用します。

timestamps debug datetime msec

上記のサンプルは、どちらもこれらのコマンドが設定された状態でのものなので、タイムスタンプが月、日、時間、分、秒（ミリ秒単位）の形式で表示されています。

なお、コンソールログには、タイムスタンプの後に %LINK-3-UPDOWNのように「%」から始まる文字列が表示されますが、デバッグメッセージには「%」は含まれません。