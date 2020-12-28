From node:14

WORKDIR /app

COPY package.json /app

#RUN npm cache clean

#RUN npm config set proxy

#`RUN npm config set registry http://registry.npmjs.org/

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm","start"]
