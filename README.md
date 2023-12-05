# PXC кластер с Vagrant и Ansible
Стенд для настройки Percona XtraDB Cluster

Дистрибутив: Ubuntu 22.04.

Запуск двух машин:

* pxc1: 10.0.26.201
* pxc2: 10.0.26.202
* pxc3: 10.0.26.203

Перед запуском нужно разрешить диапазон адресов 10.0.* для частных сетей.

По умолчанию устанавливается PXC 8.0 из репозиториев Percona.

Основные настройки находятся в файле: provision/roles/mysql/defaults/main.yml

Запуск:

```bash
vagrant up

cd provision
ansible-playbook playbooks/environment.yml

vagrant ssh pxc1
```
