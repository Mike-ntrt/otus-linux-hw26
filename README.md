# Linux HW 26 Network

 В Vagantfile поправил подсеть для роутеров, сделав маску /29  
 Добавил роутеры и серверы, вынес форвадинг и добавление правил iptables в ansible playbook `network.yml`

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
