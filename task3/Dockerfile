FROM node:16-alpine
# Задаем рабочую директорию
WORKDIR /home/ilovedocker/app
# Убираем копирование hello.sh
#COPY hello.sh .
COPY packages/package*.json src/* ./
RUN npm i --omit=dev
COPY src/* ./
# Экспозим порт 3032
EXPOSE 3032
# Убираем старую команду
ENTRYPOINT [ "node","main.js"]
