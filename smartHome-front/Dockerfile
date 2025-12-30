FROM node:18-alpine AS builder
WORKDIR /app
COPY . .
RUN npm run build

FROM nginx:alpine
COPY --from=builder /app/dist/smart-home /usr/share/nginx/html
