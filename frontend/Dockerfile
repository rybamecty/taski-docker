FROM node:18

WORKDIR /app

COPY package.json package.json
COPY package-lock.json package-lock.json

RUN npm install

COPY . .
RUN npm run build

# Запуск встроенного сервера для раздачи статики
CMD ["npx", "-y", "http-server", "-p", "8000", "/app/build"]
