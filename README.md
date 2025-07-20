# personal_seafile_cloud

## Общее описание
Личное облачное хранилище на базе Seafile, с обратным прокси Traefik и автоматизацией через Ansible.

## Структура проекта
```
personal-seafile-cloud/
├── playbook.yml
├── inventory.ini
├── roles/
│   ├── docker/
│   │   └── tasks/main.yml
│   ├── traefik/
│   │   ├── files/
│   │   │   └── traefik.yml
│   │   └── tasks/main.yml
│   └── seafile/
│       ├── files/
│       │   └── docker-compose.yml
│       └── tasks/main.yml
├── .gitignore                
└── README.md                  
```

## Основные команды

### 1. Запуск плейбука для проверки соединения с серверами

```aiignore
ansible-playbook -i inventory.yml ping.yml
```

### 2. Запуск основого плейбука по развертыванию seafile и traefik

```aiignore
ansible-playbook -i inventory.yml playbook.yml
```