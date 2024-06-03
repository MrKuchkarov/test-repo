FROM node:16-alpine

# создание директории приложения
WORKDIR /usr/src/app

# установка зависимостей
# астериск ("*") по возможности скопирует оба файла: package.json и package-lock.json
# тот же символ делает копирование опциональным, т. е. без файла сборка не упадёт
COPY package*.json ./

# Очистка кэша и установка зависимостей
RUN npm cache clean --force && npm install --omit=dev

# копируем исходный код
COPY . .

EXPOSE 3000
CMD [ "node", "index.js" ]
