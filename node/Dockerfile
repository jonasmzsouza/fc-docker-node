FROM node:22

WORKDIR /usr/src/app

# Instala dockerize
RUN apt-get update \
  && apt-get install -y wget \
  && wget https://github.com/jwilder/dockerize/releases/download/v0.6.1/dockerize-linux-amd64-v0.6.1.tar.gz \
  && tar -C /usr/local/bin -xzvf dockerize-linux-amd64-v0.6.1.tar.gz \
  && rm dockerize-linux-amd64-v0.6.1.tar.gz

# Copia apenas os arquivos de dependências primeiro
COPY package*.json ./

# Instala as dependências
RUN npm install

# Copia o restante dos arquivos
COPY . .

EXPOSE 3000

CMD ["node", "index.js"]
