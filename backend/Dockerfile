FROM node:20-alpine

WORKDIR /app

# Puppeteer
RUN apk add \
    chromium \
    nss \
    freetype \
    harfbuzz \
    ca-certificates \
    ttf-freefont
ENV PUPPETEER_EXECUTABLE_PATH=/usr/bin/chromium-browser

COPY package*.json ./
RUN npm install

COPY . .

CMD ["node", "src/server.js"]