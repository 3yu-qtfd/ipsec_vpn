## dig
Server20:~# dig www.lab.local

; <<>> DiG 9.20.20 <<>> www.lab.local
;; global options: +cmd
;; Got answer:
;; WARNING: .local is reserved for Multicast DNS
;; You are currently testing what happens when an mDNS query is leaked to DNS
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 60968
;; flags: qr aa rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 1232
; COOKIE: a43e6af403e6eabb010000006a2266a1f74864707db0d85c (good)
;; QUESTION SECTION:
;www.lab.local.                 IN      A

;; ANSWER SECTION:
www.lab.local.          3600    IN      A       192.168.20.20

;; Query time: 3 msec
;; SERVER: 192.168.10.10#53(192.168.10.10) (UDP)
;; WHEN: Fri Jun 05 15:03:13 JST 2026
;; MSG SIZE  rcvd: 86

## Screenshots (Windows 11)
