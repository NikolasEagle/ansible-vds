# ansible-vds

Автоматизация настройки k3s кластеров с помощью Ansible.

## 📌 Описание

Данный репозиторий содержит Ansible playbooks и роли для базовой настройки серверов.  
Позволяет быстро развернуть и привести сервер к рабочему состоянию без ручной конфигурации.

Используется подход **Infrastructure as Code (IaC)**.

---

## 🚀 Возможности

- Базовая настройка сервера
- Создание пользователей
- Настройка SSH
- Установка необходимых пакетов
- Подготовка окружения для дальнейшего деплоя
- Идемпотентная конфигурация

---

## 📂 Структура проекта

```
.
├── roles/
├── templates/
├── vds-kz/
├── vds-ru/
├── ansible.cfg
├── hosts.yml
├── k3s-master-kz.yml
└── k3s-master-ru.yml
```

---

## ⚙️ Требования

- Ansible >= 2.9
- Python на целевых серверах
- SSH доступ к серверам

---

## 🔧 Установка

```
git clone https://github.com/NikolasEagle/ansible-vds.git
cd ansible-vds
```

---

## 🔐 Переменные

Основные переменные находятся в:

- vds-kz/vars/
- vds-ru/vars/

---

## 🧪 Проверка

```
ansible-playbook -i hosts.yml k3s-master-kz.yml --check
ansible-playbook -i hosts.yml k3s-master-ru.yml --check
```

---

## 📄 Лицензия

MIT