## Auto mount failure

#### Symptoms
- Auto mount failed after starting/rebooting the server, but manual mount (mount -a) worked

#### Investigations
- The netfs service is required for moust Linux servers such as REHL -> The netds was not installed in the server

- For alpine Linux, netmount service is required

- Auto mount succeeded after enabling the netmount service

#### Evidences
Server20:~# rc-service netmount status
 * status: started

Server20:~# rc-status | grep netmount
 netmount                                                          [  started  ]

Server20:~# df -Th | grep nfs
192.168.10.10:/srv/nfs
                     nfs4            5.5G    126.8M      5.1G   2% /mnt/nfs

#### References

https://wiki.alpinelinux.org/wiki/Setting_up_an_NFS_server

https://docs.redhat.com/ja/documentation/red_hat_enterprise_linux/6/html/storage_administration_guide/nfs-clientconfig
