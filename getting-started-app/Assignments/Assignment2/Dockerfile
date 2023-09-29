FROM node:18-alpine
FROM amazon/aws-cli
WORKDIR /app
COPY . .
RUN yarn install --production
RUN yarn install -g aws-sdk
CMD ["node", "src/index.js"]
EXPOSE 3000