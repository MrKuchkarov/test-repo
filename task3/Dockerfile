# Использование базового образа node:16-alpine
FROM node:16-alpine

# Установка рабочей директории
WORKDIR /home/ilovedocker/app

# Копирование файлов package.json и package-lock.json из поддиректории packages в рабочую директорию
COPY packages/package*.json ./

# Установка зависимостей
RUN npm install --omit=dev

# Копирование исходников проекта из поддиректории src в рабочую директорию
COPY src .

# Экспозируемый порт
EXPOSE 3032

# Команда запуска
CMD ["node", "main.js"]
