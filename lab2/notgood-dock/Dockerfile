# Не крутая практика 1: Использование latest-тега
FROM ubuntu:latest

# Не крутая практика 2: Многоступенчатая установка пакетов без очистки кеша
RUN apt-get update && apt-get install nano

# Не крутая практика 3: Запуск от пользователя root
RUN mkdir /app && echo "NotGoooodFile" > /app/badfile.txt

CMD ["sh", "-c", "echo 'Running as user:' $(whoami)"]
