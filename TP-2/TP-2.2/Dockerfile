FROM node:18-slim AS build
WORKDIR /app
COPY ../TP-1/package*.json ./
RUN npm install --only=production
RUN npm install typescript --save-dev
COPY ../TP-1/ ./
RUN npx tsc index.ts

FROM node:18-slim AS runtime
RUN useradd -m appuser
USER appuser
WORKDIR /app
COPY --from=build /app /app
EXPOSE 4040
CMD ["node", "index.js"]
