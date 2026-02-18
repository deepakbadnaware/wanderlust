FROM node:21
WORKDIR /backend
COPY . .
RUN npm install
COPY .env.sample .env
EXPOSE 8080
CMD ["npm","start"]
