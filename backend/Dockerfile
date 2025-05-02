FROM node:20-slim
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm ci --only=production
COPY backend/ ./
EXPOSE 8000
CMD ["npm", "start"]

#test workflow 2
