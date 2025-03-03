# Install Clickhouse and Vector Ansible Playbook

Плейбук для установки Clickhouse, Vector на одном хосте, ОС Linux использующих пакетный менеджер на базе rpm.

## Конфигурация

Файл конфигурации:
`./group_vars/clickhouse/vars.yml`

Переменные:

`clickhouse_version:` - версия clickhouse
`clickhouse_packages:` - список пакетов для установки

`vector_version:` - версия vector
`vector_architecture:` - системная архитектура пакета vector

## Установка

Запуск плейбука:

```bash
sudo ansible-playbook -i inventory/prod.yml site.yml
```

## Play Tags

clickhouse - Для установки clickhouse

vector - Для установки vector

## Templates:

Файл шаблона:

`./templates/vector.j2`

Файл содержит базовую конфигурацию Vector в формате yaml и устанавливается на целевой хост при запуске плейбука.