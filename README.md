# myRPC: Remote Procedure Call System
**Система удалённого выполнения команд через сокеты с авторизацией пользователей**

## Назначение
Система позволяет:
- Выполнять Bash-команды на удалённом сервере;
- Контролировать доступ через конфигурационные файлы;
- Логировать операции через `libmysyslog`;
- Поддерживает текстовый и JSON-форматы сообщений.

## Установка
### Из deb-пакетов:
```bash
# На сервере
sudo apt install ./deb/myrpc-server.deb
```

```bash
# На клиенте
sudo apt install ./deb/myrpc-client.deb
```

## Запуск сервера:
```bash
myrpc-server -c /etc/myRPC/myRPC.conf
```
## Пример вызова команды с клиента:
```bash
myrpc-client -h 192.168.1.10 -p 1234 -s -c "ls -la"
```

