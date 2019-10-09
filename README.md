# React

## Configurações básicas para utilização do React

Pronto para uso de:
 * Imagens
 * CSS
 * Style

### Instalar as bibliotecas

   yarn init -y

   yarn add @babel/core @babel/preset-env @babel/preset-react webpack webpack-cli -D

   yarn add react react-dom

### Criar os arquivos: 

 * babel.config.js
 * webpack.config.js

### Criar a pasta: src

### Instalar a biblioteca

   yarn add babel-loader -D

### Adicionar o script abaixo ao package.json

   "scripts": {
    "build": "webpack --mode development"
   },

### Ir ao terminal e executar 

   yarn build

Será criado um arquivo public/bundle.js 

Que é uma versão tradicional do Javascrip para que funcione em qualquer Browser 

Na mesma pasta criar um arquivo index.html e colocar entre o body

   <script src="./bundle.js"></script>

realizar o teste *Ok!*

### Para colocar alterações aplicáveis automaticamente no servidor

  yarn add webpack-dev-server -D

Adicionar ao arquivo *webpack.config.js* dentro do *module.exports ={*

   devServer: {
    contentBase: path.resolve(__dirname, 'public'),
   },

Altear o arquivo *package.json* de

   "scripts": {
    "build": "webpack --mode development"
  },

para: 

  "scripts": {
    "build": "webpack --mode production",
    "dev": "webpack-dev-server --mode development"
  },

Execute

   yarn dev    -> para executar em desenvolvimento, será gerado um bundle.js legivel

ou 
   yarn build    -> para executar em produção, será gerado um bunble.js mimificado

A segunda mensagem mostra onde o endereço do servidor:
  * http://localhost:8080

Agora quaisquer alterações no */index.js* ou em outros arquivos será refletida automaticamente no servidor.

## Adicionando CSS

    yarn add style-loader css-loader -D

Editar o *webpack.config.js*, adicionando outro loader

## Adicionando importação de imagens

    yarn add file-loader -D

Editar o *webpack.config.js*, adicionando outro loader.

Adicionar a pasta *assets* dentro de src
