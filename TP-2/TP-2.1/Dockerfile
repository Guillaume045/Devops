FROM node:18-slim
WORKDIR /app
COPY ../TP-1/package*.json ./
RUN npm install --only=production
RUN npm install typescript --save-dev
COPY ../TP-1/ ./
RUN npx tsc index.ts
EXPOSE 4040
CMD ["node", "index.js"]