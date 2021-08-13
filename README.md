# Linux HW 26 Network

 В Vagantfile поправил подсеть для роутеров, сделав маску /29  
 Добавил роутеры и серверы, вынес форвадинг и добавление правил iptables в ansible playbook `network.yml`
 
```
[root@office1Server vagrant]# tracepath -n 8.8.8.8
 1?: [LOCALHOST]                                         pmtu 1500
 1:  192.168.2.1                                           1.387ms
 1:  192.168.2.1                                           1.817ms
 2:  192.168.255.2                                         1.130ms
 3:  192.168.255.1                                         1.795ms asymm  2
 4:  no reply
 5:  no reply
 6:  no reply
 7:  212.1.243.152                                         8.160ms asymm 64
 8:  212.1.251.66                                          5.127ms asymm 63
 9:  72.14.215.172                                         7.352ms asymm 62
...
```

Проект использует pipenv для установки ansible  
Как установить проект:  

```
cd otus-linux-hw26
pip install pipenv
pipenv shell
pipenv install
```

Как запустить проект:
```
vagrant up
ansible-playbook network.yml -v
```
