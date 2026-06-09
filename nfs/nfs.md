## exportfs
Server10:~# exportfs -v
/srv/nfs        192.168.20.0/24(sync,wdelay,hide,no_subtree_check,sec=sys,rw,secure,no_root_squash,no_all_squash)

## mount (manual)
Server20:~# mount 192.168.10.10:/srv/nfs /mnt/nfs
Server20:~#
Server20:~# df -Th | grep nfs
192.168.10.10:/srv/nfs
                     nfs4            5.5G    126.9M      5.1G   2% /mnt/nfs

## mount (auto)
Server20:~# cat /etc/fstab | grep nfs
192.168.10.10:/srv/nfs  /mnt/nfs        nfs     defaults        0       0

## file creation and share

#### create files on server2
Server10:~# ls -l /srv/nfs
total 0
Server10:~#
Server10:~# touch /srv/nfs/nfs_test.txt
Server10:~#
Server10:~# ls -l /srv/nfs
total 0
-rw-r--r--    1 root     root             0 Jun  4 16:41 nfs_test.txt

#### confirm from server1
Server20:/etc/samba# ls -l /mnt/nfs
total 0
-rw-r--r--    1 root     root             0 Jun  4 16:41 nfs_test.txt

