# CCNAドリル 問題.15

問題15.showコマンド

CCNA R&S 一問一答

問題
アクティブなtelnet接続を確認できるshowコマンドを、次の選択肢の中から1つ選びなさい。

① show cdp neighbors
② show sessions
③ show cdp entry *
④ show vty login

- 解答

② show sessions

- 解説

Telnet接続を確認するには、show sessions コマンドを使用します。show sessionsコマンドを使用すると、Telnet接続を確立したホストのリストが表示されます。また、show usersコマンドを使うと、現在アクティブなEXECセッションとしてコンソールからの接続ユーザとTelnetからの接続セッションを同時に確認できます。show users コマンドの出力では、「con」がローカルコンソールを表し、「vty」がリモート接続を表します。ユーザが複数存在する場合は、アスタリスク(*)が現在の端末セッションユーザを示します。