# CCNAドリル 問題.3

問題3.Catalystスイッチの設定

CCNA R&S 一問一答

問題
Catalystスイッチでswitchport trunk native vlan 10コマンドを設定すると、どのように動作しますか。次の選択肢の中から1つ選びなさい。

① VLAN 10インターフェイスを作成する
② VLAN10の情報はトランクリンクでタグを付けずに転送する
③ スイッチのデフォルトVLANを10に設定する
④ トランクリンクからVLAN10宛てのトラフィックをブロックする

- 解答

② VLAN10の情報はトランクリンクでタグを付けずに転送する

- 解説

switchport trunk native vlan コマンドは、トランクポートに設定するコマンドです。トランクポートでは各VLANの情報はタグ付けされますが、Native VLANに限りタグ付けされません。