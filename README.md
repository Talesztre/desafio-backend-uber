Email Microservice
Uber Backend Challenge

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
[![Licence](https://img.shields.io/github/license/Ileriayo/markdown-badges?style=for-the-badge)](./LICENSE)

Este projeto é um microserviço de API desenvolvido em Java utilizando Spring Boot e AWS Simple Email Service (SES). O microserviço foi criado como parte do Desafio Backend da Uber.

Tabela de Conteúdos
Instalação
Configuração
Uso
Endpoints da API
Contribuindo
Instalação
Clone o repositório:

bash
Copiar código
git clone https://github.com/Talesztre/desafio-backend-uber.git
Instale as dependências com Maven:

bash
Copiar código
mvn clean install
Configure suas credenciais da AWS no arquivo application.properties:

properties
Copiar código
aws.region=us-east-1
aws.accessKeyId=YOUR_ACCESS_KEY_ID
aws.secretKey=YOUR_SECRET_KEY
Uso
Inicie a aplicação com Maven:

bash
Copiar código
mvn spring-boot:run
A API estará acessível em http://localhost:8080.

Endpoints da API
A API fornece os seguintes endpoints:

Enviar Email
POST /api/email/send

Descrição: Envia um e-mail do remetente configurado para o destinatário especificado.

Corpo da Requisição:

json
Copiar código
{
  "to": "destinatario@example.com",
  "subject": "Assunto do Email",
  "body": "Conteúdo do Email"
}
Resposta: Retorna um status indicando o sucesso ou falha do envio.

Contribuindo
Contribuições são bem-vindas! Se você encontrar algum problema ou tiver sugestões de melhorias, sinta-se à vontade para abrir uma issue ou enviar um pull request para o repositório.

Ao contribuir com este projeto, por favor, siga o estilo de código existente, as convenções de commit, e submeta suas mudanças em uma branch separada.
