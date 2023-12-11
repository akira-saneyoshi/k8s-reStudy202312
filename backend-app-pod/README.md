docker run \
  -e MONGODB_USERNAME="user" \
  -e MONGODB_PASSWORD="welcome" \
  -e MONGODB_HOSTS="172.21.113.109:32717" \
  -e MONGODB_DATABASE="weblog" \
  -d \
  -p 8080:3000 \
  weblog-app:v1.0.0

※1：MONGODB_HOSTSは、UbuntuのIPアドレスを記載する。
　　　saneyoshi@LAPTOP-IOE8NK0E:~$ ip addr show
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP group default qlen 1000
    link/ether 00:15:5d:e8:df:06 brd ff:ff:ff:ff:ff:ff
    inet 172.21.113.109/20 brd 172.21.127.255 scope global eth0
       valid_lft forever preferred_lft forever
    inet6 fe80::215:5dff:fee8:df06/64 scope link
       valid_lft forever preferred_lft forever