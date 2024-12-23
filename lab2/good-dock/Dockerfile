# Указываем версию, чтобы избежать неопределенности
FROM ubuntu:24.04

# Устанавливаем пакеты и очищаем cash для минимизации размера образа
RUN apt-get update && \
    apt-get install nano && \
    rm -rf /var/lib/apt/lists/*

# Создаем пользователя и директорию, назначаем нужные права
RUN useradd -m nginxuser && mkdir -p /app && \
    echo "NormFile" > /app/mybestfile.txt && \
    chown -R nginxuser:nginxuser /app

# Переходим на пользователя с минимальными правами
USER nginxuser
CMD ["sh", "-c", "echo 'Running as user:' $(whoami)"]

