## 目的
- ネットワーク・サーバの理解を深めるため、企業ネットワークを模した環境をVMware上に構築しました。

## 構成図
<img width="1160" height="734" alt="image" src="https://github.com/user-attachments/assets/79b06749-a208-46fd-985c-f5c21c25bfc3" />

## 構築内容
#### ネットワーク
- FortiGate VM：各仮想マシン間を接続
- IPsec VPN：LAN外のホスト～LANサーバ間を接続

#### サーバ
- Server1：NFS(クライアント)、Samba、BIND(キャッシュDNS）、Nginx(リバースプロキシ)
- Server2：NFS(サーバ)、BIND(権威DNS)、Apache

## 制約
- 通信経路は以下の通りに制限しています。（無償版FortiGateで登録できるファイヤーウォールのポリシーが3つまでのため）
  1. LAN間：Server1→FortiGate→Server2
  2. インターネット：Server1 or Server2→FortiGate→インターネット　※必要に応じ送信元ポートを変更
  3. IPsec VPN：Windows 11→FortiGate→Server1
