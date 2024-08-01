#Usar a imagem base do NodeJS
FROM node:18-alpine

#Definir o diretório de trabalho dentro do container
WORKDIR /app

#Copiar o package.json para o diretório de trabalho
COPY package*.json ./

#Instalando as dependências do projeto
RUN npm install

#Copie todos os arquivos do projeto para o diretorio de trabalho
COPY . .

#Construir o projeto (build)
RUN npm run build

#Definir a posta do servidor
EXPOSE 3000

#Inicializar a aplicação
CMD ["npm", "start"]

