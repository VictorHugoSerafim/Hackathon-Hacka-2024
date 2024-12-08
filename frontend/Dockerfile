# Usando imagem oficial do Node.js
FROM node:16-alpine

# Definindo diretório de trabalho
WORKDIR /app

# Copiando o package.json e o package-lock.json
COPY package*.json ./

# Instalando dependências do React
RUN npm install

# Copiando o restante do código
COPY . .

# Rodando o build da aplicação React
RUN npm run build

# Servindo a aplicação (usando serve)
RUN npm install -g serve

# Expondo a porta padrão do React
EXPOSE 3000

# Rodando o servidor
CMD ["serve", "-s", "build", "-l", "3000"]