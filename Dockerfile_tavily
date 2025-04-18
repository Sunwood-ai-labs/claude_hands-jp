FROM node:22.12-alpine AS builder

WORKDIR /app
COPY tavily-mcp/package*.json ./
RUN npm install
COPY tavily-mcp/build ./build

FROM node:22-alpine AS release

WORKDIR /app
COPY --from=builder /app/build /app/build
COPY --from=builder /app/package.json /app/package.json
COPY --from=builder /app/package-lock.json /app/package-lock.json

ENV NODE_ENV=production

RUN npm ci --ignore-scripts --omit-dev

ENTRYPOINT ["node", "build/index.js"]
