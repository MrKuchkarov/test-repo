# Использование базового образа node:16-alpine
FROM node:16-alpine

# Установка рабочей директории
WORKDIR /home/ilovedocker/app

# Копирование файла hello.sh в рабочую директорию
COPY hello.sh .

# Установка прав на выполнение для hello.sh
RUN chmod +x hello.sh

# Установка команды запуска для контейнера
ENTRYPOINT ["sh", "hello.sh"]
