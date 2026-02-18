FROM node:21
WORKDIR /frontend
COPY . .
RUN npm install --ignore-scripts
COPY .env.sample .env.local
EXPOSE 5173
CMD ["npm","run","dev","--","--host"]
