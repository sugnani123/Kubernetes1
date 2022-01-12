#  FROM node:8

# WORKDIR /usr/src/app

# COPY package*.json ./
# RUN npm ci --only=production

# COPY . .

# EXPOSE 8080
# CMD [ "npm", "start" ] #

FROM node:12-alpine
RUN apk add --no-cache python2 g++ make
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
