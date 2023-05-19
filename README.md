
<p align="center">
  Serverless - Funções lambda para emissão de certificado 📰🚀
  <br>
  <br>

  <img alt="Language count" src="https://img.shields.io/github/repo-size/alvarobraz/lambdaCertificate"/>

  <a href="https://rocketseat.com.br">
    <img alt="Made by Rocketseat" src="https://img.shields.io/badge/made%20by-Rocketseat-%237519C1">
  </a>

  <a href="https://www.linkedin.com/in/alvarobraz/">
    <img alt="Made by alvarobraz" src="https://img.shields.io/badge/made%20by-alvarobraz-%237519C1">
  </a>

  <a href="https://github.com/alvarobraz/blog-ig-news/commits/main">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/alvarobraz/lambdaCertificate">
  </a>

  <img alt="License" src="https://img.shields.io/github/license/alvarobraz/lambdaCertificate">
</p>

---

<p align="center">
  <a href="#dart-sobre">Sobre</a> &#xa0; | &#xa0; 
  <a href="#rocket-tecnologias">Tecnologias</a> &#xa0; | &#xa0;
  <a href="#estrutura">Estrutura</a> &#xa0; | &#xa0;
  <a href="#white_check_mark-requerimentos">Requerimentos</a> &#xa0; | &#xa0;
  <a href="#checkered_flag-começando">Começando</a>
</p>

<br>

## :dart: Sobre ##

O projeto lambdaCertificate se trata de funções em Serverless (não servidor), apesar do nome existe um servidor por trás da aplicação, mas não é necessário seu gerenciamento, o próprio provedor faz isso.<br/><br/>
O projeto consiste em uma emissão de um certificado para aluno, os dados vêm de uma tabela NoSQL populada no DynamoDB, implementada em funções lambda na aws, permite upar o certificado em pdf no s3 da aws, projetado para ações que seriam usadas de tempo em tempo sem a necessidade de um servidor rodando full time.<br/><br/>
Forma criadas dois end-points, um apara criação e outro para verificação da existência deste certificado:<br/><br/>
[POST] -https://xgl5kq688b.execute-api.us-east-1.amazonaws.com/dev/generateCertificate<br/>
[GET]  -https://xgl5kq688b.execute-api.us-east-1.amazonaws.com/dev/generateCertificate/{id}
<br>

## :rocket: Tecnologias ##

As seguintes tecnologias foram utilizadas no projeto:

- [TypeScript](https://www.typescriptlang.org/)
- [Node](https://nodejs.org/en/)
- [DynamoDB](https://aws.amazon.com/pt/dynamodb/)
- [s3](https://aws.amazon.com/pt/s3/)
- [Middy](https://fauna.com/)
- [chrome-aws-lambda](https://www.npmjs.com/package/chrome-aws-lambda)
- [dayjs](https://day.js.org/)
- [handlebars](https://handlebarsjs.com/)
- [puppeteer-core](https://www.npmjs.com/package/puppeteer-core)

## :estrutura ##

```
.
├── certificate.pdf
├── package.json
├── package-lock.json
├── README.md
├── serverless.ts
├── src
│   ├── functions
│   │   ├── generateCertificate.ts
│   │   └── verifyCertificate.ts
│   ├── templates
│   │   ├── certificate.hbs
│   │   └── selo.png
│   └── utils
│       └── dynamodbClient.ts
├── tsconfig.json
└── yarn.lock
```

## :white_check_mark: Requerimentos ##

- [Node](https://nodejs.org/en/) >=14.15.0
- [serverless](https://www.npmjs.com/package/serverless)
- [Yarn](https://yarnpkg.com/lang/en/)

## :checkered_flag: Começando ##

```bash
# Clone this project
$ git clone https://github.com/alvarobraz/lambdaCertificate

# Access
$ cd lambdaCertificate

# Install dependencies
$ yarn install

# Run the project
$ yarn dev

# The server will initialize in the <http://localhost:3000>
```