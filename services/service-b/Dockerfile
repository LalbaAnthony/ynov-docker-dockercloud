FROM custom-node:22

WORKDIR /app

COPY package*.json ./
RUN npm ci --omit=dev

COPY src ./src

HEALTHCHECK --interval=10s --timeout=3s --retries=3 \
    CMD curl -f http://localhost:3002/health || exit 1

EXPOSE ${PORT}

CMD ["node", "src/index.js"]
