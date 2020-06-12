FROM node:alpine
WORKDIR '/app'
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

FROM nginx

# Exposing port (important to AWS)
EXPOSE 80

# 0 is the index of the node:alpine
COPY --from=0 /app/build /usr/share/nginx/html
