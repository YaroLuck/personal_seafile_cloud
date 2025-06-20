# personal_seafile_cloud

## Общее описание
Личное облачное хранилище на базе Seafile, с обратным прокси Traefik и автоматизацией через Ansible.

## Структура проекта
```
personal-seafile-cloud/
│
├── ansible/                  # Ansible-скрипты
│   ├── inventory.ini          # Ansible-инвентарь
│   ├── playbook.yml           # Основной плейбук
│   └── roles/
│       └── setup-docker/     # Роль установки Docker, Compose и развёртки
│
├── docker/                   # Docker-файлы
│   ├── docker-compose.yml     # Основной compose файл
│   ├── .env                   # Переменные окружения
│   └── data/
│       └── traefik/           # Конфиги Traefik
│            └── acme.json    # Хранение сертификатов Let's Encrypt
│
├── scripts/                   # Вспомогательные скрипты (backup.sh, restore.sh и т.д.)
├── .gitignore                
└── README.md                  
```
