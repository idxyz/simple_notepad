

sudo gedit /etc/systemd/logind.conf


把这一个行的值suspend 修改为ignore

#HandleLidSwitch=suspend

改成这样

HandleLidSwitch=ignore



保存文件以后， 重启Login Manager服务

sudo restart systemd-logind
