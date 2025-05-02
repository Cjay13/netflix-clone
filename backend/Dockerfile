# Stage 1

FROM node:20.19.1 AS build
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install

#Stage 2

FROM node:20.19.1
WORKDIR /usr/src/app
COPY --from=build /usr/src/app ./
EXPOSE 8000
CMD ["npm", "start"]

#test workflow 2
