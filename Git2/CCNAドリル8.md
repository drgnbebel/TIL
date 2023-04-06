# CCNAドリル 問題.8

問題8.スイッチに設定すべきコマンド

CCNA R&S 一問一答

問題
図にあるレイヤ2スイッチYを新しく追加します。このレイヤ2スイッチYは、管理用ワークステーションからリモート接続して管理する必要があります。このために、スイッチYに設定すべきコマンドとして正しいものを、次の選択肢の中から1つ選びなさい。

①　SwitchY(config)#ip default-network 192.168.2.254[]SwitchY(config)#interface vlan 1[]SwitchY(config-if)#ip address 192.168.2.253 255.255.255.0[]SwitchY(config-if)#no shutdown
②　SwitchY(config)#ip route 192.168.1.0 255.255.255.0 192.168.2.254[]SwitchY(config)#interface vlan 1[]SwitchY(config-if)#ip address 192.168.2.253 255.255.255.0[]SwitchY(config-if)#no shutdown
③　SwitchY(config)#ip default-gateway 192.168.2.254[]SwitchY(config)#interface vlan 1[]SwitchY(config-if)#ip address 192.168.2.253 255.255.255.0[]SwitchY(config-if)#no shutdown
④　SwitchY(config)#ip route 192.168.1.0 255.255.255.0 192.168.2.254[]SwitchY(config)#interface fa0/24[]SwitchY(config-if)#ip address 192.168.2.253 255.255.255.0[]SwitchY(config-if)#no shutdown
⑤　SwitchY(config)#ip default-gateway 192.168.2.254[]SwitchY(config)#interface fa0/24[]SwitchY(config-if)#ip address 192.168.2.253 255.255.255.0[]SwitchY(config-if)#no shutdown

- 解答

⑤　SwitchY(config)#ip default-gateway 192.168.2.254[]SwitchY(config)#interface fa0/24[]SwitchY(config-if)#ip address 192.168.2.253 255.255.255.0[]SwitchY(config-if)#no shutdown

- 解説

レイヤ2スイッチにIPアドレスを設定する場合、interface vlan 1 に対してIPアドレスを設定します。レイヤ2スイッチのfa0/24のような各物理ポートにはIPアドレスを設定することはできません。また、レイヤ2スイッチにはルータのようなIPルーティング機能は備わっていませんので、別サブネットと通信を行うには、PCと同様に「デフォルトゲートウェイ」を設定する必要があります。デフォルトゲートウェイは、グローバルコンフィグレーションモードにおいてip default-gatewayコマンドで設定します。