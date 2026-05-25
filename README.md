## 概要
- ネットワーク・サーバの理解を深めるため、企業ネットワークを模した環境をVMware上に構築しました。
- 各コンポーネントの構成と、検証内容を載せています。

## 構成図
<img width="1154" height="762" alt="image" src="https://github.com/user-attachments/assets/e3c4d04e-da57-44c3-b44a-3e31f61b103a" />

## 構成
#### ネットワーク
- FortiGate VM
- IPsec VPN

#### サーバ
- NFS
- Samba
- BIND (権威DNS / キャッシュDNS)
- Nginx (リバースプロキシ)
- Apache

## 検証内容
