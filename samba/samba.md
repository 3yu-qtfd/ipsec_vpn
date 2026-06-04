## samba user
Server1:~# cat /etc/passwd | grep smb
smbuser:x:1000:1000::/home/smbuser:/bin/sh

## service status
Server1:~# rc-service samba status
 * status: started

## process
Server1:~# ps -ef | grep smb | grep -v grep
 3945 root      0:00 /usr/sbin/smbd -D
 3951 root      0:00 {smbd-notifyd} /usr/sbin/smbd -D
 3952 root      0:00 {smbd-cleanupd} /usr/sbin/smbd -D

## port
Server1:~# netstat -tulnp | grep smb
tcp        0      0 0.0.0.0:445             0.0.0.0:*               LISTEN      3945/smbd
tcp        0      0 0.0.0.0:139             0.0.0.0:*               LISTEN      3945/smbd
tcp        0      0 :::445                  :::*                    LISTEN      3945/smbd
tcp        0      0 :::139                  :::*                    LISTEN      3945/smbd

## shared directories and files

#### before edit
Server1:~# ls -l /samba/share
total 0
-rw-r--r--    1 smbuser  smbuser          0 Mar  5 12:58 testfile.txt

Server1:/etc/samba# cat /samba/share/testfile.txt

#### after editing from remote client
Server1:/etc/samba# ls -l /samba/share
total 4
-rw-r--r--    1 smbuser  smbuser          8 Jun  4 15:48 testfile.txt

Server1:/etc/samba# cat /samba/share/testfile.txt
testfile

