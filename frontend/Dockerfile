FROM node:18

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm ci

COPY . .
RUN npm run build

CMD ["cp", "-r", "/app/build/.", "/frontend_static/"]
