# Stage 1

FROM node:20.19.1 AS build
WORKDIR /usr/src/app
COPY backend/package*.json ./
RUN npm install
COPY backend/ .
RUN npm run build

#Stage 2

FROM node:20.19.1
WORKDIR /usr/src/app
COPY --from=build /usr/src/app/dist ./dist
COPY --from=build /usr/src/app/package.json ./package.json
COPY --from=build /usr/src/app/.env ./.env
EXPOSE 8000
CMD ["npm", "start"]

#test workflow 2
