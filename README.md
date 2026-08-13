# Ansible disk migration

Проект отвечает за шаги внутри Ubuntu после того, как новый диск уже создан и прикреплён к ВМ.

## Зависимости

Python-пакеты:
```bash
pip install -r requirements.txt
```

Ansible collections:
```bash
ansible-galaxy collection install -r requirements.yml
```

## Запуск
```bash
ansible-playbook playbooks/migrate_disk.yml -k -K
```

Перед запуском проверьте `inventory.ini`, `new_disk`, точки монтирования и список сервисов, которые необходимо не останавливать.
