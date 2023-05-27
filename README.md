# netology-ansible-02
homework
### Этот плейбук работает в окружении `Docker`. Он устанавливает в подготовленные контейнера:
- clickhouse версии "22.3.3.44"
- vector версии "0.29.1"

Для запуска плейбука нобходимо загрузить 2 контейнера с образом CentOS-7, можно использовать команду 
```bash
sudo docker run --name clickhouse -d pycontribs/centos:7 sleep infinity && sudo docker run --name vector -d pycontribs/centos:7 sleep infinity
``` 
Затем, для запусуа плейбука, можно воспользоватся следующей командой:
```bash
sudo ansible-playbook -i inventory/prod.yml site.yml
``` 
