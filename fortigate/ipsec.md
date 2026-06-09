FGVMEVR9SYWYUME5 # diagnose vpn ike gateway list

vd: root/0
name: test-p1_0
version: 1
interface: port1 3
addr: 192.168.171.100:500 -> 192.168.171.129:500
tun_id: 192.168.171.129/::10.0.0.3
remote_location: 0.0.0.0
network-id: 0
transport: UDP
created: 696s ago
xauth-user: testuser
2FA: no
peer-id: 192.168.171.129
peer-id-auth: no
FortiClient UID: 7BC1ABFE3E5B412AAE48621E989525B9
assigned IPv4 address: 10.10.10.10/255.255.255.255
pending-queue: 0
IKE SA: created 1/1  established 1/1  time 10/10/10 ms
IPsec SA: created 1/1  established 1/1  time 0/0/0 ms

  id/spi: 1 7d01eaf19d732e02/4b0d2cd61ab79746
  direction: responder
  status: established 696-696s ago = 10ms
  proposal: des-sha256
  key: c98c75c03cc40ece
  QKD: no
  PQC-KEM (IKE): no
  PQC-KEM (all IPsec): no
  lifetime/rekey: 86400/85433
  DPD sent/recv: 00000000/00000089
  peer-id: 192.168.171.129


