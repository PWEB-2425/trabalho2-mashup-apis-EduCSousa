API Mashup - Trabalho #2

Autores: Eduardo Sousa (nº 31658) e Rui Miranda (nº 31803)

Descrição: Aplicação web que integra dados de múltiplas APIs externas (OpenWeatherMap e Wikipedia) com autenticação segura e histórico de pesquisas por utilizador.

Funcionalidades:
-Sistema de autenticação (registo/login)
-Pesquisa unificada que combina dados climáticos e informações da Wikipedia
-Histórico persistente em MongoDB
-Interface moderna e responsiva

Tecnologias:
-Frontend: HTML5, CSS3, EJS
-Backend: Node.js, Express, Passport.js
-BD: MongoDB (Mongoose)
-APIs: OpenWeatherMap + Wikipedia REST API

Link de Deployment: https://mashup-api-app.onrender.com/login

Instalação:
-git clone https://github.com/PWEB-2425/trabalho2-mashup-apis-EduCSousa.git
-npm install
-Criar ficheiro .env com:

text
MONGODB_URI=[string_de_conexão]  
OPENWEATHER_API_KEY=[chave]  
WIKIPEDIA_API_KEY=[chave]  
SESSION_SECRET=[segredo]  
npm start

Base de Dados:
-Coleção users armazena:
-Credenciais (username + password hashed)
-Array searches com termos e timestamps

Autenticação:
-Passport-local com sessões persistentes
-Passwords hasheadas com bcrypt
-Middleware protege rotas privadas

Fluxo:
-Utilizador autentica-se
-Pesquisa termo (ex: "Porto")

Servidor consulta:
-Clima (OpenWeatherMap)
-Resumo (Wikipedia)
-Resultados combinados + histórico atualizado

Dependências: express, mongoose, passport, axios, ejs, dotenv, express-session, connect-mongo.

Segurança:
-Variáveis sensíveis em .env
-Sanitização de inputs
-HTTPS em produção

