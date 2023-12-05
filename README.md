# vagrant-mysql-repl
Стенд для настройки репликации MySQL

Дистрибутив: Ubuntu 22.04.

Запуск двух машин:

* mysql1: 10.0.26.101
* mysql2: 10.0.26.102

Перед запуском нужно разрешить диапазон адресов 10.0.* для частных сетей.

По умолчанию устанавливается Percona Server for MySQL 8.0 из репозиториев Percona.

Основные настройки находятся в файле: provision/roles/mysql/defaults/main.yml

Запуск:

```bash
vagrant up

cd provision
ansible-playbook playbooks/environment.yml

vagrant ssh mysql1
```
