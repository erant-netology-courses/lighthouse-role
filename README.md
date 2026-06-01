# Ansible Role: lighthouse

Установка и настройка Lighthouse — веб-интерфейса для ClickHouse.

## Requirements

- Роль `nginx-lighthouse` (зависимость)
- ОС: Ubuntu 20.04/22.04 или Debian 11/12
- Ansible 2.9+

## Role Variables

| Переменная | Значение по умолчанию | Описание |
|-----------|----------------------|----------|
| `lighthouse_repo` | `https://github.com/VKCOM/lighthouse.git` | URL репозитория Lighthouse |
| `lighthouse_dest` | `/var/www/html/lighthouse` | Путь установки |
| `lighthouse_version` | `master` | Ветка или тег для клонирования |

## Dependencies

- `nginx-lighthouse`

## Example Playbook

```yaml
- name: Install Lighthouse
  hosts: lighthouse
  roles:
    - lighthouse
```

## Inventory

```yaml
lighthouse:
  hosts:
    lighthouse-01:
      ansible_host: 192.168.1.10
      ansible_user: ubuntu
```

## Tags

Теги не заданы.

## License

MIT

## Author

@erant-netology-courses