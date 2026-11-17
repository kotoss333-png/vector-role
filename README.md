# vector-role

Ansible-роль для установки и базовой настройки Vector.

## Требования

- Целевая ОС: CentOS / Rocky Linux / RHEL (x86_64).
- Установленный Ansible версии 2.12 и выше.

## Переменные роли

### Переменные по умолчанию (`defaults/main.yml`)

| Переменная | Значение по умолчанию | Описание |
| :--- | :--- | :--- |
| `vector_version` | `"0.34.0"` | Версия устанавливаемого пакета Vector |
| `vector_config_dir` | `"/etc/vector"` | Директория хранения конфигурационного файла |
| `vector_data_dir` | `"/var/lib/vector"` | Рабочая директория данных Vector |
| `clickhouse_host` | `"clickhouse-01"` | Хост или IP-адрес сервера ClickHouse для отправки логов |

### Внутренние переменные (`vars/main.yml`)

| Переменная | Описание |
| :--- | :--- |
| `vector_url` | Прямая ссылка на скачивание `.rpm` дистрибутива Vector |

## Пример использования

```yaml
---
- name: Install Vector
  hosts: vector
  roles:
    - vector-role
```

## Лицензия

MIT
