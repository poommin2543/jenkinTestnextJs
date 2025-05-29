# ใช้ Node Alpine เพื่อขนาดเล็ก
FROM node:18-alpine

WORKDIR /app

# copy package.json และ package-lock.json ก่อนเพื่อใช้ cache docker build
COPY package.json package-lock.json ./

RUN npm install

COPY . .

RUN npm run build

EXPOSE 3000

CMD ["npm", "start"]
