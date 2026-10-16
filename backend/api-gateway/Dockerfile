FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json* yarn.lock* pnpm-lock.yaml* ./
RUN npm ci || npm install
COPY tsconfig.json ./
COPY src ./src
RUN npx tsc -p .
EXPOSE 3000
CMD [ " node\, \dist/index.js\ ]
