<img src="https://res.cloudinary.com/practicaldev/image/fetch/s--nTfuVZvi--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/4qa1g2dsx1hre7hjjlze.png">

# Ignite Desafio 01 trilha node.js

<p align="center">
<img src="https://img.shields.io/github/license/BrunoSSantana/desafio02-trilha-node.js" />
<img src="https://img.shields.io/github/last-commit/BrunoSSantana/desafio02-trilha-node.js" />
</p>

---
### Sumário
 <details>
  <summary>CHAPTER I</summary>
 
  * [Aula I - Introdção](#aula-i)
  * [Aula II - Conceito do Node](#aula-ii)
  * [Aula III](#aula-ii)
  * [Aula IV](#aula-iv)
  * [Aula V](#aula-v)
  * [Aula VI](#aula-vi)
  * [Aula VII](#aula-vii)
  * [Aula VIII](#aula-viii)
  * [Aula IX](#aula-ix)
  * [Aula X](#aula-x)
  * [Aula XI](#aula-xi)
  * [Aula XII](#aula-xii)
  * [Aula XIII](#aula-xiii)
  * [Aula XIV](#aula-xiv)
  * [Aula XV](#aula-xv)
  * [Aula XVI](#aula-xvi)
  * [Aula XVII](#aula-xvii)
  * [Aula XVIII](#aula-xviii)
  * [Aula XIX](#aula-xix)
  * [Aula XX](#aula-xx)
</details>
<details>
 <summary>DESAFIOS I</summary>

 - [Desafio I: Conceitos do Node.js](https://github.com/BrunoSSantana/desafio01-trilha-node.js/)
 - [Desafio II: Trabalhando com Middlewares](https://github.com/BrunoSSantana/desafio02-trilha-node.js/)
 - [Desafio III: Corrigindo o código](https://github.com/BrunoSSantana/desafio03-trilha-node.js/)
</details>
<details>
 <summary>CHAPTER II</summary>
 
  * [Aula XXI](#aula-xxi)
  * [Aula XXII](#aula-xxii)
  * [Aula XXIII](#aula-xxiii)
  * [Aula XXIV](#aula-xxiv)
  * [Aula XXV](#aula-xxv)
  * [Aula XXVI](#aula-xxvi)
  * [Aula XXVII](#aula-xxvii)
  * [Aula XXVIII](#aula-xxviii)
  * [Aula XXIX](#aula-xxix)
  * [Aula XXX](#aula-xxx)
  * [Aula XXXI](#aula-xxxi)
  * [Aula XXXII](#aula-xxxii)
  * [Aula XXXIII](#aula-xxxiii)
  * [Aula XXXIV](#aula-xxxiv)
  * [Aula XXXV](#aula-xxxv)

</details>

<details>
 <summary>DESAFIOS II</summary>

 - [Desafio IV: Conceitos do Node.js](https://github.com/BrunoSSantana/desafio04-trilha-node.js/)
</details>

### Projetos Criados
- [RENTALX](https://github.com/BrunoSSantana/rentalx)

---

## CHAPTER I
  
  ## Aula I
  > Introdução

Assuntos aboradados:
* Node.js
* API
* API REST
* Status Code
* Métodos de Requisição HTTP
* Middleware

## Aula II
> Conceitos do Node

O que é o Node.js? è uma plataforma open-source que permite o Javascript rodar no servidor.
O que torna o Node.js tão poderoso?
* [V8](https://v8.dev/)
* [libuv](https://nodejs.org/en/docs/meta/topics/dependencies/#libuv)
* [Conjunto de Módulos](https://nodejs.org/en/docs/meta/topics/dependencies/)

Características
* Bseado em eventos 
* Single Thread
* Non-blocking I/O
* Módulos próprios: http, dns, fs, buffer

Gerenciadores de Pacote
* [npm](https://www.npmjs.com/)
* [yarn](https://yarnpkg.com/)

Frameworks
* [Express](https://expressjs.com/)
* [Egg.js](https://eggjs.org/)
* [Nest.js](https://nestjs.com/)
* [Adois.js](https://adonisjs.com/)

## Aula III
> Conceitos Sobre API REST

**API**

O acrônimo API que provém do inglês Application Programming Interface (Interface de Programação de Aplicações), nada mais é um estilo de arquitetura, ou seja, uma série de restrições que devem ser seguidas no processo de criação de um web service, com a finalidade de que outras aplicações consigam utilizar as funcionalidades desta aplicação, sem precisar conhecer detalhes da implementação da mesma.

**REST**

REST significa Representational State Transfer (Transferência de Estado Representacional), consistido de princípios/regras/constraints que, quando seguidas, permitem a criação de um projeto com interfaces bem definidas. Desta forma, permitindo, por exemplo, que aplicações se comuniquem.  **RESTful**  seria, então, a API que está de acordo com todas as restrições:

* Ter uma arquitetura cliente/servidor formada por clientes, servidores e recursos, com solicitações gerenciadas por meio de HTTP.
* Estabelecer uma comunicação stateless entre cliente e servidor. Isso significa que nenhuma informação do cliente é armazenada entre solicitações GET e toda as solicitações são separadas e desconectadas.
* Armazenar dados em cache para otimizar as interações entre cliente e servidor.
* Ter uma interface uniforme entre os componentes para que as informações sejam transferidas em um formato padronizado. Para tanto, é necessário que:
  * os recursos solicitados sejam identificáveis e estejam separados das representações enviadas ao cliente;
  * os recursos possam ser manipulados pelo cliente por meio da representação recebida com informações suficientes para tais ações;
  * as mensagens autodescritivas retornadas ao cliente contenham informações suficientes para descrever como processá-las;
  * hipertexto e hipermídia estão disponíveis. Isso significa que após acessar um recurso, o cliente pode usar hiperlinks para encontrar todas as demais ações disponíveis para ele no momento.
* Ter um sistema em camadas que organiza os tipos de servidores (responsáveis pela segurança, pelo carregamento de carga e assim por diante) envolvidos na recuperação das informações solicitadas em hierarquias que o cliente não pode ver.
* Possibilitar código sob demanda (opcional): a capacidade de enviar um código executável do servidor para o cliente quando solicitado para ampliar a funcionalidade disponível ao cliente.

## Aula IV
> Métodos de Requisição HTTP

 ### Métodos HTTP aborados no curso:
* **GET** - Leitura - O método GET solicita a representação de um recurso específico. Requisições utilizando o método GET devem retornar apenas dados.
* **POST** - Criação - O método POST é utilizado para submeter uma entidade a um recurso específico, frequentemente causando uma mudança no estado do recurso ou efeitos colaterais no servidor.
* **PUT** - Atualização - O método PUT substitui todas as atuais representações do recurso de destino pela carga de dados da requisição.
* **DELETE** - Deleção - O método DELETE remove um recurso específico.
* **PATCH** - Atualização parcial - O método PATCH é utilizado para aplicar modificações parciais em um recurso.


[Referência](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods)

### HTTP Code
![](https://miro.medium.com/max/920/1*w_iicbG7L3xEQTArjHUS6g.jpeg)

## Aula V
> Criando a Estrutura do Projeto

* Criar pasta `mkdir Projeto`
* Iniciar projeto `yarn init -y`
* Escolher Framework => Express `yarn add express`
* Criar na raiz a pasta src/ e o arquivo src/index.js
```javascript
const express = require('express');
const app = express();
app.listen(3000)
```
* Executar arquivo => node caminho/arquivo.js `node src/index.js`
* Rotas
```javascript
app.get("/", (request, response) => {
  return reponse.json({})
})
```

## Aula VI
> Adicionado o Nodemon na aplicação
 
Para que serve? Agilizar o processo para evitar de reestartar automaticamente após alterar o código.

Instalação:
```bash
yarn add nodemon -D
```
a flag `-D` singnifica será instalada como dependência de desenvolvimento já que só precisaremos para precisaremos durante o desenvolvimento.

## Aula VII
> Utilizando os Métodos HTTP

#### Exemplos

GET:
```javascript
app.get("/courses", (request, response) => {
    return response.json(courses);
});
```
POST:
```javascript
app.post("/aula", (request, response) => {
    const { student } = request.headers;
    const { duration, educator } = request.body;

    const aula = {
        duration,
        educador,
        student_name
    }
    customer.aulas.push(aula)
    
    return response.status(201).send();  
});
```
PUT:
```javascript
app.put("/aula", checkStudent (request, response) => {
    const { student } = request;
    const { educator, duration } = request.body;

    student = {
      educator,
      duration
    }
    aulas.push(student)

    return response.status(201).send();
});
```
PATCH:
```javascript
app.put("/student", checkStudent (request, response) => {
    const { student } = request;
    const { newName } = request.body;

    student.student_name = newName
    aulas.push(student)

    return response.status(201).send();
});
```
DELETE:
```javascript
app.delete("/account", checkStudent, (request, response) => {
    const { student } = request;

    aulas.splice(student, 1);

    return response.status(200).json(aulas);
})
```

## Aula VIII
> Utilizando o Insomnia

Para que serve?
O Insomnia é uma ferramenta para auxiliar a criação de api, onde cria requisições HTTP afim de testar o código. 
[Download](https://insomnia.rest/download)
Alternativas:
* [Postman](https://www.postman.com/)
* [Hoppscotch](https://hoppscotch.io/)

Setar URl => No Enviroment / Manage Enviroments / `{"baseURL": "http://localhost:3000"}`
Adicionar Requisição => New Request / Selecionar método

## Aula IX
> Parâmetros da Requisição

* Headers Params
* Query Params
  * ? => iniador da query
  * chave=valor
  * & => separador
* Route Params
* Body Params


## Aula X
> Conhecendo os requisitos da aplicação

REQUISITOS:
- [X] Criar uma conta
- [X] Buscar o extrato bancário
- [X] Realizar um depósito
- [X] Realizar um saque
- [X] Buscar o extrato bancário do cliente por data
- [X] Atualizar dados da conta do cliente
- [X] Obter dados da conta do cliente
- [X] Deletar uma conta

REGRAS DE NEGÓCIO:
- [X] Não poder cadastrar uma conta com
- [X] Não poder fazer depósito em uma conta não existente
- [X] Não poder buscar extrato em uma conta que não existe
- [X] Não poder fazer saque em uma conta não existente
- [X] Não poder excluir uma conta não existente
- [X] Não poder fazer saque quando o saldo for insuficiente

## Aula XI
> Cadastro de conta

* Criar array 'customers'
* Dados que no body: CPF, name
* Dados da conta:
 * CPF: string
 * name: string
 * statement: array
 * id: uuid

```javascript
app.post("/account", (request, response) => {
    const {cpf, name} = request.body;

    customers.push({
        cpf,
        name,
        id: uuid(),
        statement: []
    })

    return response.status(201).send();
});
```

## Aula XII
> Validando CPF existente

```javascript
 const customerAlreadyExists = customers.some((customer) => customer.cpf === cpf);

 if (customerAlreadyExists) {
     return response.status(400).json({ error: "Customer Already Exists" });
 }
```

## Aula XIII
> Listando extrato

```javascript
 const customer = customers.find(customer => customer.cpf === cpf);
 return response.json(customer.statement);
```

## Aula XIV
> Validando conta
 
```javascript
    const { cpf } = request.headers

    const customer = customers.find(customer => customer.cpf === cpf);

    if (!customer) {
        return response.status(401).json({error: "Customer not found!"});
    }
```

## Aula XV
> Middlewares

Função que age entre o request e o reponse. No express, necessariamente precisam ser passados 3 parâmetros: request, response e next.
```javascript
function userExists(request, response, next) {
    const { cpf } = request.headers

    const customer = customers.find(customer => customer.cpf === cpf);

    if (!customer) {
        return response.status(401).json({error: "Customer not found!"});
    }

    request.customer = customer;

    return next();
}
```
Existem e maneiras principais de usar middlewares com express
1. Declarando a função passando ela no `app.use(nome do middleware)`
2. Declarando a função e passando ela dentro do método de roteamento
```javascript
app.get("/statement", userExists, (request, response) => {
    return response.json(customers);
});
```

## Aula XVI
> Criando depósito na conta

```javascript
app.post("/deposit", userExists, (request, response) => {
    const { customer } = request;
    const { amount, description } = request.body;

    const deposit = {
        amount,
        description,
        type: "credit",
        created_at: new Date()
    }

    customer.statement.push(deposit)

    return response.status(201).send();

    
});
```

## Aula XXVII
> Criando saque na conta

```javascript

app.post("/withdraw", userExists, (request, response) => {
    const { customer } = request;
    const { amount } = request.body;

    const balance = getBalance(customer.statement);

    if (balance<=amount) {
        return response.status(400).json({error: "Saldo insuficiente"})
    }

    const deposit = {
        amount,
        type: "debit",
        created_at: new Date()
    }

    customer.statement.push(deposit)

    return response.status(201).send();

});
```

## Aula XVIII
> Listar extrato bancário por data

```javascript
app.get("/statement/:date", userExists, (request, response) => {
    const { customer } = request;
    const { date } = request.query;

    const dateFormat = new Date( date + " 00:00");

    const statement = customer.statement.filter((statement) => statement.created_at.toDateString() === new Date(dateFormat).toDateString());

    return response.json({statement})
});
```

## Aula XIX
> Atualizar conta

```javascript
app.put("/account", userExists, (request, response) => {
    const { customer } = request;
    const { name } = request.body;

    customer.name = name;

    return response.status(201).send();
});
```

## Aula XX
> Remover conta

```javascript
app.delete("/account", userExists, (request, response) => {
    const { customer } = request;

    customers.splice(customer, 1);

    return response.status(200).json(customers);
});
```

## CHAPTER II

## Aula XXI
> Introdução

Nesse capítulo será desenvolvido uma API de aluguel de carros onde iremos trabalhar nessa API com o typescript explicar pq usá-lo, como usá-lo. Na nossa API faremos cadastros de usuários, alugueis, carros e suas especificações com o intuito de construir um sistema de busca, além de abordar o streming do node e seus módulos, introdução a SOLID (princípios de programação orientada a objeto), arquitetura limpa, melhorar a escrita e a qualidade do código afim de facilitar o entendimento e sua manutenção além da criação de uma documentação com utilização de ferramentas.

## Aula XXII
> Introdução ao Typescript

* Superset  do Javascript open-source criada pelo time da Microsoft
* Definido como Estaticamente Tipada
* Ter um controle melhor sobre o tipo de parâmetros a serem passados nas funções e um melhor controle de forma geral na aplicação, diminuindo a chance de erros futuramente
* A ideia do Typescript é complementar o Javascript e não substituílo
* Não é necessário tipar todas as variáveis (porém recomenda-se e tipe ao máximo já que estamos usando esse super set pra isso)
* Auxilia a desenvolvimento

## Aula XXIII
> Criando Projeto com Typescript

Agora vamos iniciar a desenvolver a [API RENTALX](https://github.com/BrunoSSantana/rentalx)


- [x] Criar Pasta
- [x] `yarn init -y`
- [x] `mkdir src/`
- [x] `touch src/server.ts`
- [x] `yarn add express`

### Importando dependências

Com Javascript:
```javascript
const express = require('express');
```

Com Typescript:
```typescript
import express from 'express';
```

### Adicionando Tipagens do express

Com o Typescript a depedêcia requer mais uma dependência afim de tipar e ajudar no intellisense. Para tal, efetuamos o comando a seguir:
```bash
yarn add @types/express -D
```
> lembrando que a flag `-D` significa que será instalada como dependência de desenvolvimento, já que só utilizamos o typescript em ambiente de desenvolviment.

### Criando a primeira rota

```typescript
const app = express(); // chamando express
app.get("/", (request, response) => {
    return response.json({message: "Hello, World"})
}); // modelo de rota com express
app.listen(3333) // porta onde será ouvido nosso servidor
```

Por padrão atualmente, o node não reonhece a syntaxe de import/export, para isso é preciso que esse código seja convetido de alguma forma em javascript para que ela possa ser executado. Para isso, primeiramente nós instalamos a dependência do typescript e seguimos os seguinte passos:

- Instalando Typescript :arrow_right: `yarn add typescript -D`
- Iniciando o typescript :arrow_right: `yarn tsc --init`
- Em tsconfig.json, setamos :arrow_right: ` "outDir": "./dist"`
- Convertendo para Js :arrow_right:`yarn tsc`
- Executando arquivo criado :arrow_right: `node dist/server.js`

## Aula XXIV
> Adicionando os Tipos

Vamos iniciar criando dois arquivos na pasta src:

```bash
touch src/routes.ts src/CreateCoursesService.ts
```
Nos arquivos criados, vamos como adicionar tipagens. Como em tantas outras linguagens de programação, nós definimos que tipo dedado (string, number, boolean...) determinada função irá receber. Podendo no Typescript ser feito esse procedimento de duas formas como veremos. 

CreateCoursesService.ts:
```typescript
class CreateCoursesService {
    execute(name: string, duration: number, educator: string) {

    }
}

export default new CreateCoursesService;
```
> Dessa forma, os parâmetros vão ter por obrigação serem passados para função nessa ordem ou dará erro.

```typescript
interface ICourse {
    name: string;
    duration: number;
    educator: string;
}

class CreateCoursesService {
    execute({name, duration, educator}: ICourse) {

    }
}

export default new CreateCoursesService;
```
> Os parâmetros não precisarão serem passados para função nessa mesma ordem.

routes.ts:
```typescript
import { Request, Response } from 'express';
import CreateCoursesService from './CreateCoursesService';

export function createCourse(request: Request, response: Response) {
    CreateCoursesService.execute("NodeJS", 10, "Dani");

    return response.send();
}
```
server.ts:
```typescript
app.get("/", createCourse);
```
Para verificar executar o código criado precisamos dos seguinte comandos:
```bash
yarn tsc
node dist/server.js
```

Aqui vamos importar o Request e o Response do express já que não está dentro o módulo de rotas.
```typescript
import { Request, Response } from 'express';
import CreateCoursesService from './CreateCoursesService';

export function createCourse(request: Request, response: Response) {
    CreateCoursesService.execute({
        name: "NodeJS", 
        duration: 10,
        educator: "Dani"
    });

    return response.send();
}
```
e aqui vamos verificar se está funcionando com os seguintes comandos:
```bash
yarn tsc
node dist/server.js
```

## Aula XXV
> Definindo os parâmetos obrigatórios

Para definir quais parâmetros serão obrigatórios, temos que definir primeiro qais serão opicionais opicionais, para isso pasta utilizar `?` após o nome do parâmetro e antes do `:` na interface, como é mostrado a seguir.
```typescript
interface ICourse {
    name: string;
    duration?: number;
    educator: string;
}
```

Com o Typescript assim como no Javascript, podemos definir o valor default (padrão), como por exemplo:
```javascript
class CreateCoursesService {
    execute({name, duration = 8, educator}: ICourse) {

    }
}
```

## Aula XXVI
> Configurando ts-node-dev

- Iniciar aplicação rentalx
```bash
yarn init -y
yarn add express
yarn add @types/express -D
yarn add typescript -D
yarn tsc --init
yarn ts-node-dev -D
```
- Adicionar script no package.json
```bash
"scripts": {
    "dev": "ts-node-dev --transpile-only --ignore-watch node-modules --respawn src/server.ts"
},
```
- Padronização de código com [eslint](https://www.youtube.com/watch?v=rCeGfFk-uCk&t=1935s) e prettier
- Desabilitar no `tsconfig.json` a conf `strict`
- Testar rota
```typescript
import express from "express";

const app = express();

app.get("/", (request, response) => {
  return response.json({ message: "Hello World" });
});

app.listen(3333, () => console.log("Server is running"));
```
## Aula XXVII
> Debugando aplicação

O uso do `console.log` apesar de funcionar muitas vezes para ajudar achar o erro na aplicaão, muitas vezes não é o mais rápido e eficiente. Afim de agilizar o nosso processo vamos começar a utilizar a ferramenta de debug do vscode. No lado esquerdo da tela, próimo ao eplorador do vscode, vamos abrir a seção de executar e depurar e clicar na opção de "create a launch.json file" e selecionar a opção de Node.js
```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "attach",
      "name": "Launch Program",
      "skipFiles": ["<node_internals>/**"],
      "outFiles": ["${workspaceFolder}/**/*.js"]
    }
  ]
}
```
Após feito a configuração podemos rodar o comando `yarn dev` selecionar o break point e clicar no botão de :arrow_forward: do depurador. É possível observar as variáveis presentens no processo adicionando-as precionando o botão de :heavy_plus_sign: .

## Aula XXVIII
> Criando Categoria

O diagrama abaixo represata de como iremos montar nossa aplicação com as tabelas que iremos criar

![##table](https://xesque.rocketseat.dev/1571029149847-attachment.png)

Agora iremos iniciar trabalhando nas nossas rotas. Para isso, dentro da pastas `src` vamos criar outro diretório chamado `routes` e dentro criar um arquivo `categorias.routes.ts` onde iremos importar o `Router` do `express`, em seguida guardamos o  `Router` em uma const (de preferência que faça referência ao tipo da rota por exemplo, `categoriesRoutes`) para fazermos a criação de nossas rotas e exportamos ela no fim do arquivo.

**Exemplo de Rota criada:**

```typescript
import { Router } from "express";

const categoriesRoutes = Router();

const categories = [];

categoriesRoutes.post("/", (request, response) => { // apenas "/" pois iremos passar o "/categories" junto ao nosso middleware
  const { name, description } = request.body;

  categories.push({
    name,
    description,
  });

  return response.status(201).send(); //.send() obrigatório sempre que n for passando um json ou algo do tipo
});

export { categoriesRoutes };

```

Para podermos usar as rotas criadas neste arquivo precisamos fazer duas coisas importar no arquivo `server.ts` e dar use => `app.use("/categoris",categoriesRoutes)`, onde o primeiro termo passado no nosso middleware significa a rota que sempre irá fazer. agora podemos verificar se está tudo rodando corretamente.

## Aula XXIX
> Inserindo Id com uuid

Para criarmos nossos id por motivos de segurança simulando o que ocorre normalemnte no cenário real, iremos utilizar o formato uuid que nada mais é que um Identificador Único Universal. Assim, iremos utilizar a biblioteca uuid na qual conta com algumas opções de formatos do uuid, escolheremos a v4 que gera a chave a partir de números aleatórios.
```bash
yarn add uuid
```

## Aula XXX
> Inserindo Tipagem para Categoria

Afim de criar uma estrutura de dados que serão passados no `POST/categories` vamos criar justamente um modelo que nossa categoria irá ter. Dessa forma, na pasta `src/` vamos criar outro diretório, `model` e nele criar um arquivo chamado `Category.ts`, onde vamos criar a seguinte estrutura, utilizando-se das funciolidades de tipagem do typescript:
```typescript
import { v4 as uuidv4 } from "uuid"; // importando a lib uuid

class Category { // criando o objeto/modelo
  id?: string; // o caractere '?' indica que é opicional
  name: string; //usamos as tipagens do typescript
  description: string;
  created_at: Date;

  constructor() { // o constructor é semelhante a um método que só é cahmado apenas quando o objeto é instânciado 
    if (!this.id) {
      this.id = uuidv4();
    }
  }
}

export { Category };
```

E agora, no arquivo `categories.routes.ts`, na criação das rotas vamos utilizar esse objeto como um tipo, como no exemplo da criação de uma rota:
```typescript
categoriesRoutes.post("/", (request, response) => {
  const { name, description } = request.body;

  const category = new Category(); // instanciando o objeto

  Object.assign(category, { // Utilizando esta função passamos como primeiro parâmetro o objeto e como segundo parâmetro os atributos.
    name,
    description,
    created_at: new Date(),
  });

  categories.push(category);

  return response.status(201).json({ category });
});
```

## Aula XXXI
> Criando um Repositório de Categoria

Repositórios ou Repositories é a camada responssável por fazer a manipulação de dados na aplicação, no momento na nossa aplicação essa responsabilidade está por conta das nossas rotas. Afim de resolver essa problemática, iremos criar um diretório dentro do `src/` chamado `repositories/` e nele, um arquivo representando o repositório das categorias `CategoriesRepository`, com a seguinte estrutura:

```typescript
import { Category } from "../model/Category";

// Sempre quer formos criar um objeto que vai receber informaçãoes vindas da rota, vai criar os DTO para pegar os valores vindos da rota e receber em nossos repositórios
interface ICreateCategoryDTO {
  name: string;
  description: string;
}

class CategoriesRepository {
  private categories: Category[];

  constructor() {
    this.categories = [];
  }

  // responssávelpor cadastrar nossa categoria e será importada nas rotas
  // Vamos dizer aqui que tipo de informações iremos receber na rota com ajuda do DTO
  // informamos que o retorno desse método é vasio (void) jáque iremos apenas salvar os dados no db
  create({ name, description }: ICreateCategoryDTO): void {
    // instanciamos o nosso model
    const category = new Category();

    Object.assign(category, {
      name,
      description,
      created_at: new Date(),
    });

    this.categories.push(category);
  }
}

export { CategoriesRepository };
```

E no nosso arquivo de rotas vamos fazer algumas modificações:

```typescript
import { Router } from "express";

import { CategoriesRepository } from "../repositories/CategoriesRepository";

const categoriesRoutes = Router();
const categoriesRepository = new CategoriesRepository(); // instanciando

categoriesRoutes.post("/", (request, response) => {
  const { name, description } = request.body;

  // utilizando o método create passando as infos vindas do client
  categoriesRepository.create({ name, description });

  return response.status(201).send();
});

export { categoriesRoutes };
```

## Aula XXXII
> Listando Categorias

Ainda no nosso arquivo `CategoriesRepository` vamos criar  um método para listar nossas categorias da seguinte maneira:
```typescript
// informamos o retorno do nosso método que no casso é um array de Category
list(): Category[] {
  return this.categories; // retornando nosso array
}
```
`categories.routes.ts`:
```typescript
categoriesRoutes.get("/", (request, response) => {
  // guardando informação que retornou do método
  const all = categoriesRepository.list();
  // retonando
  return response.json(all);
});
```

## Aula XXXIII
> Validando Cadastro de Categoria

Para a nossa validação, vamos criar um método no nosso repositório chamado `findByName` onde iremos buscar uma categoria com aquele nome recebido na rota e retornará uma categoria.
```typescript
findByName(name: string): Category {
  const category = this.categories.find((category) => category.name === name);
  return category;
}
```
para validação vamos fazer uma logica simple onde passamos o `name` passado no body, caso retorne uma categoria significa que já existe uma categoria com esse nome, nesse caso vamos retornar um `json` com a mensagem de erro, caso contrário, a rota seguirá  normalmente criando uma categoria com o novo `name`.
```typescript
const categoryAlreadyExists = categoriesRepository.findByName(name);

if (categoryAlreadyExists) {
  return response.json({ error: "category Already Exists" });
}
```

## Aula XXXIV
> Entendendo o S.O.L.I.D

"SOLID são cinco princípios da programação orientada a objetos que facilitam no desenvolvimento de softwares, tornando-os fáceis de manter e estender. Esses princípios podem ser aplicados a qualquer linguagem de POO."
[ref](https://medium.com/desenvolvendo-com-paixao/o-que-%C3%A9-solid-o-guia-completo-para-voc%C3%AA-entender-os-5-princ%C3%ADpios-da-poo-2b937b3fc530)
![](https://www.dtidigital.com.br/wp-content/uploads/2019/03/1-768x768.png)

S.O.L.I.D: Os 5 princípios da POO
1. S — Single Responsiblity Principle (Princípio da responsabilidade única)
2. O — Open-Closed Principle (Princípio Aberto-Fechado)
3. L — Liskov Substitution Principle (Princípio da substituição de Liskov)
4. I — Interface Segregation Principle (Princípio da Segregação da Interface)
5. D — Dependency Inversion Principle (Princípio da inversão da dependência)

Caso a aplicação seja muito simples e não há prospecções de crescimento, o SOLID não faz muito sentido ser aplicado, ou pelo menos não por completo. Para saber se ou não implementar e quando implementar, é necesário a compreensão de cada princípio.

## Aula XXXV
> Utilizando o Princípio de Responsabilidade Única (SRP)

SRP — Single Responsibility Principle:
Princípio da Responsabilidade Única — Uma classe deve ter um, e somente um, motivo para mudar.

Esse princípio declara que uma classe deve ser especializada em um único assunto e possuir apenas uma responsabilidade dentro do software, ou seja, a classe deve ter uma única tarefa ou ação para executar.
Caso que não ocorre nas nossas rotas, onde no POST/categories vemos validação, criação, alí no mesmo contexto.

Para isolar essa parte iremos criar uma nova classe, a classe de services. No diretório `src/`, vamos criar a pasta `services/` e nele o arquivo `CreateCategoryService` com a seguinte estrutura:
```typescript
// importando Repositório para definir o tipo do objeto que o CreateCategory vai receber quando for instanciado
import { CategoriesRepository } from "../repositories/CategoriesRepository";

//definimos os tipos dos parâmetros passados no 'execute'
interface IRequest {
  name: string;
  description: string;
}

class CreateCategoryService {
  // Precisamos do repositório porém outros services também irão precisar, não podemos instancialo aqui pois a cada vez que instanciarmos será criado um novo repositório
  // A responsabilidade de criar ficará para quem chama o service no caso a rota
  constructor(private categoriesRepository: CategoriesRepository) {}
  
  // especificando o retorno do método como vazio
  execute({ description, name }: IRequest): void {
  
  // this é usado por conta da privete 
    const categoryAlreadyExists = this.categoriesRepository.findByName(name);

    if (categoryAlreadyExists) {
  
  // tiramos o response pois isso é da responsabilidade da rota
      // tratando o erro com  'throw'
      throw new Error("Category Already Exists");
    }

    this.categoriesRepository.create({ name, description });
  }
}

export { CreateCategoryService };
```

POST/category:
```typescript
categoriesRoutes.post("/", (request, response) => {
  const { name, description } = request.body;

//instanciando e passando o repositório como parâmetro
  const createCategoryService = new CreateCategoryService(categoriesRepository);

  // executando o método e passando como parâmetro as variáveis  vindas do body
  createCategoryService.execute({ name, description });

  return response.status(201).send();
});
```
## Aula XXXVI
> Utilizando o Princípio da Substituição de Liskov (LSP)

LSP— Liskov Substitution Principle:
Princípio da substituição de Liskov — Uma classe derivada deve ser substituível por sua classe base.
O princípio da substituição de Liskov foi introduzido por Barbara Liskov em sua conferência “Data abstraction” em 1987.

**A definição formal de Liskov diz que:**

*"Se para cada objeto o1 do tipo S há um objeto o2 do tipo T de forma que, para todos os programas P definidos em termos de T, o comportamento de P é inalterado quando o1 é substituído por o2 então S é um subtipo de T."*

**Um exemplo mais simples e de fácil compreensão dessa definição. Seria:**

*"Se S é um subtipo de T, então os objetos do tipo T, em um programa, podem ser substituídos pelos objetos de tipo S sem que seja necessário alterar as propriedades deste programa."*

Em modos práticos, agora, na nossa aplicação iremos criar um arquivo que definirá a(s) classe(s) do(s) repositório(s) usado(s), `ICategoriesRepository.ts`, nele vamos ter uma interface definido cada método da classe com a seguinte estrutura:

```typescript
import { Category } from "../model/Category";

interface ICreateCategoryDTO {
  name: string;
  description: string;
}

interface ICategoriesRepository {
  findByName(name: string): Category;
  list(): Category[];
  create({ name, description }: ICreateCategoryDTO): void;
}

export { ICategoriesRepository, ICreateCategoryDTO };
```

dando sequência, iremos implementar essas interfaces criadas em nosso repositório e no nosso service, tipando ele com o `ICategoriesRepository.ts`

`CategoriesRepository.ts`:
```typescript
// imporatando model
import { Category } from "../model/Category";
import {                          // importando interfaces
  ICategoriesRepository,
  ICreateCategoryDTO,
} from "./ICategoriesRepository";

// implementando interface
class CategoriesRepository implements ICategoriesRepository {
  private categories: Category[];

  constructor() {
    this.categories = [];
  }

  create({ name, description }: ICreateCategoryDTO): void { // retorno: vazio
  // regras de negócio
    const category = new Category();

    Object.assign(category, {
      name,
      description,
      created_at: new Date(),
    });

    this.categories.push(category);
  }

  list(): Category[] { // retorno: array de Category
  // regras de negócio
    return this.categories;
  }

  findByName(name: string): Category { // um category
  // regras de negócio
    const category = this.categories.find((category) => category.name === name);
    return category;
  }
}

export { CategoriesRepository };

```
`CreateCategoryService.ts`:
```typescript
import { ICategoriesRepository } from "../repositories/ICategoriesRepository";

interface IRequest {
  name: string;
  description: string;
}

class CreateCategoryService {
  constructor(private categoriesRepository: ICategoriesRepository) {} //recebe interface

  execute({ description, name }: IRequest): void {
    const categoryAlreadyExists = this.categoriesRepository.findByName(name);

    if (categoryAlreadyExists) {
      throw new Error("Category Already Exists");
    }

    this.categoriesRepository.create({ name, description });
  }
}

export { CreateCategoryService };

```

## Aula XXXVII
> Criando Service de Especificação e Separando em Módulos

**Criando Specifications**

Para as Specifications, vamos seguir o [diagrama](#aula-xxviii) onde mostra quais os dados serão guardados, Assim como as Categorias, vamos começar criando o model.
```typescript
import { v4 as uuidv4 } from "uuid";

class Specification {
  id?: string;

  name: string;

  description: string;

  created_at: Date;

  constructor() {
    if (!this.id) {
      this.id = uuidv4();
    }
  }
}

export { Specification };

```

Dando sequeência vamos continuar criando o `CreateSpecificationService.ts`:
```typescript
class CreateSpecificationService {
  execute() {
    console.log("TODO");
  }
}

export { CreateSpecificationService };
```
Além disso vamos criar mais dois arquivos em nosso diretório `repositories/`: `ISpecificationsRepository.ts` e `SpecificationsRepository.ts`
Com nossa aplicação criando tamanho podemos observar que futuramente será inviável visualizar facilmente nossos arquivos no repositories, services, mode. Com o intuito de melhorar nossa visualização ao longo do nosso desenvolvimento, vamos criar no `src/`, um diretório `modules/` onde iremos isolar melhor nossas responsabilidades. Detro da pasta `modules/`, vamos criar a pasta `cars/` que será responssável por tudo que estiver relacionado a carros, por tanto vamos mover as pastas `services/`, `repositories/`, `model/`, para `cars/`

## Aula XXXVIII
> Corrigindo as Importações

Vamos abrir aquirvo o arquivo de rotas e corrigir caso alguma rota esteja fazendo a importação incorretamente.

## Aula XXXIX
> Criando repositório de Especificações

Vamos iniciar criando nossas interfaces, para isso, no arquivo `ISpecificationsRepository.ts`, vamos criar a seguinte estrutura:
```typescript
// importano model
import { Specification } from "../model/Specification";

//interface do create
interface ICreateSpecificationDTO {
  name: string;
  description: string;
}

interface ISpecificationsRepository {
  create({ name, description }: ICreateSpecificationDTO): void; // tipando retorno
  findByName(name: string): Specification; // tipo do retorno igual a objeto
}

export { ISpecificationsRepository, ICreateSpecificationDTO };
```

Agora iremos criar o `SpecificationsRepository.ts` implementando o `ISpecificationsRepository.ts`, da seguinte maneira:
```typescript
import { Specification } from "../model/Specification";
import {
  ICreateSpecificationDTO,
  ISpecificationsRepository,
} from "./ISpecificationsRepository";


class SpecificationsRepository implements ISpecificationsRepository {
  private specifications: Specification[]; // criando tabela(db) fake

  constructor() {
    this.specifications = []; // inicializando nosso array
  }

  create({ name, description }: ICreateSpecificationDTO): void {
    const specification = new Specification(); // instanciando o Specification ou seja, criando um novo

    // colocando os atributos no objeto specification
    Object.assign(specification, {
      name,
      description,
      created_at: new Date(),
    });

    // adicionando no array de specifications
    this.specifications.push(specification);
  }

  findByName(name: string): Specification {
    const specification = this.specifications.find(
      (specification) => specification.name === name
    );

    return specification;
  }
}

export { SpecificationsRepository };
```
E o próximo passo é o `CreateSpecificationService.ts`:
```typescript
import { ISpecificationsRepository } from "../repositories/ISpecificationsRepository";

// Interface simulando a request
interface IRequest {
  name: string;
  description: string;
}

class CreateSpecificationService {

  //para a variável estar disponível para toda a classe
  constructor(private specificationsRepository: ISpecificationsRepository) {}

  // informando que o execute precisa receber esses dois dados com retorno void
  execute({ name, description }: IRequest): void {
    // validando
    const specificationAlreadyExists =
      this.specificationsRepository.findByName(name);

    if (specificationAlreadyExists) {
      // exceção, "caso dê errado"
      throw new Error("Specification already exists");
    }
    // caso esteja tudo certo, crie uma specification
    this.specificationsRepository.create({ name, description });
  }
}

export { CreateSpecificationService };
```

E o próximo passo é criar o arquivo de rotas:
```typescript
//importando Router
import { Router } from "express";

import { SpecificationsRepository } from "../modules/cars/repositories/SpecificationsRepository";
import { CreateSpecificationService } from "../modules/cars/services/CreateSpecificationService";

const specificationsRoutes = Router(); // iniciando rotas
const specificationsRepository = new SpecificationsRepository(); // importando e iniciando nosso repositório

specificationsRoutes.post("/", (request, response) => {
  const { name, description } = request.body;

  // criando specification
  const createSpecificationService = new CreateSpecificationService(
    specificationsRepository
  );

  // recebendo request do body
  createSpecificationService.execute({ name, description });

  return response.status(201).send();
});

export { specificationsRoutes };
```

Importando a rota no `server.ts`:
```typescript
app.use("/specifications", specificationsRoutes);
```
E agora podemos testar no insomnia.

## Aula XL
> Criando os Use Case de Categoria

Nesse momento, mais uma vez, com o intuito de descentralizar asresponssabilidades e melhorar a legibilidade, vamos ajustar a organização do nosso projeto.

Apesar de termos tirado bastante da responsabilidade das nossas rotas, ainda assim fazem operações que não são de sua responsabilidade, responsabilidade essa que seria apenas de receber as requisições e repassar. Para isso vamos criar controllers que ficarão com a atribuição de  receber a requisição e passar a resposta.

Nesse primeiro momento vamos reorganizar um pouco nossa estrutura. Dentro do diretório `cars/` (nosso módulo) vamos criar a pasta `useCasaes/` (regras de negócios) onde separaremos noassas "ações" e a primeira será a `createCategory/` nela vamos por o nosso controller e nosso service (renomear para useCase), além de criar também um index.

![](./assets/usecases.png)

`CreateCategoryController.ts`:
```typescript
import { Request, Response } from "express";

import { CreateCategoryUseCase } from "./CreateCategoryUseCase";

class CreateCategoryController {
  // incorporando e iniciando o objeto
  constructor(private createCategoryUseCase: CreateCategoryUseCase) {}

  // criando método importando os tipos do express 
  handle(request: Request, response: Response): Response {
    const { name, description } = request.body;
    
    // executando o método do antido service onde temos nossos de negócio
    this.createCategoryUseCase.execute({ name, description });

    return response.status(201).send();
  }
}

export { CreateCategoryController };
```

Para importarmos o controller para nossa rota vamos vafazer o seguinte, criar um arquivo para instanciar nosso repositório, usecase, para usarmos na nossa rota.
`index.ts`:
```typescript
import { CategoriesRepository } from "../../repositories/CategoriesRepository";
import { CreateCategoryController } from "./CreateCategoryController";
import { CreateCategoryUseCase } from "./CreateCategoryUseCase";

const categoriesRepository = new CategoriesRepository();
const createCategoryUseCase = new CreateCategoryUseCase(categoriesRepository);
const createCategoryController = new CreateCategoryController(
  createCategoryUseCase
);

export { createCategoryController };
```

Em `categories.routes.ts` vamos fazer uma pequena modificação retornando o médodo handle do controller passando o request e o response:
```typescript
categoriesRoutes.post("/", (request, response) => {
  return createCategoryController.handle(request, response);
});
```
E em seguida só checar as importações.

## Aula XLI
> Refatorando a Listagem de Categoria

para listagem de categoria vamos seguir o memso raciocínio, criando um useCase e mover o service criar o controller e criar o index.

No UseCase: criamos a classe `ListCategoriesuseCase` e exportamos ela adicionamos uns constructor onde chamamos e tipamos o nosso reposotório com o Interface (*private*). Criamos um método `execute` com uma tipagem `Category[]` pois é um array do tipo `Category` (*model*), após buscarmos a lista com o método `list()` retornamos as `categories`.
```typescript
import { Category } from "../../model/Category";
import { ICategoriesRepository } from "../../repositories/ICategoriesRepository";

class ListCategoriesuseCase {
  constructor(private categoriesRepository: ICategoriesRepository) {}
  execute(): Category[] {
    const categories = this.categoriesRepository.list();

    return categories;
  }
}
export { ListCategoriesuseCase };
```

Processo semenlhante vai se repetir no controller:
```typescript
import { Request, Response } from "express";

import { ListCategoriesuseCase } from "./ListCategoriesUseCase";

class ListCategoriesController {
  constructor(private listCategoriesUseCase: ListCategoriesuseCase) {}

  handle(request: Request, response: Response): Response {
    const all = this.listCategoriesUseCase.execute();

    return response.json(all);
  }
}

export { ListCategoriesController };
```
Dando sequência vamos ao index, onde vamos instanciar os objetos que serão usados na rota.
```typescript
import { CategoriesRepository } from "../../repositories/CategoriesRepository";
import { ListCategoriesController } from "./ListCategoriesController";
import { ListCategoriesuseCase } from "./ListCategoriesUseCase";

const categoriesRepository = new CategoriesRepository();
const listCategoriesUseCase = new ListCategoriesuseCase(categoriesRepository);
const listCategoriesController = new ListCategoriesController(
  listCategoriesUseCase
);

export { listCategoriesController };
```
E finalmente na rota:
```typescript
  categoriesRoutes.get("/", (request, response) => {
  return listCategoriesController.handle(request, response);
});
```

## Aula XLII
> Conhecendo Singleton Pattern

Singleton é um padrão de projeto de software. Este padrão garante a existência de apenas uma instância de uma classe, mantendo um ponto global de acesso ao seu objeto. Nota linguística: O termo vem do significado em inglês para um conjunto que contenha apenas um elemento. -[Wikipedia](https://pt.wikipedia.org/wiki/Singleton)

Implementando o Singleton em nosso repositório de categorias:
```typescript
class CategoriesRepository implements ICategoriesRepository {
  private categories: Category[];

  private static INSTANCE: CategoriesRepository;

  private constructor() {
    this.categories = [];
  }
  // caso n tenha a instância, crie a instância
  public static getInstance(): CategoriesRepository {
    if (!CategoriesRepository.INSTANCE) {
      CategoriesRepository.INSTANCE = new CategoriesRepository();
    }
    return CategoriesRepository.INSTANCE;
  }
  ...
}
```
[REVISAR](https://www.youtube.com/watch?v=zkzPhD8Lnno&t=399s)

## Aula XLIII
> Separando os repositórios

Agora vamos simplesmente criar uma diretório chamado `implementations/`, dentro do diretório de repositórios para separas as nossas interfaces em seguida ajustar os imports que aparecerem errados.

## Aula XLIV
> Criando Use Case de Especificações

- Criar diretório `createSpecification/` dentro do `useCase/`
- Criar os diretório `index.ts` e `CreateSpecificationController.ts` e mover `CreateSpecificationService.ts` para o diretório criado
- Renomear `CreateSpecificationService.ts` para `CreateSpecificationUseCase.ts` e sua classe seguindo o mesmo padrão
- Controller:
  - Criar uma classe e exportá-la seguindo o modelo das anteriores
  - criar método `handle` que recebe `Request` e `Response` do `express`
  - tipar é método com `Response`
  - pegar o que tem no post/ e passar para o `handle`
  - Criar constructor onde recebe o useCase
- index:
  - instaciar o repositório
  - instanciar o use case e passar o repositório
  - instanciar o controller e passar  o usecase
  - exportar o controller
- Importar o controller na rota e passar o request e o response

## Aula XLV
> Refatorando as Rotas

Agora vamos fazer um pequeno retoque. Nas rotas vamos criar um index dentro da pasta `routes/` para unificar todas as rotas e exportálas para o server da seguinte maneira:

**`routes/index.ts`**:
```typescript
import { Router } from "express";

import { categoriesRoutes } from "./categories.routes";
import { specificationsRoutes } from "./specifications.routes";

const router = Router();

router.use("/categories", categoriesRoutes);
router.use("/specifications", specificationsRoutes);

export { router };
```
`server.ts`:
```typescript
import { router } from "./routes";

app.use(router);
```
## Aula XLVI
> Conhecendo o Multer

Vamos cadasrar as categorias importando um arquivo, lendo o arquivo e salvando, para nos auxiliar vamos utilizar a biblioteca [multer](https://www.npmjs.com/package/multer) para o upload de arquivos.

## Aula XLVII
> Criando Upload de Arquivos

- Instalar o multer: `yarn add multer`
- Instalar as tipagens do multer: `yarn add @types/multer -D`
- Criar rota: `categoriesRoutes.post("/import", (request, response) =>{})`
- Instanciar o multer: `const upload = multer()`
- Criar pasta `temp/` na raiz no projeto
- setar o pasta de destino do upload: `const upload = multer({dest: "./temp"})`
- passar o multer como middleware: `categoriesRoutes.post("/import", upload.single("file"), (request, response) =>{})` obs.: o nome do arquivo q será passad, será "file"

Visualizando o arquivo importado

```typescript
categoriesRoutes.post("/import", upload.single("file"), (request, response) =>{
  const { file } = request;
  console.log(file);
  return response.send();
})
```

No insommia vamos criar nossa request post e no body vamos escolher "Multipart Form", por nossa rota "/categories/import" e por no campo "name" do Multipart "file" e no value, escolher "file".

## Aula XLVIII
> Criando o Use Case  para Importar Categorias

Dentro do diretório `useCases/` vamos criar o diretório do nosso useCase `importCategory/` e os três arquivos assim como nos demais useCases, sendo eles:
- [] **ImportCategoryController.ts**
- [] **ImportCategoryUseCase.ts**
- [] **Index.ts**

Vamos dar início por aqui criando nosso método handle na nossa classe controller, seguindo a mesma ideia de nomenclatura das classes feitas até aqui. no handle, nós recebemos o request e o reponse tipando nosso retorno como Response e recebemos nosso "file" do request => `const { file } = request`. Para visualizarmos o arquivo, damos um `console.log(file);` e um `return response.send();`.

Para já integrarmos o nosso controller a nossa rota seguindo a estrutura aoresentada anteriormente vamos forerir se estamos exportando nosso controller importálo no index e exportálo para o categories.routes onde retornará o método hadle passando o request e o response.

Agora vamos iniciar criando a nossa classe useCase e em seguida exportando-a para o controller e depois para o index como feito anteriormente em outros useCases.
**importCategoryUseCase:**
![](./assets/UseCase.png)
> Criação o método execute passando o console.log(file).


**importCategoryController:**
![](./assets/controller.png)
> pasando o useCase para o constructor possibilitando assimo uso do método execute do useCase, passando o file.


**index:**
![](./assets/index.png)
> Aqui no index vamos apenas instanciar nossos objetos passando o use case pelo controller.

Nesse momento podemos verificar se está tudo ok indo lá no insomnia.

## Aula XLIX
> Conhecendo o conceito de stream

Para a leitura do nosso arquivo vamos usar o conceito de stream, usando a biblioteca fs do próprio NodeJS. No fs iremos guardar em uma variável chamada `stream`, o retorno do método para criar leitura de stream, onde passamos como parâmetro o path do nosso arquivo. A variável stream retonará pedaços do nosso arquivo utilizando o método pipe como mostra a figura a baixo:

![](assets/fs.png)

Paraleitura do arquivo csv em si vamos utilizar outra biblioteca, a `csvParse`, onde vamos receber do método pipe os dados passando o objeto do csv-parse da seguinte maneira:

![](assets/csv-parse.png)

## Aula L
> lendo os Dados do Upload

Já conseguimos importar o arquivo, ler o arquivo, agora nosso objetivo será salvar os dados desse arquivo. para manipulação do nossos dados precisamos inicialmente importar nosso repositório, recebendo ele em nosso constructors e passando a sua tipagem: `constructor(private categoriesRepository: ICategoriesRepository) {}`. Assim que feito isso, vamos instanciá-lo no nosso arquivo index e passá-lo no useCase.
```typescript
const categoryRepository = CategoriesRepository.getInstance();
const importCategoryUseCase = new ImportCategoryuseCase(categoryRepository);
```

Para guardar nossos dados vamos fazer a leitura e guardar primeiramente os dados e um array para em seguida passar para o repositório, paa isso vamos criar uma interface que vai receber os dados de name e description.

```typescript
interface IImportCategory {
  name: string;
  description: string;
}
```
Inicializar array
```typescript
class ImportCategoryuseCase {
  constructor(private categoriesRepository: ICategoriesRepository) {}

  loadCategories(file: Express.Multer.File): Promise<IImportCategory[]> {
    return new Promise((resolve, reject) => {
      const stream = fs.createReadStream(file.path);
      const categories: IImportCategory[] = []; // <==========================
```

```typescript
class ImportCategoryuseCase {
  constructor(private categoriesRepository: ICategoriesRepository) {}

  loadCategories(file: Express.Multer.File): Promise<IImportCategory[]> { // Já que estamos trabalhando com Promisses, passamos a promisse como tipo e o tipo da promisse
    return new Promise((resolve, reject) => { // criando promisse
      const stream = fs.createReadStream(file.path);
      const categories: IImportCategory[] = [];

      const parseFile = csvParse();

      stream.pipe(parseFile);

      parseFile
        .on("data", async (line) => {
          const [name, description] = line;
          categories.push({ // passando os dados para o array
            name,
            description,
          });
        })
        .on("end", () => {       // quando finalizar
          resolve(categories);   // retorne o array
        })
        .on("error", (err) => {  // tratando erro caso tenha
          reject(err);
        });
    });
  }
  async execute(file: Express.Multer.File): Promise<void> { // Já que estamos trabalhando com Promisses, passamos a promisse como tipo e o tipo da promisse
    const categories = await this.loadCategories(file);
    console.log(categories);
  }
}
```
![](assets/retorno_upload.png)

## Aula LI
> Inserindo os Dados do Upload no Repositório

Pra inserir as categorias no "banco de dados" vamos usar um map dentro do nosso arra, fazendo manipulação intem por item.
```typescript
categories.map(async (category) => {
      const { name, description } = category; // desestruturação do objeto
      
      // fazendo validação
      const existCategory = this.categoriesRepository.findByName(name); // buscando objeto

      if (!existCategory) { // apenas se não existir salve-o em nosso banco de dados
        this.categoriesRepository.create({
          name,
          description,
        });
      }
    });
```

## Aula LII
> Conhecendo o Swagger

[Swagger](https://swagger.io) é uma ferramenta que nos ajuda a criar documentações claras de forma simples tanto pra quem faz quant pra quem utiliza.

## Aula LIII
> Configurando o Swagger

**Instalação**

- Instalar: `yarn add swagger-ui-express`
- Instalar tipagem: `yarn add @types/swagger-ui-express -D` 

**Importação**

Importar o swagger dentro no nosso server:
```typescript
import swaggerUi from "swagger-ui-express";
...
app.use("/api-docs", swaggerUi.serve, swaggerUi.setup(swaggerFile)); // rota da documentação, middleware, JSON com as configurações
```
obs: é necesário que no tsconfig.json esteja habilitado a seguinte configuração: `"resolveJsonModule":true `

**Criação do JSON**

Esse JSON será responsável por todas as inforções apresentadas na documentação. todas as possibilidades de informação a respeito dessa parte está neste [link aqui](https://swagger.io/docs/specification/basic-structure/). Nosso JSON inicialmente ficará assim:
```json
{
  "openapi":"3.0.0",
  "info": {
    "title": "RentalX Documentation",
    "description": "This is an API Rent",
    "version": "1.0.0",
    "contact": {
      "email": "brunoosouza15@gmail.com"
    }
  }
}
```
Finalizado esta etapa, podemos rodar um `yarn dev` e ir até a rota <http://localhost:3333/api-docs>.

## Aula LIV
> Criando a Documentação de Criação de Categoria

Após a seção de `infos`, vamos iniciar com a criação de um objetochamado `"paths":{}` que será responsável por adicionar todas as rotas seguindo a seguinte estrutura:
```JSON
  "paths": {
    "/categories": {
      "post": {
        "tags": ["Category"],
        "sumary": "Create a category",
        "description": "Create a new category",
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "type": "object",
                "properties": {
                  "name": {
                    "type": "string"
                  },
                  "description": {
                    "type": "string"
                  }
                },
                "example": {
                  "name": "CategoryTest",
                  "description": "Category description test"
                }
              }
            }
          }
        },
        "responses": {
          "201": {
            "description": "Created"
          },
          "500": {
            "description": "Category already exists"
          }
        }
      }
    }
  }
```

## Aula LV
> Criando Documentação da Listagem de Categorias

Agora vamos fazer a rota da documnetação pra fazer a listagem das categorias.

```json
"get": {
        "tags":["Category"],
        "summary": "List all category",
        "description": "List all category",
        "responses": {
          "200": {
            "description": "Sucess",
            "content": {
              "application/json": {
                "schema":{
                  "type":"array",
                  "items": {
                    "type":"object",
                    "properties": {
                      "name": {
                        "type":"string"
                      },
                      "description":{
                        "type":"string"
                      }
                    }
                  }
                }
              }
            }
          }
        }
      }
```

## Aula LVI
> Removendo os Arquivos de Upload

Adicone a seguinte linha no useCase do importCategory:
```typescript
parseFile
        .on("data", async (line) => {
          const [name, description] = line;
          categories.push({
            name,
            description,
          });
        })
        .on("end", () => {
          fs.promises.unlink(file.path); // passe o caminho do arquivo a ser excluído
          resolve(categories);
        })
        .on("error", (err) => {
          reject(err);
        });
```

**CHAPTER III**

## Aula LVII
> Introdução ao Chapter III

* Introdução ao Docker
* Criando containers no Docker
* Bancode dados no Docker
* Comandos no Docker
* Incremetnando a documentação 
* Criptografias e senhas

## Aula LVIII
> O que é Docker?

* Ferramenta que auxilia a craição de containers (ambiente isolados da nossa máquina)
* As "intruções" para criação desses ambientes isolados são chamados de **imagens**

> O Docker é uma plataforma open source que facilita a criação e administração de ambientes isolados. Ele possibilita o empacotamento de uma aplicação ou ambiente dentro de um container, se tornando portátil para qualquer outro host que contenha o Docker instalado.

![Docker](https://dkrn4sk0rn31v.cloudfront.net/2018/09/28135438/virtualization-vs-containers.jpg)

### Containers

Um container é um ambiente isolado. Um container contém um conjunto de processos que são executados a partir de uma imagem, imagem esta que fornece todos os arquivos necessários. Os containers compartilham o mesmo kernel e isolam os processos da aplicação do restante do sistema.

**Por exemplo:** se você está desenvolvendo uma aplicação para um cliente, você pode fazer suas configurações nessa aplicação… Mas, em um ambiente convencional, você precisará replicar estas configurações para os outros ambientes de execução. Com o Docker, você estará fazendo isso em um ambiente isolado e, por causa da facilidade para replicação de containers, você acaba criando ambientes padronizados, tanto em desenvolvimento como em produção, por exemplo. 

## Aula LIX
> Criando nosso peimeiro container e Dockerfile

Passando a responsabilidade dos prerequisitos de instalação para o Docker, ficamos livres para nãos instalarmos pacotes como node, postgres, qualquer outro banco de dados, ou ferramenta que requeira sua instalação no computador.


1. `touch .dockerignore` *Arquivos que serão ignorados pelo Docker*
```
node_modules
.git
.vscode
assets
README.md
```
2. `touch Dockerfile` *Esse arquivo serve como um receita de bolo para que o Docker saibar quais procedimentos devem ser feitos*
```
FROM node // buscando imagem do node

WORKDIR /usr/app // Diretório de trabalho onde vai ser rodado no projeto

COPY package.json ./ // primeiro argumento é o que vai ser copiado e o segundo é o seu destino no workdir

RUN npm install // instalar as dependências criando o nodemodules

COPY . . // copia tudo (.) para a raiz (.)

EXPOSE 3333 // porta do nosso projeto

CMD ["npm", "run", "dev"] // permite executar comandos onde são separados em uma lista de array
```
3. Executando nosso arquivo Dockerfile
```bsh
sudo docker build -t rentalx . // "retalx" = nomde da imagem que vamos criar, "." =  onde está o arquivo Dockerfile
```
4. Com a imagem criada vamos executála
```bsh
sudo docker run -p 3333:3333 rentalx // "-p 3333:3333" setando a portando do Docker e do nosso localhost "rentalx a imagem q será rodada"
```
5. Verificar nome do container
```bsh
sudo docker ps

```
6. Acesso ao container
```bsh
sudo docker -it 'nome do container' /bin/bash

```

## Aula LX
> Usando Docker-compose

**Para que serve o DOcker-compose?**
Ele funciona como um orquestrador de container, basicamente. Para realizar a comunicação entre os containers, podemos utilizar uma ferramenta do próprio Docker chamada de Docker Compose. Com o Docker Compose podemos criar um arquivo e especificar as propriedades de cada container, como comandos, variáveis de ambiente, etc.

Utilizando  **Docker-compose**

Na raiz do nosso projeto, vamos criar um arquivo chamado `docker-compose.yml` onde iremos passar as seguintes confirações:
```yml
version: "3.7"

services:
  app:
    build: .
    container_name: rentalx
    ports: 
      - 3333:3333
    volumes: 
      - .:/usr/app
```

E rodar os seguintes comandos

Para executar  os containers em segundo plano:
```yml
sudo docker-compose up -d
```
Conferir o logs do docker:
```yml
sudo docker-compose logs nome_do_container -f
```

## Aula LXI
> Comandos do Docker

Lista os containers em execução:
```sh
sudo docker ps
```
Lista todos os containers:
```sh
sudo docker ps -a
```
Remover container:
```sh
sudo docker rm id_do_container
```
Iniciar um container:
```sh
sudo docker start id_do_container
```
Para executar  os containers em segundo plano:
```sh
sudo docker-compose up -d
```
Parar container em execução:
```sh
sudo docker-compose stop
```
Executar container do docker-compose:
```sh
sudo docker-compose start
```
Remover docker-compose e seus serviços:
```sh
sudo docker-compose down
```
Para acessar o container:
```sh
sudo docker exec -it nome_do_container /bin/bash
```
Para sair do container:
```sh
CTRL + D
```
Conferir o logs do docker:
```sh
sudo docker-compose logs nome_do_container -f
```
Parar o log:
```sh
CTRL + C
```
## Aula LXII
> Conhecendo as formas de usar o banco de dados

Divrer Nativo: Dificulta a troca futura de um banco de dados
Querry Bilders : Facilita uma possível troca de banco de dados
ORM: Facilita uma possível troca de banco de dados, além de mapear nossas entidades trabalhando melhor com o banco de dados

## Aula LXIII
> Instalando TypeORM

Nesse momento vamos instalar além do typeorm, o reflect-metada como a documentação sugere e um banco de dados da nossa escolha.

```sh
yarn add typeorm reflect-metadata pg
```

Em seguida vamos criar um diretório no `src/`, chamado `database/`, onde nele vamos criar um arquivo index.ts com o seguinte código, onde estaremos estabelecendo nossa conexão.
```typescript
import { createConnection } from "typeorm";

createConnection();
```
Agora vamos importar o nosso database para nosso server:
```typescript
import express from "express";
import swaggerUi from "swagger-ui-express";

import { router } from "./routes";
import swaggerFile from "./swagger.json";

import "./database";
...
```
Dando sequência, vamos passar nossas configurações do banco de dados para um arquivo chamado `ormconfig.json` com a seguinte estrutura:
```json
{
  "type": "postgres",
  "host": "localhost",
  "username": "docker",
  "password": "ignite",
  "database": "rentalx"
}
```

## Aula LXIV
> Criando Container do postgres

Vamos criar nosso banco de dados através do docker-compose e conectar o banco de dados ao app. Para isso vamos editar nosso arquivo `docker-compose.yml`:
```yml
version: "3.7"

services:
  database_ignite:
    image: postgres
    container_name: database_ignite
    restart: always
    ports: 
      - 5432:5432
    environment:
      - POSTGRES_USER=docker
      - POSTGRES_PASSWORD=ignite
      - POSTGRES_DB=rentalx
    volumes:
      - pgdata:/data/postgres

  app:
    build: .
    container_name: rentalx
    ports: 
      - 3333:3333
    volumes: 
      - .:/usr/app
    links: 
      - database_ignite
    depends_on: 
      - database_ignite

volumes:
  pgdata:
    driver: local
```

## Aula LXV
> Aprendendo o conceito de migrations

As migrations é um versionamento para nosso banco de dados, onde vamos criar e alterar nossas tabelas pelas migrations criadas.

## Aula LXVI
> Criando Migration de Category

Vamos iniciar criando um script como sugere a documentação para podermos executar a nossa `cli`:
```JSON
"srcipts": {
  "typeorm": "ts-node-dev ./node_modules/typeorm/cli"
}
```
Logo após, vamos criar dentro do diretório `database/` a pasta `migrations` onde serão criadas as migrations invocadas a partir da nossa cli. Para mapear essa pasta, nós vamos adicionar uma pequena configuração ao nosso aqrquivo `ormconfig.json`:
```JSON
"cli": {
    "migrationsDir": "./src/database/migrations"
  }
```
E para executar o comando criando a nossa migration CreateCategories: `yarn typeorm migration:create -n CreateCategories`.

No nosso arquivo de migration, nós vamos iniciar a criação de tabela de categories, com a seguinte estrutur:
```typescript
import { MigrationInterface, QueryRunner, Table } from "typeorm";

export class CreateCategories1622503323530 implements MigrationInterface {
  public async up(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.createTable(
      new Table({
        name: "categories",
        columns: [
          {
            name: "id",
            type: "uuid",
            isPrimary: true,
          },
          {
            name: "name",
            type: "varchar",
          },
          {
            name: "description",
            type: "varchar",
          },
          {
            name: "created_at",
            type: "timestamp",
            default: "now()",
          },
        ],
      })
    );
  }

  public async down(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.dropTable("categories");
  }
}
```
Vamos verificar  a seguinte configuração:
```JSON
{
  "migrations": ["./src/database/migrations/*.ts"],
}
```

E para executar nossa migration:
```sh
yarn typeorm migration:run
```
Para desfazer:
```sh
yarn typeorm migration:revert
```

## Aula LXVII
> Refatorando o Model de Category

Para que nosso ORM possa "mapear" nossas tabelas na aplicação recisamos ter algo parecido com o que na verdade já temos no nosso model, só que com o nome entities. Para isso vamos renomear nossa pasta model para entities e adicionar a seguinte estrutura nossa "Category":

```typescript
import { Column, CreateDateColumn, Entity, PrimaryColumn } from "typeorm";
import { v4 as uuidv4 } from "uuid";

@Entity("categories") // nome da tabela representada
class Category {
  @PrimaryColumn()
  id?: string;

  @Column()
  name: string;

  @Column()
  description: string;

  @CreateDateColumn()
  created_at: Date;

  constructor() {
    if (!this.id) {
      this.id = uuidv4();
    }
  }
}

export { Category };
```

## Aula LXVIII
> Alterando o Repositório de Category

Para podermos manipular o banco de dados, nosso ORM oferece o "Repository" que já possuem alguns métodos que podem ser usadas na nossa aplicação. No cassa desta aplicação já criamos os métodos a serem usados, por tanto vamos tornar nosso repository "private".

```typescript
private repository: Repository<Category>;

private constructor() {
  this.repository = getRepository(Category);
}
```

Os métodos serão todos async, portanto, vamos alterar o tipo de retorno de todos para "Promise" do tipo que estava anteriormente.
```typescript
async create({ name, description }: ICreateCategoryDTO): Promise<void> {
  const category = await this.repository.create({ // criando category
    name,
    description, // não é mais necessário criar a data de criação pois essa função está a cargo agora do nosso banco de dados
  });

  await this.repository.save(category); // salvando category
}

async list(): Promise<Category[]> {
  const categories = await this.repository.find(); // buscando todas as categorias
  return categories;
}

async findByName(name: string): Promise<Category> {
  const category = await this.repository.findOne({ name }); // buscando por nome
  return category;
}
```

Em seguid vamos alterar a nossa interface:
```typescript
interface ICategoriesRepository {
  findByName(name: string): Promise<Category>;
  list(): Promise<Category[]>;
  create({ name, description }: ICreateCategoryDTO): Promise<void>;
}
```

## Aula LXIX
> Refatorando o Caso de Uso de Category

Primeiramente vamos refatorar nosso repositório onde vamos tirar nosso construtor do `private` e retirar a parte de `instance` ja que estaremos agora o nosso banco de dados.

Agora no arquivo `index.ts` do `createCategory/` vamos alterar o import do nosso repository já que acbamos de alterar e transformar tudo em uma função onde teremos o cotrole de quando serrá executada.

```typescript
// [importações]
export default (): CreateCategoryController => {
  const categoriesRepository = new CategoriesRepository();

  const createCategoryUseCase = new CreateCategoryUseCase(categoriesRepository);

  const createCategoryController = new CreateCategoryController(
    createCategoryUseCase
  );
  return createCategoryController;
};
```
Na nossa rota, vamos fazer duas pequenas correções. A primeira refere-se a importação do `createCategoryController` onde tiramos as `{}` já que exportamos como `default`. A segunda alteração é na invocação `createCategoryController` como função, ficando da seguinte maneira .
```typescript
// [...]
import createCategoryController from "../modules/cars/useCases/createCategory";
// [...]
categoriesRoutes.post("/", (request, response) => {
  return createCategoryController().handle(request, response);
});
// [...]
```
Para que o código possa rodar sem ser feito todas as alterções na parte dos `category`, nos demais `useCase/` vamos atribuir o valor como null ao `categoriesRepository`. Próximo passo é corrigir as funções onde usamos de alguma forma o banco de dados ou onde passam as informações dele, tornando-os assícronos (Arquivos de useCase e conotroller).

## Aula LXX
> Entendendo as Alterações

- Refatoração do repositório de categorias
- Tirar a parte de instâncias pois agora não guardamos as informações em memória e sim no nosso banco de dados
- Tirar o `private` do `constructor`
- Envolver o `Controller` em uma função (instanciar apenas quando chamar)

## Aula LXXI
> Conhecendo TSyringe

O TSyringe vai nos ajudar a fazer as injenções de dependêncis na nossa aplicação.

**Instalar**
```typescript
yarn add tsyringe
```

incluir configuraçõs do Typescript
```JSON
{
  "compilerOptions": {
    "experimentalDecorators": true,
    "emitDecoratorMetadata": true,
  }
}
```
Importar o reflect-metadata pra nosso "arquivo inicial"
```typescript
import "reflect-metadata";
``` 

Na pasta `src/` vamos criar `shared/container/index.ts` com a sguinte extrutura.

```typescript
import { container } from "tsyringe";

import { CategoriesRepository } from "../../modules/cars/repositories/CategoriesRepository";
import { ICategoriesRepository } from "../../modules/cars/repositories/Implementations/ICategoriesRepository";

container.registerSingleton<ICategoriesRepository>(
  "CategoriesRepository", // Nome da chamada
  CategoriesRepository // Classe a ser chamada
);
```

No arquivo CreateCategoryUseCase:

```typescript
@injectable() // Torna injetável pelo nosson controller, no caso
class CreateCategoryUseCase {
  constructor(
    @inject("CategoriesRepository") // cria ferência com a classe
    private categoriesRepository: ICategoriesRepository
  ) {}

```

No arquivo CreateCategoryController:
```typescript
import { Request, Response } from "express";
import { container } from "tsyringe";

import { CreateCategoryUseCase } from "./CreateCategoryUseCase";

class CreateCategoryController {
  async handle(request: Request, response: Response): Promise<Response> {
    const { name, description } = request.body;
    const createCategoryUseCase = container.resolve(CreateCategoryUseCase);

    await createCategoryUseCase.execute({ name, description });

    return response.status(201).send();
  }
}

export { CreateCategoryController };
```
Podemos disconsiderar o nosso arquivo index.ts e ir as rotas:
```typescript
import { CreateCategoryController } from "../modules/cars/useCases/createCategory/CreateCategoryController"; // importando controller

const createCategoryController = new CreateCategoryController();

categoriesRoutes.post("/", createCategoryController.handle);
```
Chamar o container em nosso `server.ts`:
```typescript
import "reflect-metadata";
import express from "express";
import swaggerUi from "swagger-ui-express";

import "./database";

import "./shared/container";
```

## Aula LXXII
> Refatorando as especificações

Primeiramente vamos excluir o index na pastas `useCases/createCategory/`

Agora vamos refatorar o restante dos Nossos useCases. O repositório das categorias já está pronto lá no nosso "container" do TSyringe então vamos criar o das especificações e avançar para os casos de uso. Assim como foi feito para a CategoriesRepository vamos fazer o seguinte para SpecificationsRepository da seguinte maneira:

```typescript
container.registerSingleton<ISpecificationsRepository>(
  "SpecificationsRepository",
  SpecificationsRepository
);
```

Voltando para os casos de uso de categories, a princípio, nos nossos arquivos *CategoryUseCase.ts, vamos adicionar a seguinte estrutura:

```typescript
@injectable() // aqui torna a classe "injetável" onde vamos usar no no controller
class ImportCategoryUseCase {
  constructor(
    @inject("CategoriesRepository") // "instancia" no repositório 
    private categoriesRepository: ICategoriesRepository
  ) {}
```

Vamos retirar os index de casa useCase e importar o controller no arqquivo de rotas da seguinte maneira:

```typescript
// [...]
import { ListCategoriesController } from "../modules/cars/useCases/listCategories/ListCategoriesController";
// [...]
const listCategoriesController = new ListCategoriesController();
categoriesRoutes.get("/", listCategoriesController.handle);
```

## Aula LXXIII
> Criando Migration de Especificações

Migrations -> Entities -> Repository -> useCase -> Routes

**Migrations**

```sh
yarn typeorm migration:create -n CreateSpecifications
```

Vamos seguir com a seguinte extrutura:
```typescript
import { MigrationInterface, QueryRunner, Table } from "typeorm";

export class CreateSpecifications1623924126000 implements MigrationInterface {
  public async up(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.createTable(
      new Table({
        name: "specifications",
        columns: [
          {
            name: "id",
            type: "uuid",
            isPrimary: true,
          },
          {
            name: "name",
            type: "varchar",
          },
          {
            name: "description",
            type: "varchar",
          },
          {
            name: "created_at",
            type: "timestamp",
            default: "now()",
          },
        ],
      })
    );
  }

  public async down(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.dropTable("specifications");
  }
}
```
**Entities**

Após, rodar o comando `yarn typeorm migration:run` e estruturaremos as entidades de specifications assim:

```typescript
import { Column, CreateDateColumn, Entity, PrimaryColumn } from "typeorm";
import { v4 as uuidv4 } from "uuid";

@Entity("specifications")
class Specification {
  @PrimaryColumn()
  id?: string;

  @Column()
  name: string;

  @Column()
  description: string;

  @CreateDateColumn()
  created_at: Date;

  constructor() {
    if (!this.id) {
      this.id = uuidv4();
    }
  }
}

export { Specification };
```
**Repository**

```typescript
class SpecificationsRepository implements ISpecificationsRepository { // modificar a interface colocando os retornos como "Promise<'tipo'>" 
  private repository: Repository<Specification>;

  constructor() {
    this.repository = getRepository(Specification);
  }

  async create({ name, description }: ICreateSpecificationDTO): Promise<void> {
    const specification = this.repository.create({
      name,
      description,
    });

    await this.repository.save(specification);
  }

  async findByName(name: string): Promise<Specification> {
    const specification = await this.repository.findOne({
      name,
    });

    return specification;
  }
}

export { SpecificationsRepository };
```

**UseCase & Controller**

Aqui vamos basicamente refatorar as funções em assíncronas quando necessário.

**Routes**

```typescript
// [...]
import { CreateSpecificationController } from "../modules/cars/useCases/createSpecification/CreateSpecificationController";
// [...]
const createSpecificationController = new CreateSpecificationController();

specificationsRoutes.post("/", createSpecificationController.hadle);
```
## Aula LXXIV
> Continuação da Documentação

Continuando aqui na documentação, vamos adicionar mais um path, o `"/specifications"` com a seguinte estrutura:
```JSON
"paths": {
    "/specifications": {
      "post": {
        "tags": ["Specifications"],
        "summary":"Create a specification",
        "description": "Create a new specification",
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/definitions/Specification" // fazendo referencia a definition uma forma de reduzir linhas caso tenha uma parte que da documentaçã onde alguma parte se repete
              }
            }
          }
        },
        "responses": {
          "201": {
            "description": "Created"
          },
          "500": {
            "description": "Specification already exists!"
          }
        }
      }
    }
  },
  "definitions": {
    "Specification": {
      "type": "object",
      "properties":{
        "name": {
          "type":"string"
        },
        "description": {
          "type":"string"
        }
      }
    }
  }
```

Em seguida podemos testar na documentação se está funcionando e verificar se recebemos no banco de dados.

Para criar agora a documentação do nosso **Import Category** vamos adicionar mais um path, o `/categories/import` com a estrutur a seguir:
```JSON
"/categories/import": {
  "post": {
    "tags": ["Category"], // Apontando para seção de categorias
    "summary": "Upload a new category",
    "description": "Upload a new category",
    "requestBody": {
      "content": {
        "multipart/form-data": { // configuração  para importar nosso arquivo 
          "schema": {
            "type": "object",
            "properties": {
              "file": {
                "type": "string",
                "format": "binary"
              }
            }
          }
        }
      }
    },
    "responses": {
      "201": {
        "description": "Created"
      }
    }
  }
}
```
Aqui novamente podemos conferir se está tudo ok indo na rota de listagem e verificando se conseguimos importar os dados do nosso arquivo.

## Aula LXXV
> Criando Migration de Usuário

Não muito diferente do que já foi feito, vamos criar agora uma migration para criar a tabela de usuários onde teremos os campos de: id, name, username, email, password, driver_license, isAdmin e created_at como mostra a seguir.
```typescript
import { MigrationInterface, QueryRunner, Table } from "typeorm";

export class CreateUsers1623974939522 implements MigrationInterface {
  public async up(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.createTable(
      new Table({
        name: "users",
        columns: [
          {
            name: "id",
            type: "uuid",
          },
          {
            name: "name",
            type: "varchar",
          },
          {
            name: "username",
            type: "varchar",
            isUnique: true, // Apenas um usuário por username
          },
          {
            name: "password",
            type: "varchar",
          },
          {
            name: "email",
            type: "varchar",
          },
          {
            name: "driver_license",
            type: "varchar",
          },
          {
            name: "isAdmin",
            type: "boolean",
            default: "false", // por padrão é falso
          },
          {
            name: "created_at",
            type: "timestamp",
            default: "now()",
          },
        ],
      })
    );
  }

  public async down(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.dropTable("users");
  }
}
```
Podemos rodar o comando `yarn typeorm migration:run` e após verificar a criação da tabela no banco de dados.

Logo depois da criação das migrations, vamos criar nossa entidade, antes dissso, na nossa pasta modules vamos criar o módulos `accounts/` e nele o diretório `entities/` e então nosso arquivo `User.ts` onde vamos seguir com uma estrutura bem parecido com a qual já trabalhamos.

```typescript
import { Column, CreateDateColumn, Entity, PrimaryColumn } from "typeorm";
import { v4 as uuidv4 } from "uuid";

@Entity("users")
class User {
  @PrimaryColumn()
  id: string;

  @Column()
  name: string;

  @Column()
  username: string;

  @Column()
  email: string;

  @Column()
  password: string;

  @Column()
  driver_license: string;

  @Column()
  isAdmin: boolean;

  @CreateDateColumn()
  created_at: Date;

  constructor() {
    if (!this.id) {
      this.id = uuidv4();
    }
  }
}

export { User };
```

## Aula LXXVI
> Criando Repositório de Usuário

Após criado nossa entidade, que será a comunicação com nosso banco de dados, iremos partir pra o repositório o qual irá trabalahar esse banco de dados. Primeiramente iremos criar dentro do módulo `accounts` os arquivos: `IUsersRepository.ts` no diretório `repositories/implementations/`; `UsersRepository.ts` no diretório `repositories/`; `ICreateUserDTO.ts` no diretório `dtos`.

**`ICreateUserDTO.ts`:**
```typescript
interface ICreateUserDTO {
  name: string;
  email: string;
  password: string;
  driver_license: string;
}

export { ICreateUserDTO };
```

**`IUsersRepository.ts`:**
```typescript
import { ICreateUserDTO } from "../../dtos/ICreateUserDTO";

interface IUsersRepository {
  create(data: ICreateUserDTO): Promise<void>;
}

export { IUsersRepository };
```

**`UsersRepository.ts`:**
```typescript
import { getRepository, Repository } from "typeorm";

import { ICreateUserDTO } from "../dtos/ICreateUserDTO";
import { User } from "../entities/User";
import { IUsersRepository } from "./implementations/IUsersRepository";

class UserRepository implements IUsersRepository {
  private repository: Repository<User>; // Informamos do que vi se tratar o repositório

  constructor() {
    this.repository = getRepository(User); // pegamos o repositório user e métodos do typeorm para serem 
  }
  async create({ // função assíncrona que cria o novo usuário
    name,
    username,
    email,
    password,
    driver_license,
  }: ICreateUserDTO): Promise<void> {
    const user = this.repository.create({
      name,
      username,
      email,
      password,
      driver_license,
    });

    await this.repository.save(user); // salvando o usuário
  }
}

export { UserRepository };
```
## Aula LXXVII
> Criando Controller de Usuário

Com  a parte dos repositórios finalizada, vamos dá cntinuidade com os useCases. no nosso diretório de `accounts` vamos criar `useCases/createUser/` e aí os arquivos de `useCase` e `controller`. Além desses arquivos precisamos preparar nosso container que fica dentro a pasta `shared/`, no nosso inde.ts iremos repetir a ideia a já viemos fazendo. No nosso arquivo **`CreateUserUseCase.ts`** vamos seguir a seguinte estrutura:
```typescript
import { inject, injectable } from "tsyringe";

import { ICreateUserDTO } from "../../dtos/ICreateUserDTO";
import { IUsersRepository } from "../../repositories/implementations/IUsersRepository";

@injectable()
class CreateUserUseCase {
  constructor(
    @inject("UserRepository")
    private usersRepository: IUsersRepository
  ) {}

  async execute({
    name,
    username,
    email,
    password,
    driver_license,
  }: ICreateUserDTO): Promise<void> {
    await this.usersRepository.create({
      name,
      username,
      email,
      password,
      driver_license,
    });
  }
}

export { CreateUserUseCase };
```
**`container/index.ts`:**
```typescript
container.registerSingleton<IUsersRepository>(
  "UserRepository",
  UserRepository
);
```

## Aula LXXVIII
> Alterar Tabela de Usuário

Parando para bservar que a nossa tabela altualmente salva o name, email e username, nota-se que não se faz necessário salvar o username para esta aplicação. Sendo assim, vamos remover a coluna `usernme` da tabela `users` e para isso vamos utilizar o typeorm, onde iremos rodar o comando: `yarn typeorm migration:create -n AlterUserDeleteUsername`. Criada nossa migration, vamos seguir e criar as query.

```typescript
import { MigrationInterface, QueryRunner, TableColumn } from "typeorm";

export class AlterUserDeleteUsername1624059958422
  implements MigrationInterface
{
  public async up(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.dropColumn("users", "username");
  }

  public async down(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.addColumn(
      "users",
      new TableColumn({
        name: "username",
        type: "varchar",
      })
    );
  }
}
```
Criada nossa migration, podemos rodar ela com o comando `yarn typeorm migration:run`. Nesse momento vamos apens retirar a parte do código que faz referência a esta coluna.

## Aula LXXIX
> Criptografar senha

Aqui no banco de dados a nossa senha está totalmente exposta dando brechas para algum mal intensionado fazer qualquer operação. Para não deixar nossas senhas expostas dessa maneira iremos usar uma biblioteca, a bcrypt, que irá criptografar nossa senha antes de salvar no banco de dados. Para isso iremos importa a função hash, da lib bcrypt, no arquivo CreateUserUseCase.ts, usar a função hash no nosso password e salva-la.

```typescript
import { hash } from "bcrypt";
// [...]

function async execute({ name, email, password, driver_license }: ICreateUserDTO): Promise<void> {

  const passwordHash = await hash(password, 8); // esse "8" seria o número de vezes que embaralhamos esses caracteres

  await this.usersRepository.create({
    name,
    email,
    password: passwordHash,
    driver_license,
  });
}
// [...]
```

Podemos notar que estamos salvando emails iguais, para evitar isso vamos fazer uma simples validação antes de salvar o email e criar mais um método para classe `UsersRepository`, o `findByEmail()`.

**CreateUserUseCase.ts**
```typescript
const userAlreadyExists = await this.usersRepository.findByEmail(email);

if (userAlreadyExists) {
  throw new Error("Users already Exists");
}
```
**UsersRepository.ts**
```typescript
function async findByEmail(email: string): Promise<User> {
  const user = await this.repository.findOne({ email });

  return user;
}
```
## Aula LXXX
> Entendendo Antenticação com JWT

Hoje não tems o controle para saber se o usuário está ou não logado na nossa aplicação, para ter umcontrole maior nobre nosso usuário, sobre "quem tá fazendo o que". Para abordar esse problema vamos utilizar o JWT (Json Web Token). No momento que o usuário passa a senha e verificamos que ela está correta, geramos este token onde passamos algumas informações nesses tokens, mas nunca informações senssíveis.

## Aula LXXXI
> Criando Token do Usuário

Vamos iniciar aqui adicionando a biblioteca `jsonwebtoken`:
```sh
yarn add jsonwebtoken
yarn add @types/jsonwebtoken -D
```

Adicionamos o diretório `authenticateUser/` a pasta `useCases/`, onde vamos criar os arquivos de useCase e Controller, `AuthenticateUserUseCase.ts` e `AuthenticateUserController.ts`.

**`AuthenticateUserUseCase.ts`:**
```typescript
import { compare } from "bcrypt";
import { sign } from "jsonwebtoken";
import { inject, injectable } from "tsyringe";

import { IUsersRepository } from "../../repositories/IUsersRepository";

// Interfaces

interface IRequest {
  email: string;
  password: string;
}

interface IResponse {
  user: {
    name: string;
    email: string;
  };
  token: string;
}

@injectable() 
class AuthenticateUserUseCase {
  constructor(
    @inject("UsersRepository")
    private usersRepository: IUsersRepository
  ) {}

  async execute({ email, password }: IRequest): Promise<IResponse> {
    // Autentificação de usuário
    const user = await this.usersRepository.findByEmail(email);

    if (!user) {
      throw new Error("Email or password incorrect!");
    }

    // Autentificação de senha
    const passwordMatch = await compare(password, user.password);

    if (!passwordMatch) {
      throw new Error("Email or password incorrect!");
    }

    // Gerando Token
    const token = sign({}, "7f0a80fe059648190ad441eff2bf0dae", // md5
    {
      subject: user.id, // id
      expiresIn: "1d", // tempo de experição
    });

    const tokenReturn: IResponse = { // Repassando apenas os dados revelantes do usuário junto ao token
      token,
      user: {
        name: user.name,
        email: user.email,
      },
    };

    return tokenReturn;
  }
}

export { AuthenticateUserUseCase };
```

**`AuthenticateUserController.ts`**
```typescript
import { Request, Response } from "express";
import { container } from "tsyringe";

import { AuthenticateUserUseCase } from "./AuthenticateUserUseCase";

class AuthenticateUserController {
  async handle(request: Request, response: Response): Promise<Response> {
    const { password, email } = request.body;

    const authenticateUserUseCase = container.resolve(AuthenticateUserUseCase);

    const token = await authenticateUserUseCase.execute({
      password,
      email,
    });

    return response.json(token);
  }
}

export { AuthenticateUserController };
```

Com o useCase e controller finalizados vamos nos encaminhar para criação da rota. Para isso vamos criar o arquivo `authenticate.routes.ts` na pasta `routes/` com uma extrutura já bastante semelhante das criadas anterioemnte.
```typescript
import { Router } from "express";

import { AuthenticateUserController } from "../modules/accounts/useCases/authenticateUser/AuthenticateUserController";

const authenticateRoutes = Router();

const authenticateUserController = new AuthenticateUserController();
authenticateRoutes.post("/sessions", authenticateUserController.handle);

export { authenticateRoutes };
```
E finalizando trazendo esta rota para o nosso `index.ts` do diretório `routes/`.
```typescript
// [...]
import { authenticateRoutes } from "./authenticate.routes";
// [...]
router.use(authenticateRoutes);
```
## Aula LXXXII
> Autenticação das Rotas

Agora limitar o acesso de alguns usuários a algumas de nossas rotas utilizando o nosso token. Para isso vamo criar um middleware que vai sempre verificar se é um token válido para realizarmos a nossa requisição, se o usuário existe. Nesse sentido, na pasta `src/`, vamos iniciar criando uma `pastamiddlewares/` e nela o arquivo `ensureAuthenticated.ts`.

Antes de criarmos o nosso middleware, precisamos criar o método `findById()` no nosso repository. NO arquivo `IUsersRepository.ts` vamos adicionar a nossa interface o trecho: `findById(id: string): Promise<User>;` e no **`UsersRepository.ts`**:
```typescript
  async findById(id: string): Promise<User> {
    const user = await this.repository.findOne(id);

    return user;
  }
```
E finalmente...
**`ensureAuthenticated.ts`:**
```typescript
import { NextFunction, Request, Response } from "express";
import { verify } from "jsonwebtoken";

import { AppError } from "../errors/AppErrors";
import { UsersRepository } from "../modules/accounts/repositories/implementations/UsersRepository";

interface IPayload {
  sub: string;
}

export async function ensureAuthenticated(
  request: Request,
  response: Response,
  next: NextFunction // Função obrigatória em qualquer middleware
): Promise<void> {
  const authHeader = request.headers.authorization; // buscando token => "Bearer jdhaskdnaosidjasjdask"

  if (!authHeader) { // se não existir token emitimos um erro
    throw new AppError("Token missing", 401);
  }

  const [, token] = authHeader.split(" "); // desestruturando nosso token. dividindo com split onde aparecer um espaço em branco e vamos capturar apenas o segundo parâmentro

  try {
    // na função verify, passamos 2 parâmetros, o token e a chave secretea que foi passado para criação do token
    const { sub: user_id } = verify(
      token,
      "7f0a80fe059648190ad441eff2bf0dae"
    ) as IPayload; // com essa interface nós informamos o tipo de retorno que retemos 

    const usersRepository = new UsersRepository();
    const user = usersRepository.findById(user_id); // buscando usuário pelo id que encontramos no token

    if (!user) { // se não existir retornamos um erro
      throw new AppError("User does not exists!", 401);
    }

    next();
  } catch (error) {
    throw new AppError("Invalid token", 401);
  }
}
```

## Aula LXXXIII
> Tratamento de exceções

O objetivo nesse momento é que a api repasse os erros que aparecerem, fazendo com que o erro não cai no log e a aplicação não pare.

Vamos iniciar criando dentro de `src/` a pasta `errors/` e nela o arquivo `AppErrors`.
**`AppErrors`:**
```typescript
export class AppError {
  public readonly message: string; // propriedade apenas para leitura

  public readonly statusCode: number; // propriedade apenas para leitura

  constructor(message: string, statusCode = 400) { // setando o statusCode em 400
    this.message = message; // propriedade message recebe message passada no constructor
    this.statusCode = statusCode; // propriedade statusCode recebe statusCode passada no constructor
  }
}
```
Agora vamos substitutir todos os `Erros` em nosso código pelo `AppError`. Nos erros do arquivo `ensureAuthenticated.ts` vamos por o código 401 em todos, pois se trata de autorização, da seguinte maneira: `throw new AppError("Token missing", 401);`.

Vamos criar agora um middleare para que o erro consiga ser repassado para frente. No server, depois das rotas, vamos criar:
```typescript
// [...]
import { AppError } from "./errors/AppErrors";

// [...]
app.use(
  (err: Error, request: Request, response: Response, next: NextFunction) => { // em middleware de erro sempre passamos o Error primeiro
    if (err instanceof AppError) { // se o erro for um AppError
      return response.status(err.statusCode).json({ // retornamos no satus, o statusCode que passamos no AppError
        message: err.message, // e a mensagem também
      });
    }
    // Se o erro for de qualquer outro tipo
    return response.status(500).json({ // erro da aplicação que não temos controle
      status: "error",
      message: `Internal server error - ${err.message}`,
    });
  }
);
```
E para finalmente concluir a missão de repassar os erros, vamos instalar a lib `express-asyndc-errors` com o comando `yarn add express-async-errors`. Para utilizar, vamos importar essa lib no nosso `server.ts` após o express.

## Aula LXXXIV
> Adcionando Coluna de Avatar

Para armazenar os arquivos de imagem de avatar, vamos utilizar os storages para armazenar o arquivo e reverenciar esse por uma url em nosso banco de dados para podemos está recuperando esse arquivo quando necessário. Esse processo recomendável devido ao peso desse tipo de arquivo em nosso banco podendo tornar mais pesado e afetando  o desempenho.

Antes de adicionar a coluna, na pasta de `accounts/useCases/` vamos adiccionar o diretório `updateUserAvatar/` e nele o arquivo `UpdateUserAvatarUseCase.ts` com a seguinte estrutura:

```typescript
class UpdateUserAvatarUseCase {
  async execute() {}
}

export { UpdateUserAvatarUseCase };
```
Em seguida, vamos delimitar quando serão os próximos passos.

- [] Adicionar coluna avatar na tabela de users
- [] Refatorando usuário com coluna avatar
- [] Configuração upload multer
- [] Criar regra de negócio do upload
- [] Criar Controller

Vamos prosseguir adicionando a coluna avatar na tabela de usuário, para isso vamos criar uma migration do nosso typeorm e sequência executar a mesma. Para criar nossa migration, vamos executar o seguinte comando: `yarn typeorm migration:create -n AlterUserAddAvatar`. A estrutura da migration deve seguir o seguinte padrão:

```typescript
import { MigrationInterface, QueryRunner, TableColumn } from "typeorm";

export class AlterUserAddAvatar1624201713726 implements MigrationInterface {
  public async up(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.addColumn(
      "users",
      new TableColumn({
        name: "avatar",
        type: "varchar",
        isNullable: true,
      })
    );
  }
  public async down(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.dropColumn("users", "avatar");
  }
}
```

Executando migration: `yarn typeorm migration:run`

Após a execução da nossa migration, podemos verificar a alteração no nosso banco de dados. Além disso, vamos refatorar nossa entidade `User`, adicionando a coluna `avatar` do tipo *string*. E agora vamos adicionar o nosso avatar ao banco de dados no arquivo de useCase da seguinte maneira:
```typescript
import { inject, injectable } from "tsyringe";
import { IUsersRepository } from "@modules/accounts/repositories/IUsersRepository";

interface IRequest {
  user_id: string;
  avatar_file: string;
}

@injectable()
class UpdateUserAvatarUseCase {
  constructor(
    @inject("UsersRepository")
    private usersRepository: IUsersRepository
  ) {}

  async execute({ user_id, avatar_file }: IRequest): Promise<void> {
    const user = await this.usersRepository.findById(user_id);

    user.avatar = avatar_file;

    await this.usersRepository.create(user);
  }
}
export { UpdateUserAvatarUseCase };
```
Para recebermos o nosso usuário na requisição do controller, vamos aproveitar o middleware de autentificação para que ele passe a informação do usuário. Para podermos fazer uso da informação vinda do middleware, é preciso passar o objeto para o `request`, para evitar erros de tipagens, vamos adicionar a tipagem do `request` o nosso objeto `user` que será passado, para isso, vamos adicionar ao diretório `src/`, a pasta `@types/` e nela a pasta `express/` com o arquivo `index.d.ts` onde iremos alterar a tipagem do `request`.

**`index.d.ts`:**
```typescript
declare namespace Express {
  export interface Request {
    user: {
      id: string;
    }
  }
}
```

Daí então, já pomos capturar o user.id no controller:

**`UpdateUserAvatarController`:**
```typescript
import { Request, Response } from "express";
import { container } from "tsyringe";

import { UpdateUserAvatarUseCase } from "./UpdateUserAvatarUseCase";

class UpdateUserAvatarController {
  async handle(request: Request, response: Response): Promise<Response> {
    const { id } = request.user;              // desestruturando request e capturando id do usuário

    // Recebendo arquivo
    const avatar_file = null;

    const updateUserAvatarUseCase = container.resolve(UpdateUserAvatarUseCase);

    await updateUserAvatarUseCase.execute({ user_id: id, avatar_file });

    return response.status(204).send();
  }
}
export { UpdateUserAvatarController };
```

Agora no `users.routes.ts`, vamos utilizar o método `patch` e para o upload do avatar vamos utulizar novament eo multer, o qual funciona como um middleware, para permanecermos com um bom código, vamos configurar o multer em outra local, dividindo assim melhor cada arquivo por responsabilidades diferentes. Na pasta `src/` vamos criar o diretório `config/` e nele o arquivo `upload.ts` com a seguinte estrutura:

```typescript
import crypto from "crypto";
import multer from "multer";
import { resolve } from "path";

export default {
  upload(folder: string) {

  },
};

```

## Aula LXXXV
> Upload de Avatar

Continuando a estrutura do arquivo `upload.ts`:

```typescript
import crypto from "crypto";
import multer from "multer";
import { resolve } from "path";

export default {
  upload(folder: string) {
    return {
      // setar onde será salvo o arquivo e o padrão de salvamento do filename
      storage: multer.diskStorage({
        destination: resolve(__dirname, "..", "..", folder),
        filename: (request, file, callback) => {
          const fileHash = crypto.randomBytes(16).toString("hex");
          const fileName = `${fileHash}- ${file.originalname}`;

          return callback(null, fileName);
        },
      }),
    };
  },
};
```
Passamos essas configurações para o arquivo de rotas.

```typescript
import { Router } from "express";
import multer from "multer";

import uploadConfig from "@config/upload";
import { CreateUserController } from "@modules/accounts/useCases/createUser/CreateUserController";
import { UpdateUserAvatarController } from "@modules/accounts/useCases/updateUserAvatar/UpdateUserAvatarController";

import { ensureAuthenticated } from "../middlewares/ensureAuthenticated";

const usersRoutes = Router();

const uploadAvatar = multer(uploadConfig.upload("./tmp/avatar"));

const createUserController = new CreateUserController();
usersRoutes.post("/", createUserController.handle);

const updateUserAvatarController = new UpdateUserAvatarController();
usersRoutes.patch(
  "/avatar",
  // autentificação: passando o usuário
  ensureAuthenticated,
  // upload do avatar: passando o arquivo
  uploadAvatar.single("avatar"),
  updateUserAvatarController.handle
);

export { usersRoutes };
```
Para que o avatar_file e o id possa ser reconhecido precisamos identificar ele em nossa interface `ICreateUserDTO`.
```typescript
interface ICreateUserDTO {
  name: string;
  email: string;
  password: string;
  driver_license: string;
  id?: string; // opicional
  avatar?: string; // opicional
}
export { ICreateUserDTO };
```
Repassamos essas alterações pra o método responssável pela criação do usuário em nosso repositório.
```typescript
function async create({
  name,
  email,
  driver_license,
  password,
  avatar,
  id,
}: ICreateUserDTO): Promise<void> {
  const user = this.repository.create({
    name,
    email,
    driver_license,
    password,
    avatar,
    id,
  });

  await this.repository.save(user);
}
```

Para finalizar vamos receber no controller:

```typescript
import { Request, Response } from "express";
import { container } from "tsyringe";

import { UpdateUserAvatarUseCase } from "./UpdateUserAvatarUseCase";

class UpdateUserAvatarController {
  async handle(request: Request, response: Response): Promise<Response> {
    // pegando o id do usuário para filtrar
    const { id } = request.user;
    // pegando no nome do arquivo para salvar no banco de dados
    const avatar_file = request.file.filename;

    const updateUserAvatarUseCase = container.resolve(UpdateUserAvatarUseCase);

    await updateUserAvatarUseCase.execute({ user_id: id, avatar_file });

    return response.status(204).send();
  }
}
export { UpdateUserAvatarController };
```
## Aula LXXXVI
> Remover Arquivo de Avatar Existente

Vamos criar uma função para deletar arquivos e que poderemos reutilizar futuramente. Para isso, vamos criar o aquivo `file.ts` na pasta `utils/` dentros de `src/`, com a seguinte estrutura:
```typescript
import fs from "fs";

export const deleteFile = async (filename: string): Promise<void> => {
  try {
    await fs.promises.stat(filename); // verifica se o arquivo existe
  } catch {
    return; // se não existor, sai da função
  }
  await fs.promises.unlink(filename); // se existir, deleta o arquivo
};
```

Para que não adicionemos vários arquivos vamos inserir no useCase o seguinte trecho de código na função `execute()`:
```typescript
if (user.avatar) {
  await deleteFile(`./tmp/avatar/${user.avatar}`); // contatenção do path com o nome do arquivo
}
```

## Aula LXXXVII
> Introdução

- [ ] Testes
- [ ] Tipos de testes
- [ ] Que momento usar
- [ ] TDD ( Test Driven Development | Desenvolvimento Orientado por Testes)
- [ ] Como aplicar TDD
- [ ] Regras de negócio e análise de requisitos

## Aula LXXXVIII
> Conhecendo os Tipos de Testes

Vamos utilizar basicamente dois tipos de testes aqui, sendo eles os **Testes Unitário** e os **Testes de Integração**.

*Testes Unitários*: Os testes unitários procuram aferir a corretude do código, em sua menor fração. Em linguagens orientadas a objetos, essa menor parte do código pode ser um método de uma classe. Sendo assim, os testes unitários são aplicados a esses métodos, a partir da criação de classes de testes. No caso da nossa aplicação vai testar nossas regras de negócio.

*Testes de Integração*: Teste de integração é a fase do teste de software em que módulos são combinados e testados em grupo. Ela sucede o teste de unidade, em que os módulos são testados individualmente, e antecede o teste de sistema, em que o sistema completo é testado num ambiente que simula o ambiente de produção. Ou seja vamos testar todo no fluxo, desde a chamada da rota até o retorno.

Utilização do TDD, Test Driven Development, ou seja, Desenvolvimento Orientado por Testes, onde iremos criar nossos teste e desenvolver a aplicação encima dos testes criados, fazendo com que previna de problemas futuros com  as regras de negócio e a aplicação como um todo.

## Aula LXXXIX
> Criando o primeiro teste

A biblioteca usada para nossos testes erá o [Jest](https://jestjs.io/pt-BR/). Para instalar ele no nosso projeto vamos executar o comando, `yarn add jest @types/jest -D`, onde iremos instalar também a sua tipagem. E para iniciar vamos rodar o `yarn jest --init`, onde precisamos ter atenção para selecionar o test environment como node, o provider como V8. Agora vamos instalar um preset com o comando,`yarn add ts-jest -D` e para ativar o preset, vamos o arquivo `jest.config.ts` setar `preset: ts-jest`. Além disso vamos configurar as classes que serão mapeadas para a realização dos testes: `testMatch: ["**/*.spec.ts"]` e para finalizar nos configuraçõepor hora, vamos setar `bail: true` fazendo com que o jest pare no primeiro erro no teste.

Exemplo de estrutura de teste:

```typescript
// Agrupar testes
describe("Criar categoria", () => {
  // it criam os testes
  it("Espero que 2 + 2 seja 4", () => {
    const soma  = 2 + 2;
    const result = 4;

    // aqui eu digo: espero que (expect) - soma (soma) - seja (toBe) - result (result)
    expect(soma).toBe(result)
  })

  it("Espero que 2 + 2 não seja 5", () => {
    const soma  = 2 + 2;
    const result = 5;

    // aqui eu digo: espero que (expect) - soma (soma) - não (not) - seja (toBe) - result (result)
    expect(soma).not.toBe(result)
  })
})
```
E para rodar o teste, podemos dar o comando, `yarn test`.

## Aula XC
> Teste de Criação de Categoria

Para iniciar a criação dos nossos teste unitários, vamos ceiar na pasta `creatCategory/`, o arquivo CreatCategoryUseCase.spec.ts. Para podermos executar nossos testes, não podemos utilizar o banco de dados, afim de suprir a demanda de um repositório vamos criar um "fake" que será na verdade um repositório em memória no qual iremos implementar a interface de repositório daquele específico. Então no diretório `repositories/` vamos criar a pasta `in-memory/` e nela o arquivo CategoriesRepositoryInMemory.ts. Após implemetar a nossa interface no novo repositório, vamos estrutura-lo da seguinte maneira:
```typescript
import { Category } from "../../infra/typeorm/entities/Category";
import { ICategoriesRepository, ICreateCategoryDTO } from "../ICategoriesRepository";

class CategoriesRepositoryInMemory implements ICategoriesRepository {
  categories: Category[] = []; // Cria repositório de categorias
  async findByName(name: string): Promise<Category> {
    const category = this.categories.find((category) => category.name === name);
    return category;
  }
  async list(): Promise<Category[]> {
    const { categories } = this;
    return categories;
  }
  async create({ name, description }: ICreateCategoryDTO): Promise<void> {
    const category = new Category();
    Object.assign(category, {
      name,
      description,
    });
    this.categories.push(category);
  }
}
export { CategoriesRepositoryInMemory };
```

Com repositório criado, podemos utilizar em nossos testes de useCase onde vamos seguir a seguinte estrutura:
```typescript
let createCategoryUseCase: CreateCategoryUseCase;
let categoriesRepositoryInMemory: CategoriesRepositoryInMemory;

describe("Create Category", () => {
  // Antes de cada teste iremos instanciar as sguints variáeis
  beforeEach(() => {
    categoriesRepositoryInMemory = new CategoriesRepositoryInMemory();
    createCategoryUseCase = new CreateCategoryUseCase(
      categoriesRepositoryInMemory
    );
  });

  it("should be able to create a new category", async () => {
    const category = {
      name: "Category Test",
      description: "Category description Test",
    };

    // Criando categoria
    await createCategoryUseCase.execute({
      name: category.name,
      description: category.description,
    });
    // Buescando categoria pelo nme que foi criado
    const categoryCreated = await categoriesRepositoryInMemory.findByName(
      category.name
    );
    // Espera-se que a categoria criada tenha a prpriedade "id"
    expect(categoryCreated).toHaveProperty("id");
  });

  it("should not be able to create a new category with name exists", async () => {
    // Ao executar esse código espera-se que
    expect(async () => {
      const category = {
        name: "Category Test",
        description: "Category description Test",
      };

      await createCategoryUseCase.execute({
        name: category.name,
        description: category.description,
      });

      await createCategoryUseCase.execute({
        name: category.name,
        description: category.description,
      });
    // seja rejeitado com a instância do erro do tipo "AppError"
    }).rejects.toBeInstanceOf(AppError);
  });
});
```

## Aula XCI
> Teste de Autentificação do Usuário

Saindo um pouco do módulo `cars` vamos criar o teste de utentificação de usuário. Para isso vamos no useCase do mesmo, criar o arquivo `AuthenticateUserUseCase.spec.ts`, mas antes de iniciar os nossos testes, precisamos criar nosso repositório in-Memory assim como feito anteriormente.

```typescript
import { ICreateUserDTO } from "../../dtos/ICreateUserDTO";
import { User } from "../../infra/typeorm/entities/User";
import { IUsersRepository } from "../IUsersRepository";

class UsersRepositoryInMemory implements IUsersRepository {
  users: User[] = []; // Cria array de usuários

  // Cria usuários
  async create({driver_license, email, name, password }: ICreateUserDTO): Promise<void> {
    const user = new User();
    Object.assign(user, {
      driver_license,
      email,
      name,
      password,
    });
    this.users.push(user);
  }
  // Busca usuário por emil
  async findByEmail(email: string): Promise<User> {
    return this.users.find((user) => user.email === email);
  }
  // Busca usuário por id
  async findById(id: string): Promise<User> {
    return this.users.find((user) => user.id === id);
  }
}
export { UsersRepositoryInMemory };
```
Com repositório criado, vamos iniciar a criação dos nossos tentes.

```typescript
let authenticateUserUseCase: AuthenticateUserUseCase;
let usersRepositoryInMemory: UsersRepositoryInMemory;
let createUserUseCase: CreateUserUseCase;
describe("Authenticate User", () => {
  // Antes de cada teste
  beforeEach(() => {
    // Cria repositório
    usersRepositoryInMemory = new UsersRepositoryInMemory();
    // Cria useCae de atntificação
    authenticateUserUseCase = new AuthenticateUserUseCase(
      usersRepositoryInMemory
    );
    // Cria useCase de criação de usuário
    createUserUseCase = new CreateUserUseCase(usersRepositoryInMemory);
  });
  // Deve ser capaz de autenticar um usuário
  it("should be able to authenticate an user", async () => {
    const user: ICreateUserDTO = {
      driver_license: "000123",
      email: "user@test.com",
      password: "1234",
      name: "User Test",
    };
    // Cria usuário
    await createUserUseCase.execute(user);
    // Executa atentificação
    const result = await authenticateUserUseCase.execute({
      email: user.email,
      password: user.password,
    });
    // Espera que o objeto "result" tenha a propriedade "token"
    expect(result).toHaveProperty("token");
  });
  // Não deve ser capaz de autenticar um usuário não existente
  it("should not be able to authenticate an nonexistent user", () => {
    expect(async () => {
      // Autenticando usuário não criado
      await authenticateUserUseCase.execute({
        email: "false@email.com",
        password: "1234",
      });
    // Espera que o tipo do erro que será emitido seja do tipo "AppError"
    }).rejects.toBeInstanceOf(AppError);
  });
  // Não deve ser capaz de autenticar um usuário com uma senha incorreta
  it("should not be able to authenticate with incorrect password", () => {
    expect(async () => {
      const user: ICreateUserDTO = {
        driver_license: "9999",
        email: "user@user.com",
        password: "1234",
        name: "User Test Error",
      };
      // Cirando usuário
      await createUserUseCase.execute(user);
      // Passandosenha incorreta para autentificação
      await authenticateUserUseCase.execute({
        email: user.email,
        password: "incorrectPassword",
      });
    // Espera que o tipo do erro que será emitido seja do tipo "AppError"
    }).rejects.toBeInstanceOf(AppError);
  });
});
```

## Aula XCII
> Imports da Aplicação

Antes de seguir com os testes vamos aprender uma configuração para facilitar nossos imports. Algumas vezes no nosso import precisamos voltar várias pastas para podermos importar alguma classe/funcionalidade. Para faciliar esses imports vamos utilizar uma configuração no typescript, que nada mais é que um mapeamento das pastas que queremos referenciar. Em `tsconfig.json` vamos fazer da seguinte maneira:
```JSON
{
  "compilerOptions": {
    ...,
    "baseUrl": "./src",
    "paths": {
      // Toda vez que eu disse "@modules" eu estou me referindo a src/modules/
      "@modules/*": ["modules/*"],
      "@config/*": ["config/*"],
      "@shared/*": ["shared/*"],
      "@errors/*": ["errors/*"],
      "@utils/*": ["utils/*"]
    },
    ...
  }
}
```
E em .eslintrc.json vamos alterar uma configuração Que irá dizer o seguinte para o eslint: Toda importação que tem "@" eu quero que seja uma importação da minha aplicação.
```JSON
{

"import-helpers/order-imports": [
  "warn",
  {
    "newlinesBetween": "always",
    "groups": ["module", "/^@/", ["parent", "sibling", "index"]],
    "alphabetize": { "order": "asc", "ignoreCase": true }
  }
]
}
```
Agora já podemos referenciar todos os imports apartir das pastas mapeadas.

Para que p ts-node-dev entenda essas importações vamos instalar `yarn add tscnfig-paths -D` e nos scripts usar da seguinte maneira:
```JSON
```
Ex.: `import { ICreateUserDTO } from "@modules/accounts/dtos/ICreateUserDTO";`

## Aula XCIII
> Corrigindo as importações

Inicialment vamos configurar o jest para que ele entenda a maneira com a qual estamos importando agora, para isso:
**`jes.config.ts`**
```ts
import { pathsToModuleNameMapper } from "ts-jest/utils";
import { compilerOptions } from "./tsconfig.json";
export default {
  ...,
  moduleNameMapper: pathsToModuleNameMapper(compilerOptions.paths, {
    prefix: "<rootDir>/src/",
  }),
  ...,
}
```
> Obs.: caso o json tenha comentários precisamos retirálos.

Agora com o jest e o ts-node-dev reconhecendo nossas importações, vamos terminar de finalizar as informações no restante dos arquivos.

## Aula XCIV
> Refatorando a aplicação

O que vamos fazer agora é separar ainda mais as responsabilidades. Primeira regra: o que for de uma camada externa vamos agrupar na pasta `infra/` que vamos criar dentro de cars e accounts (e será repetido para os demais módulos). Dentro de `infra/` vamos criar a pasta `typeorm/` e enviar  a entidade que está dentro do diretório do módulo. Ainda dentro da pasta `typeorm/` criaremos o diretório `repositories` e mover o arquivo onde está implementado (na pasta implementations) o repositório do módulo e caso necessário, corrigir as importações.
Seguindo ainda a lógica da pasta `infra/`, vimos criar dentro da pasta `shared/`, outro dretório `infra/` e nela uma pasta `http/` onde iremos depositar partes referentes ao express, a começar com a pasta `midlewares/`, `routes/` e o arquivo `server.ts` e mover a pasta `errors/` para a pasta `shared/` já que usaremos para toda nossa aplicação. Junto com a pasta `http/` vamos realocar a pasta `database/` onde estão os arquivos referentes ao typeorm, renomenado o diretório para `typeorm/`.
Para finalizar vamos mudar a parte do nosso script que referencia o arquivo `server.ts`, mudando o trecho `src/server.ts` para `src/shared/infra/http/server.ts`. E depois disso só vamos arrumar as importações da nossa aplicação.

## Aula XCV
> Escrevendo os requisitos da aplicação

**RF** - Requisitos Funcionais

Parte da etapa de elicitação, os requisitos funcionais são todos os problemas e necessidades que devem ser atendidos e resolvidos pelo software por meio de funções ou serviços.

Tudo o que for relacionado a uma ação a ser feita é considerado uma funcionalidade. Também é importante lembrar que quanto menos ambíguos e mais objetivos forem os requisitos funcionais, maior será a qualidade do software gerado.

**RNF** - Requisitos Não Funcionais

Os requisitos não funcionais são todos aqueles relacionados à forma como o software tornará realidade os que está sendo planejado. Ou seja, enquanto os requisitos funcionais estão focados no que será feito, os não funcionais descrevem como serão feitos.

**RN** - Regra de Negócio

Regras de negócio são critérios e restrições informados são regras, e regras da empresa (negócio) que faz as entregas. Logo, são regras de negócio.

### Cadastro de carro

**RF**

- Deve ser possível cadastrar um novo carro

**RN**

- O usuário respossável pelo cadastro dever ser um usuário administrador.
- Não deve ser possível cadastrar um carro com uma placa existente.
- Não de ve ser possível alterar a placa de um carro cadastrado.
- O carro deve ser cadastrado como disponível por padrão.

### Listagem de Carros

**RF**

- Deve ser possível listar todos os carros disponíveis
- Deve ser possível listar todos os carros disponíveis pelo nome da categoria
- Deve ser possível listar todos os carros disponíveis pelo nome da marca
- Deve ser possível listar todos os carros disponíveis pelo nome do carro

**RN**

- O usuário não precisa estar logado no sistema

### Cadastro de Especificação no Carro

**RF**

- O usuário respossável pelo cadastro dever ser um usuário administrador.
- Deve ser possível cadastrar uma espeificação para um carro.
- Deve ser possível listar todas especificações.
- Deve ser possível listar todos os carros.

**RN**

- Não deve ser possível cadastrar uma especificação para um carro não cadastrado.
- Não deve ser possível cadastrar uma especificação existente para um mesmo carro.
- O usuário respossável pelo cadastro dever ser um usuário administrador.

### Cadastro de imagens do carro

**RF**

- Deve ser possível cadastrar a imagem do carro.
- Deve ser possível listar todos os carros.
**RNF**

- Utilizar o multer para upload dos arquivos.

**RN**

- O usuário deve poder cadastrar mais de uma imagem para o mesmo carro.
- O usuário respossável pelo cadastro dever ser um usuário administrador.

### Aluguel de carro

**RF**

- Deve ser possível cadastrar um alugel

**RN**

- O aluguel deve ter duração mínima de 24 horas.
- Não deve ser possível cadastrar um novo alugel caso já exista um aberto  parao mesmo usuário
- Não deve ser possível cadastrar um novo alugel caso já exista um aberto  parao mesmo carro

## Aula XCVI
> Alterando a importação dos repositórios

Aqui vamos corrigir as importações que não estão seguindo nosso padrão os arquivos de repositório em memória e remover as pastas de implementação.

## Aula XCVII
> Criando migrations do carro

Para dar continuidade na nossa aplicação vamos agora criar a tablea de `cars`criando nossa migrations com o comando `yarn typeorm migration:create -n CreateCars`, mas antes vamos alterar o caminho das migrations no `ormconfig.json`.

```json
{
  "type": "postgres",
  "port": 5432,
  "host": "localhost",
  "username": "docker",
  "password": "ignite",
  "database": "rentalx",
  // path alterada
  "migrations": ["./src/shared/infra/typeorm/migrations/*.ts"],
  "entities": ["./src/modules/**/entities/*.ts"],
  "cli": {
    // path alterada
    "migrationsDir": "./src/shared/infra/typeorm/migrations"
  }
}
```
E finalmente podemos criar a estrutura da migration para moldar nossa tabela de `cars`.

**`CreateCars`:**
```ts
import { MigrationInterface, QueryRunner, Table } from "typeorm";

export class CreateCars1625310735313 implements MigrationInterface {
  public async up(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.createTable(
      new Table({
        name: "cars",
        columns: [
          {
            name: "id",
            type: "uuid",
            isPrimary: true,
          },
          {
            name: "name",
            type: "varchar",
          },
          {
            name: "description",
            type: "varchar",
          },
          {
            name: "daily_rate",
            type: "numeric",
          },
          {
            name: "available",
            type: "boolean",
            default: true,
          },
          {
            name: "license_plate",
            type: "varchar",
          },
          {
            name: "fine_amount",
            type: "numeric",
          },
          {
            name: "brand",
            type: "varchar",
          },
          // coluna que referencia outra (foreignkeys)
          {
            name: "category_id",
            type: "uuid",
            // pode ser nulo
            isNullable: true,
          },
          {
            name: "created_at",
            type: "timestamp",
            default: "now()",
          },
        ],
        // linkando as colunas
        foreignKeys: [
          {
            // nome do link
            name: "FKCategoryCar",
            // referenciando tabela origem
            referencedTableName: "categories",
            // referencindo coluna da tabela origem
            referencedColumnNames: ["id"],
            // referenciando a coluna da tabela 
            columnNames: ["category_id"],
            // caso a categoria de fora seja apagada, na nossa tabela o valor irá mudar para nulo
            onDelete: "SET NULL",
            // caso a categoria de fora seja atualizada, na nossa tabela o valor irá mudar para nulo
            onUpdate: "SET NULL",
          },
        ],
      })
    );
  }
  public async down(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.dropDatabase("cars");
  }
}
```

## Aula XCVIII
> TDD na Prática

Vamos começar criando nossos casos de uso um oouco diferente, vamos iniciar com os testes, vamos usar a metodologia TDD.

1 - Escrevemos um teste simples (que vai falhar)

2 - Fazemos ele passar

3 - Refatoramos (adicionando regras de negócios e validações)

No módulo `cars/` vamos adicionar ao diretório `useCases/` uma pasta `createCar/` com os arquivos: `CreateCarUseCase.spec.ts` `CreateCarUseCase.ts`

**`CreateCarUseCase.ts`:**
```ts
// o que a método execute vai receber ⤵
interface IRequest {
  name: string;
  description: string;
  daily_rate: number;
  license_plate: string;
  fine_amount: number;
  brand: string;
  category_id: string;
}

@injectable()
class CreateCarUseCase {
  // Aqui eu digo que essa classe deve ser instanciada recebendo o objeto do tipo ICarsRepository 👍
  constructor(
    @inject("CarsRepository")
    private carsRepository: ICarsRepository
  ) {}

  async execute({
    // recebendo do usuário
    brand,
    category_id,
    daily_rate,
    description,
    fine_amount,
    license_plate,
    name,
  }: IRequest): Promise<void> {
    // esse carsRepository que vai ser instanciado terá um método create no qual vai receber ICreateDTO
    this.carsRepository.create({
      brand,
      category_id,
      daily_rate,
      description,
      fine_amount,
      license_plate,
      name,
    });
  }
}
export { CreateCarUseCase };

```

**`CreateCarUseCase.spec.ts`:**
```ts
// criando as varáveis para serem instanciadas
let createCarUseCase: CreateCarUseCase;
let carsRepositoryInMemory: CarsRepositoryInMemory;

describe("Create Car", () => {
  // antes de cada teste faça isso ⬇️
  beforeEach(() => {
    // instanciando useCase e o repositório
    carsRepositoryInMemory = new CarsRepositoryInMemory();
    // Classe responssável por manipular os dados
    createCarUseCase = new CreateCarUseCase(carsRepositoryInMemory);
  });

  it("should be able to create a new car", async () => {
    // executando o método
    await createCarUseCase.execute({
      brand: "Brand",
      category_id: "category",
      daily_rate: 100,
      description: "Description Car",
      fine_amount: 60,
      license_plate: "ABC-1234",
      name: "Name Car",
    });
  });
});
```
No diretório `repositories/` vamos criar o arquivo `ICarsRepository.ts`.

Aqui vai a interface do nosso repositório, que é uma forma de tipar uma classe/objeto para que o nosso constructor saiba o que vai entrar, quais os métodos que podem ser chamados e o que eles vão receber.
**`ICarsRepository.ts`:**
```ts
import { ICreateCarDTO } from "../dtos/ICreateCarDTO";

interface ICarsRepository {
  // no método create vamos receber dados do tipo *ICreateCarDTO* que é outra interface que vai dizer quais e de que tipo são
  // o retorno será uma promise vazia, ou seja esse será um método async sem retorno
  create(data: ICreateCarDTO): Promise<void>;
}
export { ICarsRepository };
```
No diretório do módulo `cars` vamos criar a pasta `dtos/` onde vamos criar o seguinte arquivo.

**`ICreateDTO.ts`:**

```ts
interface ICreateCarDTO {
  name: string;
  description: string;
  daily_rate: number;
  license_plate: string;
  fine_amount: number;
  brand: string;
  category_id: string;
}
export { ICreateCarDTO };
```
Na pasta repositories, criamos o diretório `in-memory/` onde vamos criar a classe `CarsRepositoryInMemory`.

O CarsRepositoryInMemory será nosso repositório que vamos criar para executar nossos testes. Nele vamos implementar o ICarsrepository e as informações serão armazenadas em um array, ou seja na memória.

**`CarsRepositoryInMemory`:**
```ts
//implementamos o ICarsRepository
class CarsRepositoryInMemory implements ICarsRepository {
  // criamos um array do tipo Car (Entidade de Car)
  cars: Car[] = [];
  // método que irá criar o car enviando-o o array cars
  async create({
    brand,
    category_id,
    daily_rate,
    description,
    fine_amount,
    license_plate,
    name,
  }: ICreateCarDTO): Promise<void> {
    // instanciando car
    const car = new Car();
    // colocando os dados recebidos dentro do objeto car
    Object.assign(car, {
      brand,
      category_id,
      daily_rate,
      description,
      fine_amount,
      license_plate,
      name,
    });
    // enviando para o array cars
    this.cars.push(car);
  }
}
export { CarsRepositoryInMemory };
```
A entidade, semelhante a interface vai dizer a forma daquele objeto, como será moldado. Ele será criado em `cars/infra/typeorm/entities/`.

```ts
class Car {
  id: string;
  name: string;
  description: string;
  daily_rate: number;
  license_plate: string;
  fine_amount: number;
  brand: string;
  category_id: string;
  created_at: Date;
}
export { Car };
```

## Aula XCIX
> Continuando caso de uso de carros

No nosso caso de uso vamos deixar comentado os trechos de código que pertencem ao tsyringe, o `@inject()` e o `@injectable()` pois só será necessário quando finalizarmos nossos testes e integrarmos essa parte da aplicação ao nosso banco de dados.

Damos prosseguimento com as regras de negócio onde vamos modificar o nosso `CreateCarUseCase.ts`. A primeira **RN** diz que não pode ser cadastro dois carros  com a mesma placa, para isso vamos fazer uma validação antes da criação do `car`
```ts
// O método findByLicensePlate ainda não existe e será criada
// Para isso vamos modificar ICarsRepository.ts e o CarsRepositoryInMemory.ts
const carAlreadyExists = await this.carsRepository.findByLicensePlate(
  license_plate
);
// Caso exista, retornará um erro
if (carAlreadyExists) {
  throw new AppError("Car already exists!");
}
```
Aqui vamos adicionar o método informando qual vai ser a entrada e a saída.
**`ICarsRepository.ts`:**
```ts
interface ICarsRepository {
  create(data: ICreateCarDTO): Promise<void>;
  findByLicensePlate(license_plate: string): Promise<Car>;
}
export { ICarsRepository };
```
E no CarsRepositoryInMemory.ts vamos implementar o método `findByLicensePlate`.
```ts
function async findByLicensePlate(license_plate: string): Promise<Car> {
  return this.cars.find((car) => car.license_plate === license_plate);
}
```

A próxima regra de negócio diz que o carro deve ser criado **available = true**  como padrão. Para podermos verificarmos isso, vamos usar a estratégia de retornar o carro na criação e assim verificarmos a propriedade no teste. Para isso vamos começar alterando o arquivo `ICarsRepository.ts`.
```ts
interface ICarsRepository {
  // alteração do retorno do método
  create(data: ICreateCarDTO): Promise<Car>;
  findByLicensePlate(license_plate: string): Promise<Car>;
}
export { ICarsRepository };
```
E no **`CarsrepositoryInMemory.ts`:**

```ts
function async create({
  brand,
  category_id,
  daily_rate,
  description,
  fine_amount,
  license_plate,
  name,
  // mudando o retorno
}: ICreateCarDTO): Promise<Car> {
  const car = new Car();
  Object.assign(car, {
    brand,
    category_id,
    daily_rate,
    description,
    fine_amount,
    license_plate,
    name,
  });
  this.cars.push(car);
  // retornando um car como prometido
  return car;
}
```

E por fim alterndo no useCase:
**`CreateCarUseCase.ts`**
```ts
function async execute({brand,category_id,daily_rate,description,fine_amount,license_plate,name}: ICreateCarDTO): Promise<Car> {
  // [VALIDAÇÃO]
  const car = await this.carsRepository.create({
    // INPUTS
  });
  return car;
}
```
Nesse momento se dermos um `console.log(car)` vamos observar que objeto estará retornando algo como:
```ts
Car {
  brand: 'Brand',
  category_id: 'category',
  daily_rate: 100,
  description: 'Description Car',
  fine_amount: 60,
  license_plate: 'ABCD-1234',
  name: 'Car Available' }
```
onde não vemos id, available e created_at. Para resolver isso vamos criar um constructor com a seguinte estrutura:
```ts
class Car {
  // Demais propriedades...
  constructor() {
    if (!this.id) {
      this.id = uuidv4();
      this.available = true;
      this.created_at = new Date();
    }
  }
}
```

Finalmente vamos criar nosso teste que confere a criação do car.available como true

```ts
it("should not be able to create a car with available true by default", async () => {
  const car = await createCarUseCase.execute({
    name: "Car Available",
    brand: "Brand",
    category_id: "category",
    daily_rate: 100,
    description: "Description Car",
    fine_amount: 60,
    license_plate: "ABCD-1234",
  });

  expect(car.available).toBe(true);
});
```
Antes de finlizar vamos modificar um pouco o primeiro teste que criamos aqui para garantir que ele está sendo criado corretamente, pra isso vamos verificar se ele é criado com a propriedade "id".
```ts
it("should be able to create a new car", async () => {
  const car = await createCarUseCase.execute({
    name: "Name Car",
    brand: "Brand",
    category_id: "category",
    daily_rate: 100,
    description: "Description Car",
    fine_amount: 60,
    license_plate: "ABC-1234",
  });

  expect(car).toHaveProperty("id");
});
```

## Aula C
> Estruturando a Entidade de Carros

Nessa aula vamos integrar o typeorm nessa parte da aplicação começando com a nossa entidade Car.

```ts
// Fazendo referencia a tabela cars criada no migration:run
@Entity("cars")
class Car {
  @PrimaryColumn()
  id: string;

  @Column()
  name: string;

  @Column()
  description: string;

  @Column()
  daily_rate: number;

  @Column()
  available: boolean;

  @Column()
  license_plate: string;

  @Column()
  fine_amount: number;

  @Column()
  brand: string;

  // chave estrangeira
  // muitos carros para uma categoria - ManyToOne
  @ManyToOne(() => Category)
  // Referenciando Coluna
  @JoinColumn({ name: "category_id" })
  category: Category;

  // chave estrangeira
  @Column()
  category_id: string;

  // cria 
  @CreateDateColumn()
  created_at: Date;
  // cria data
  constructor() {
    if (!this.id) {
      this.id = uuidv4();
      // seta Available como true
      this.available = true;
    }
  }
}
export { Car };
```

Agora podemos criar a classe'que será responssável por fazer a comunicação com o banco de dados o `CarsRepository`. Então na pasta repositories do módulo `cars` vamos criar o arquivo `CarsRepository.ts` com a seguinte estrutura:

```ts
// implementação do ICarsRepository
class CarsRepository implements ICarsRepository {
  // Cria a propriedade repository informando que el é do tipo repository do typeorm
  private repository: Repository<Car>;

  // Pega o repositório Car e no this.repository
  constructor() {
    this.repository = getRepository(Car);
  }

  // Restante do código é parecido ao repositório in-memory

  async create({
    brand,
    category_id,
    daily_rate,
    description,
    fine_amount,
    license_plate,
    name,
  }: ICreateCarDTO): Promise<Car> {
    const car = this.repository.create({
      brand,
      category_id,
      daily_rate,
      description,
      fine_amount,
      license_plate,
      name,
    });

    this.repository.save(car);

    return car;
  }
  async findByLicensePlate(license_plate: string): Promise<Car> {
    const car = await this.repository.findOne({ license_plate });
    return car;
  }
}
export { CarsRepository };
```

Agora vamos descomentar a parte do useCase que estava comentado o `@inject("CarsRepository")` e o `injectable()`

E finalmente para automatizar nosso instanciamento vamos usar os containers do tsyringe. No diretório `shared/container/` vamos adionar ao arquivo index a seguinte estrutura:

```ts
container.registerSingleton<ICarsRepository>("CarsRepository", CarsRepository);
```
Agora vamos para o controller.
```ts
class CreateCarController {
  // tipando o request e o response do express
  async handle(request: Request, response: Response): Promise<Response> {
    const {
      brand,
      category_id,
      daily_rate,
      description,
      fine_amount,
      license_plate,
      name,
    } = request.body;
    // chamando o createCaUseCase
    const createCarUseCase = container.resolve(CreateCarUseCase);
    // executando  
    const car = await createCarUseCase.execute({
      brand,
      category_id,
      daily_rate,
      description,
      fine_amount,
      license_plate,
      name,
    });
    // retornado o objeto de car
    return response.status(201).json(car);
  }
}
export { CreateCarController };
```
Finalmente chegamos nas rotas. Então em `shared/infra/http/routes/` vamos criar o arquivo `cars.routes.ts` com a seguinte estrutura:

```ts
import { Router } from "express";
import { CreateCarController } from "@modules/cars/useCases/createCar/CreateCarController";

const carsRoutes = Router();
// Instanciando o createController
const createCarController = new CreateCarController();
carsRoutes.post("/", createCarController.handle);

export { carsRoutes };
```

E chamar essa rota no index desse diretório
```ts
import { carsRoutes } from "./cars.routes";
// ... RESTO DO CÓDIGO
router.use("/cars", carsRoutes);
```
Finlizamos testanto o código no insomnia

## Aula CI
> Criando seed de usuário

Na nossa estrutura de criação de usuário atualmente não conseguimos sinalizar que ele é um admin ou não para evitar manipulações por parte de outros usuários maliciosos. Para resoler esse problema vamos utilizar o conceito de seed pra a criação do usuário admin, rodando uma query direto na aplicação como veremos a seguir.

No path `shared/infra/typeorm/` vamos criar o diretório `seed/` e nele o arquivo `admin.ts` com a finalidade de captura a conexão criada `typeorm/index.ts`. Da maneira que estamos criando atualmente a nossa conexão fica mais difícil fazer esse procedimento, para isso então, vamos reestruturar da seguinte maneira.

**`typeorm/index.ts`:**
```ts
// Definimos "database_ignite" como host padrão pois esse é o nome do meu banco de dados o qual foi definido na criação com o docker-compose, mas existem complitos do docker com o typeorm, por isso será passado outro nome no createConnection do seed/admin.ts
export default async (host = "database_ignite"): Promise<Connection> => {
  const defaultOptions = await getConnectionOptions();
  return createConnection(Object.assign(defaultOptions, { host }));
};
```
Com nossa connection sendo exportada vamos poder capturar no `seed/admin.ts`.
**`seed/admin.ts`:**
```ts
async function create() {
  // host = localhost devido a conflitos entre o typeorm e o docker
  const connection = await createConnection("localhost");

  const id = uuidv4();
  const password = await hash("admin", 8);
  // inserção do user admin na tabela USERS
  await connection.query(
    `INSERT INTO USERS(id, name, email, password, "isAdmin", created_at, driver_license )
    values('${id}', 'admin', 'admin@rentalx.com.br', '${password}', true, 'now()', '123456')`
  );
}

create().then(() => console.log("User Admin created!"));
```

Já que mudamos a forma que esportamos a nossa conexão com o banco de dados teremos que mudar também a forama como importamos no nosso server.
**`server.ts`:**
```ts
// ...
import createConnection from "@shared/infra/typeorm";
// ...
createConnection();
// ...
```

Para finalizar precisamos executar o nosso `seed/admin.ts`. Dessa maneira, vamos criar um secript no **`package.json`**:
```json
{
  // ...
    "scripts": {
    //... 
    "seed:admin": "ts-node-dev src/shared/infra/typeorm/seed/admin.ts"
  },
  // ...
}
```
E assim pode star nossa aplicação e executar o script com `yarn seed:admin`, criando assim nosso usuário admin.

## Aula CII
> Criando middleware de administrador

Na criação desse middleware vamos pegar o usuário que é enviado no request a partir do middleware ensureuthenticated, e verificar se o `isAdmin` é `true` e retornar o `net()`, simples assim. Então na pasta em `shared/infra/http/middlewares/` vamos criar  o arquivo `ensureAdmin.ts` com a seguinte estrutura:

```ts
export async function ensureAdmin(
  // estrutura padrão de middleware
  request: Request,
  response: Response,
  next: NextFunction
): Promise<void> {
  // captura id do user passado pelo ensureAuthenticated
  const { id } = request.user;
  // instanciando o usersRepository
  const usersRepository = new UsersRepository();
  // buscando o user com o mesmo id
  const user = await usersRepository.findById(id);
  // caso o usuário não seja admin ele vai retornar o erro: "User isn't Admin!"
  if (!user.isAdmin) {
    throw new AppError("User isn't Admin!");
  }
  // caso seja admin, segue na rota
  return next();
}
```
Após criado o middleware, podemos utilizá-lo em nossas rotas de `POST` em cars, categories e specificaions, lembrando que sempre será após o `ensureAuthenticated`.

**`cars.routes.ts`**
```ts
carsRoutes.post(
  "/",
  ensureAuthenticated,
  ensureAdmin,
  createCarController.handle
);
```
**`categories.routes.ts`**
```ts
categoriesRoutes.post(
  "/",
  ensureAuthenticated,
  ensureAdmin,
  createCategoryController.handle
);

categoriesRoutes.get("/", listCategoriesController.handle);

categoriesRoutes.post(
  "/import",
  upload.single("file"),
  ensureAuthenticated,
  ensureAdmin,
  importCategoryController.handle
);
```
**`specifications.routes.ts`**
```ts
specificationsRoutes.post(
  "/",
  ensureAuthenticated,
  ensureAdmin,
  createSpecificationController.hadle
);
```

## Aula CIII
> Listando carros disponíveis

Para fazer a listagem de carros, antes de tudo precisamos criar um useCase no módulo de `cars` que vamos chamar de `listAvailableCars/` e juntamente o `listAvailableCarsUseCase.ts` e `listAvailableCarsUseCase.spec.ts`. Para termos como listar todos os carros e os filtros opicionais de nome, marca ou categoria, é necessário um método no repositório, que que essa parte da aplicação é de função dele, então antes de passarmos para o useCase e o teste, vamos ajustar nosso repositório.
**`ICarsRepository.ts`:**
```ts
interface ICarsRepository {
  create(data: ICreateCarDTO): Promise<Car>;
  findByLicensePlate(license_plate: string): Promise<Car>;
  // Vamos apenas declarar esse novo método e irformar que os "inputs" são opicionais
  // Lembrando que o retorno será de uma lista de carros ➡ Car[]
  findAvailable(
    brand?: string,
    name?: string,
    category_id?: string
  ): Promise<Car[]>;
}
export { ICarsRepository };
```
Vamos relembrar um pouco do que queremos.
1 - Que retorne todos os carros disponíveis (available = true)
2 - Se informar a marca, retorne todos os carros disponíveis daquela marca
3 - Se informar a nome, retorne todos os carros disponíveis daquela nome
4 - Se informar a categoria, retorne todos os carros disponíveis daquela categoria
Ou seja, por padrão retorna tudo, mas temos filtros opicionais.
**`CarsRepositoryInMemory.ts`:**
```ts
class CarsRepositoryInMemory{
  // ...OUTROS MÉTODOS
  async findAvailable(
    brand?: string,
    name?: string,
    category_id?: string
  ): Promise<Car[]> {
    const cars = this.cars.filter((car) => {
      
      if (
        // se estiver disponíve e
        car.available === true ||
        // a marca existir e a marca do carro for igual a marca passada, retorna esse aí
                                      // OU
        ((brand && car.brand === brand) ||
        // a categoria existir e a categoria do carro for igual a categoria passada, retorna esse aí
                                                      // OU
        (category_id && car.category_id === category_id) ||
        // o nome existir e o nome do carro for igual ao nome passado, retorna esse aí
        (name && car.name === name))
      ) {
        // retorne car para o filtro
        return car;
      }
      return null;
    });
    // retorne a lista filtrada
    return cars;
  }
}
```
Com o repositó de teste criados podemos prosseguir e criar nosso useCase.
**`listAvailableCarsUseCase.ts`:**
```ts
// aqui informamos que dados serão recebidos no método execute 
interface IRequest {
  category_id?: string;
  brand?: string;
  name?: string;
}

class listAvailableCarsUseCase {
  // informando que tipo de objeto será passado no useCase quando for instanciado
  constructor(private carsRepository: ICarsRepository) {}

  async execute({ brand, category_id, name }: IRequest): Promise<Car[]> {
    // utilizando o método que acabamos de criar
    const cars = await this.carsRepository.findAvailable(
      brand,
      category_id,
      name
    );
    // retornando os carros
    return cars;
  }
}
export { listAvailableCarsUseCase };
```

**`listAvailableCarsUseCase.spec.ts`:**
```ts
// criando as variáveis de useCase e repository
let listAvailableCarsUseCase: listAvailableCarsUseCase;
let carsRepositoryInMemory: CarsRepositoryInMemory;

describe("List Cars", () => {
  // instanciando antes de cada teste
  beforeEach(() => {
    carsRepositoryInMemory = new CarsRepositoryInMemory();
    listAvailableCarsUseCase = new listAvailableCarsUseCase(carsRepositoryInMemory);
  });
  // Teste para listar todos os carros disponíveis
  it("should be able to list all available cars", async () => {
    const car = await carsRepositoryInMemory.create({
      name: "Car1",
      brand: "Car_brand",
      category_id: "category_id",
      daily_rate: 140,
      description: "Carro massa",
      fine_amount: 100,
      license_plate: "DFG-4454",
    });
    const cars = await listAvailableCarsUseCase.execute({});
    expect(cars).toEqual([car]);
  });

  // Teste para listar todos os carros disponíveis por marca
  it("should be able to list all available cars by marca", async () => {
    const car = await carsRepositoryInMemory.create({
      name: "Car2",
      brand: "Car_brand_test",
      category_id: "category_id",
      daily_rate: 140,
      description: "Carro massa",
      fine_amount: 100,
      license_plate: "DFG-4454",
    });
    const cars = await listAvailableCarsUseCase.execute({
      brand: "Car_brand_test",
    });
    expect(cars).toEqual([car]);
  });
});
```

## Aula CIV
> Continuação da listagem de carros disponíveis

Vamos dar continuidade aos nossos testes antes da implementação em nosso `CarsRepository`. Para isso vamos adicionar os outros doi testes com o name e com o category_id.
```ts
it("should be able to list all available cars by name", async () => {
  const car = await carsRepositoryInMemory.create({
    name: "Car3",
    brand: "Car_brand_test",
    category_id: "category_id",
    daily_rate: 140,
    description: "Carro massa",
    fine_amount: 100,
    license_plate: "DFG-2454",
  });
  const cars = await listAvailableCarsUseCase.execute({
    name: "Car3",
  });
  expect(cars).toEqual([car]);
});

it("should be able to list all available cars by category", async () => {
  const car = await carsRepositoryInMemory.create({
    name: "Car3",
    brand: "Car_brand_test",
    category_id: "category_id_test",
    daily_rate: 140,
    description: "Carro massa",
    fine_amount: 100,
    license_plate: "DFG-2454",
  });
  const cars = await listAvailableCarsUseCase.execute({
    category_id: "category_id_test",
  });
  expect(cars).toEqual([car]);
});
```

Teste concluído vamos ao nosso arquivo `CarsRepository.ts` e implemntar o método `findAvailable()`.
```ts
class CarsRepository{
// ...RESTANTE DO CÓDIGO
  async findAvailable(
    brand?: string,
    category_id?: string,
    name?: string
  ): Promise<Car[]> {
    // criando uma query
    const carsQuery = await this.repository
      .createQueryBuilder("c")
      .where("available = :available", { available: true });
    // se recebermos marca será adicionado esse trecho a query
    if (brand) {
      carsQuery.andWhere("brand = :brand", { brand });
    }
    // se recebermos name será adicionado esse trecho a query
    if (name) {
      carsQuery.andWhere("name = :name", { name });
    }
    // se recebermos category_id será adicionado esse trecho a query
    if (category_id) {
      carsQuery.andWhere("category_id =  :category_id", { category_id });
    }
    // execute a query
    const cars = await carsQuery.getMany();
    return cars;
  }
}
```
Método do repositório criado vamos fazer uma pequena modificação no no useCase para que ele possa se comunicar com o controller e com nosso repositório, que é adicionar o `@inject()` e o `@injectable()` tsrynge.
```ts
@injectable()
class ListAvailableCarsUseCase {
  constructor(
    @inject("CarsRepository")
    private carsRepository: ICarsRepository
  ) {}
  async execute({ brand, category_id, name }: IRequest): Promise<Car[]> {
    const cars = await this.carsRepository.findAvailable(
      brand,
      category_id,
      name
    );
    return cars;
  }
}
```
Agora vamos criar o `ListAvailableCarsController.ts` com a seguinte estrutura:
```ts
class ListAvailableCarsController {
  async handle(request: Request, response: Response): Promise<Response> {
    const { brand, name, category_id } = request.query;
    // instanciando o useCase com tsyringe
    const listAvailableCarsUseCase = container.resolve(
      ListAvailableCarsUseCase
    );
    const cars = await listAvailableCarsUseCase.execute({
      // para garantir que vamos receber strings pela request.query, tipamos aqui
      brand: brand as string,
      name: name as string,
      category_id: category_id as string,
    });
    return response.json(cars);
  }
}
export { ListAvailableCarsController };
```

Para finalizar vamos criar a rota.
```ts
// RESTANTE DO CÓDIGO
const listAvailableCarsController = new ListAvailableCarsController();
carsRoutes.get("/available", listAvailableCarsController.handle);
// RESTANTE DO CÓDIGO
```

## Aula CV
> Criando Migrations Especificação de carros(Many to Many)

Continuando nossa aplicação, vamos criar aqui uma tabela de relacionamentos, fazendo a ligação do id do carro ao id da especificação. Para isso, começaremos execuando `yarn typeorm migration:create -n CreateSpecificationsCars` e seguir a seguinte estrutura:
```ts
export class CreateSpecificationsCars1625478365910
  implements MigrationInterface
{
  public async up(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.createTable(
      new Table({
        // criando tabela
        name: "specifications_cars",
        columns: [
          {
            name: "car_id",
            type: "uuid",
          },
          {
            name: "specification_id",
            type: "uuid",
          },
          {
            name: "created_at",
            type: "timestamp",
            default: "now()",
          },
        ],
      })
    );
    await queryRunner.createForeignKey(
      // referenciando tabela local
      "specifications_cars",
      new TableForeignKey({
        // nomeando FK
        name: "FKSpecificationCar",
        // referenciando tabela estrangeira
        referencedTableName: "specifications",
        // referenciando coluna estranngeira
        referencedColumnNames: ["id"],
        // referenciando coluna local
        columnNames: ["specification_id"],
        onDelete: "SET NULL",
        onUpdate: "SET NULL",
      })
    );
    await queryRunner.createForeignKey(
      // referenciando tabela local
      "specifications_cars",
      // nomeando FK
      new TableForeignKey({
        name: "FKCarSpecification",
        // referenciando tabela estrangeira
        referencedTableName: "cars",
        // referenciando coluna estranngeira
        referencedColumnNames: ["id"],
        // referenciando coluna local
        columnNames: ["car_id"],
        onDelete: "SET NULL",
        onUpdate: "SET NULL",
      })
    );
  }
  public async down(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.dropForeignKey(
      "specifications_cars",
      "FKCarSpecification"
    );
    await queryRunner.dropForeignKey(
      "specifications_cars",
      "FKSpecificationCar"
    );

    await queryRunner.dropTable("specifications_cars");
  }
}
```
E por final executar nossa migration: `yarn typeorm migration:run`.

## Aula CVI
> Caso de uso do cadastro de especificação para carro

Vamos alterar nossa Entity de `Car` para que ele receba as propriedades das especificações que iremos cadastrar. Para fazer a referencia desses dados, precisamos adicionar o seguinte trecho ao nosso arquivo `Car.ts`:
```ts
class Car{
  // ...
  // Tipo de relação
  // para tabelas de relacionamento sempre será ManyToMany
  @ManyToMany(() => Specification)
  @JoinTable({
    // tabela que estamos referenciando
    name: "specifications_cars",
    // coluna que referencia a coluna dessa classe
    joinColumns: [{ name: "car_id" }],
    // coluna que referencia a coluna da tabela que passamos no ManyToMany
    inverseJoinColumns: [{ name: "specifications_cars" }],
  })
  specifications: Specification[];}
  // ...
```

Agora vamos criar um serviço que cria as especificações. No diretório de useCase do módulo de `cars`, vamos criar o useCase `creatCarSpecification` com os arquivos inicis de useCase e useCase (`CreateCarSpecificationUseCase.ts`) de Test (`CreateCarSpecificationUseCase.spec.ts`) como sempre fazemos.

**`CreateCarSpecificationUseCase.ts`:**
```ts
// A interface da nossa request
interface IRequest {
  car_id: string;
  specifications_id: string[];
}
class CreateCarSpecificationUseCase {
  constructor(
    private carsRepository: ICarsRepository
  ) {}
  async execute({ car_id, specifications_id }: IRequest): Promise<void> {
    // aqui vamos buscar se o carro existe 
    // o método findById() ainda não exite, mas já vamos criar antes de passarmos para os testes
    const carExist = await this.carsRepository.findById(car_id);
    // se não existir não tem como atribuir uma specification a ele
    if (!carExist) {
      throw new AppError("Car doesn't exist!");
    }
  }
}
export { CreateCarSpecificationUseCase };
```
Criando o método adicionando método a interface
**`ICarsrepository.ts`:**
```ts
interface ICarsRepository {
  // RESTANTE DA INTERFACE
  findById(car_id: string): Promise<Car>;
}
```

Implementando método em repositório para os testes
**`CarRepositoryInMemory.ts`:**
```ts
class CarRepositoryInMemory{
  // RESTANTE DA CLASSE
  async findById(car_id: string): Promise<Car> {
    return this.cars.find((car) => car.id === car_id);
  }
}
```
Com método criado, podemos começar a criar nossos testes
**`CreateCarSpecificationUseCase.spec.ts`:**
```ts
// iniciando nossas variáveis
let createCarSpecificationUseCase: CreateCarSpecificationUseCase;
let carsRepositoryInMemory: CarsRepositoryInMemory;
describe("Create Car Specification", () => {
  beforeEach(() => {
    // instanciando useCase e repository antes de cada teste
    carsRepositoryInMemory = new CarsRepositoryInMemory();
    createCarSpecificationUseCase = new CreateCarSpecificationUseCase(
      carsRepositoryInMemory
    );
  });
  // não cadastar specification caso carro não exista
  it("should not be able to add a new specification to a now-existent car", async () => {
    // espera-se que ao passar os parâmetros de car_id e specifications_id ao usecase
    expect(async () => {
      const car_id = "123";
      const specifications_id = ["54321"];
      await createCarSpecificationUseCase.execute({
        car_id,
        specifications_id,
      });
      // seja rejitado com a instância do tipo AppError (a mesma que passamos no if do useCase)
    }).rejects.toBeInstanceOf(AppError);
  });
  // Seja possível adiciona uma nova specificação a um carro
  // teste incompleto
  it("should be able to add a new specification to the car", async () => {
    const car = await carsRepositoryInMemory.create({
      name: "Name Car",
      brand: "Brand",
      category_id: "category",
      daily_rate: 100,
      description: "Description Car",
      fine_amount: 60,
      license_plate: "ABC-1234",
    });
    const specifications_id = ["54321"];
    await createCarSpecificationUseCase.execute({
      car_id: car.id,
      specifications_id,
    });
  });
});
```

## Aula CVII
> Continuação dos CreateCarSpecificationUseCase

O que vamos fazer nessa aula é salvar as specifications no repositório. Nisso, voltando para o useCase vamos ter:
**`CreateCarSpecificationUseCase.ts`:**
```ts
// RESTANTE D CÓDIGO
class CreateCarSpecificationUseCase {
  // Parte do código visto anteriormente ⤵
  // constructor(
  //   private carsRepository: ICarsRepository,
    private specificationsRepository: ISpecificationsRepository // DECLARAÇÃO PARA PODER SER FEITO O INSTÂNCIMANTO DO USECASE CORRETAMENTE 
  // ) {}
  // async execute({ car_id, specifications_id }: IRequest): Promise<void> {
  //   const carExist = await this.carsRepository.findById(car_id);
  //   if (!carExist) {
  //     throw new AppError("Car doesn't exist!");
  //   }

  // Retorna um array de Specification
  // Vamos crir em eguida o Método finByIds
    const specifications = await this.specificationsRepository.findByIds(
      specifications_id
    );
    // Vamos gravar o array de specification que findByIds trouxe no carExist.specifications
    carExist.specifications = specifications;
    // Passando para o repository
    // Teremos que alterar em breveo carsRepository pois na criação do car não existe parâmetro de specification
    await this.carsRepository.create(carExist);
  }
}
export { CreateCarSpecificationUseCase };
```

Para adicionar o método `findByIds()` ao repositório de specifications, vamos na interface dele declará-lo.

**`ISpecificationsRepository.ts`:**
```ts
interface ISpecificationsRepository {
  // RESTO DO CÓDIGO 
  findByIds(ids: string[]): Promise<Specification[]>;
}
```
Implementando no repositório de teste:
Na pasta in-memory do módulo `cars` vamos criar o arquivo `SpecificationsRepositoryInMemory.ts`
**`SpecificationsRepositoryInMemory.ts`:**
```ts
class SpecificationsRepositoryInMemory implements ISpecificationsRepository {
  specifications: Specification[] = [];

  async create({ name, description }: ICreateSpecificationDTO): Promise<void> {
    const specification = new Specification();
    Object.assign(specification, {
      description,
      name,
    });
    this.specifications.push(specification);
  }
  async findByName(name: string): Promise<Specification> {
    return this.specifications.find(
      (specification) => specification.name === name
    );
  }
  async findByIds(ids: string[]): Promise<Specification[]> {
    // Filtre do meu repositório de specifications
    const allSpesifications = this.specifications.filter((specification) =>
    // as specifications qe estão no array 'ids'
      ids.includes(specification.id)
    );
    return allSpesifications;
  }
}
export { SpecificationsRepositoryInMemory };
```
Repositório ✔, useCase ✔, vamos agora adicionar o parâmetro de specification a criação de um `car`, antes de ir ao repositório vamos declarar na interface `ICreateCarDTO`.
**`ICreateCarDTO.ts`:**
```ts 
interface ICreateCarDTO {
  // RESTANTE DOS PARÂMETROS
  // vamos deixar specifications como opicional pois na criação do carro não será ṕossível (por enquanto) adicionar as specifications
  specifications?: Specification[];
}
export { ICreateCarDTO };
```
Declarado na iterface podemos repassar aos repositórios tanto de teste como do typeorm.

**`CarsRepositoryInMemory.ts`:**
```ts
class {
  // RESTANTE DO CÓDIGO
  async create({
    brand,
    category_id,
    daily_rate,
    description,
    fine_amount,
    license_plate,
    name,
    specifications,
  }: ICreateCarDTO): Promise<Car> {
    const car = new Car();

    Object.assign(car, {
      brand,
      category_id,
      daily_rate,
      description,
      fine_amount,
      license_plate,
      name,
      specifications,
    });

    this.cars.push(car);
    return car;
  }
}
```

**`CarsRepository.ts`:**
```ts
class{
  // RESTANTE DO CÓDIGO
  async create({
    brand,
    category_id,
    daily_rate,
    description,
    fine_amount,
    license_plate,
    name,
    specifications,
  }: ICreateCarDTO): Promise<Car> {
    const car = this.repository.create({
      brand,
      category_id,
      daily_rate,
      description,
      fine_amount,
      license_plate,
      name,
      specifications,
    });

    this.repository.save(car);

    return car;
  }
}
```
E finalmente vamos aos testes, que no momento encontram-se dessa forma:
```ts
let createCarSpecificationUseCase: CreateCarSpecificationUseCase;
let carsRepositoryInMemory: CarsRepositoryInMemory;
let specificationsRepositoryInMemory: SpecificationsRepositoryInMemory;
describe("Create Car Specification", () => {
  beforeEach(() => {
    carsRepositoryInMemory = new CarsRepositoryInMemory();
    specificationsRepositoryInMemory = new SpecificationsRepositoryInMemory();
    createCarSpecificationUseCase = new CreateCarSpecificationUseCase(
      carsRepositoryInMemory,
      specificationsRepositoryInMemory
    );
  });

  it("should not be able to add a new specification to a now-existent car", async () => {
    expect(async () => {
      const car_id = "123";
      const specifications_id = ["54321"];

      await createCarSpecificationUseCase.execute({
        car_id,
        specifications_id,
      });
    }).rejects.toBeInstanceOf(AppError);
  });

  it("should be able to add a new specification to the car", async () => {
    const car = await carsRepositoryInMemory.create({
      name: "Name Car",
      brand: "Brand",
      category_id: "category",
      daily_rate: 100,
      description: "Description Car",
      fine_amount: 60,
      license_plate: "ABC-1234",
    });

    const specifications_id = ["54321"];
    
    await createCarSpecificationUseCase.execute({
      car_id: car.id,
      specifications_id,
    });
  });
});
```

## Aula CVIII
> Finalizando CreateCarSpecificationUseCase

No teste, `should be able to add a new specification to the car`, nós vamos agora adicionar uma specification para de fato usar o teste ao qu ele foi proposto, para isso nós vamos umsa um estratégia que pede que no momento que a specification seja criada ela retorne essa criação. Devido a isso ao finalizarmos no arquivo de teste, vamos alterar o `SpecificationsRepository.ts` e por consequência vamos ter que alterar também o `ISpecificationsRepository.ts` e `SpecificationsRepositoryInMemory.ts`.

**`ISpecificationsRepository.ts`:**
```ts
interface ICreateSpecificationDTO {
  name: string;
  description: string;
}
interface ISpecificationsRepository {
  create({
    name,
    description,
    // Retorna a specification
  }: ICreateSpecificationDTO): Promise<Specification>;
  findByName(name: string): Promise<Specification>;
  findByIds(ids: string[]): Promise<Specification[]>;
}
export { ISpecificationsRepository, ICreateSpecificationDTO };
```

**`SpecificationsRepository.ts`:**
```ts
class SpecificationsRepository {
  // Restante do código
  async create({
    name,
    description,
    // Tipo do retorno alterado
  }: ICreateSpecificationDTO): Promise<Specification> {
    const specification = this.repository.create({
      name,
      description,
    });
    await this.repository.save(specification);
// retornando especificação
    return specification;
  }
  // Restante do código
}
```
**`SpecificationsRepositoryInMemory.ts`:**
```ts
class SpecificationsRepositoryInMemory {
  // Restante do código
  async create({
    name,
    description,
  }: ICreateSpecificationDTO): Promise<Specification> {
    const specification = new Specification();
    Object.assign(specification, {
      description,
      name,
    });
    this.specifications.push(specification);
    return specification;
  }
  // Restante do código
}
```
Antes de mais nad vamos terminar de implementar o findByIds no `SpecificationsRepository`.

**`SpecificationsRepository.ts`:**
```ts
class SpecificationsRepository {
  // Restante do código
  async findByIds(ids: string[]): Promise<Specification[]> {
    // usando o medo do typeorm
    const specifications = await this.repository.findByIds(ids);
    return specifications;
  }
  // Restante do código
}
```
No fluxo que temos agora no update que estamos fazendo teoricamente será criado um novo `Car` já que o id não é passado, entõ vamos agora corrigir isso.

**`ICreateCarDTO.ts`:**
```ts
interface ICreateCarDTO {
  // RESTANTE DO CÓDIGO
  id?: string;
}
```
**`CarsRepository.ts`:**
```ts
class CarsRepository implements ICarsRepository {
  // RESTANTE DO CÓDIGO
  async create({
    brand,
    category_id,
    daily_rate,
    description,
    fine_amount,
    license_plate,
    name,
    specifications,
    id,
  }: ICreateCarDTO): Promise<Car> {
    const car = this.repository.create({
      brand,
      category_id,
      daily_rate,
      description,
      fine_amount,
      license_plate,
      name,
      specifications,
      id,
    });

    this.repository.save(car);

    return car;
  }
  // RESTANTE DO CÓDIGO
}
```
**`CarsRepositoryInMemory.ts`:**
```ts
class CarsRepositoryInMemory implements ICarsRepository {
  // RESTANTE DO CÓDIGO
  async create({
    brand,
    category_id,
    daily_rate,
    description,
    fine_amount,
    license_plate,
    name,
    specifications,
    id,
  }: ICreateCarDTO): Promise<Car> {
    const car = new Car();

    Object.assign(car, {
      brand,
      category_id,
      daily_rate,
      description,
      fine_amount,
      license_plate,
      name,
      specifications,
      id,
    });

    this.cars.push(car);
    return car;
  }
  // RESTANTE DO CÓDIGO
}
```
Agora Podemos nos encaminhar pra finalizar essa parte, vamos atualiza agora nosso useCase.

**`CreateCarSpecificationUseCase.ts`:**
```ts
interface IRequest {
  car_id: string;
  specifications_id: string[];
}
@injectable()
class CreateCarSpecificationUseCase {
  constructor(
    @inject("CarsRepository")
    private carsRepository: ICarsRepository,
    @inject("SpecificationsRepository")
    private specificationsRepository: ISpecificationsRepository
  ) {}
  async execute({ car_id, specifications_id }: IRequest): Promise<Car> {
    const carExist = await this.carsRepository.findById(car_id);
    if (!carExist) {
      throw new AppError("Car doesn't exist!");
    }
    const specifications = await this.specificationsRepository.findByIds(
      specifications_id
    );
    carExist.specifications = specifications;
    // Recriando car
    await this.carsRepository.create(carExist);
    // Retornando o car atualizado
    return carExist;
  }
}
export { CreateCarSpecificationUseCase };
```


```ts
it("should be able to add a new specification to the car", async () => {
  const car = await carsRepositoryInMemory.create({
    name: "Name Car",
      brand: "Brand",
      category_id: "category",
      daily_rate: 100,
      description: "Description Car",
      fine_amount: 60,
      license_plate: "ABC-1234",
    });

    const specification = await specificationsRepositoryInMemory.create({
      description: "teste description",
      name: "teste name",
    });

    const specifications_id = [specification.id];

    const specificationsCars = await createCarSpecificationUseCase.execute({
      car_id: car.id,
      specifications_id,
    });
    // Espera-se que que o novo car tenha a propriedade "specifications" 
    expect(specificationsCars).toHaveProperty("specifications");
    // Espera-se que o tamanho da nova specifications seja 1
    expect(specificationsCars.specifications.length).toBe(1);
  });
```
Terminado essa parte de teste vamos agora criar o o controller e em seguida adicionar as rotas da api.

**`CreateCarSpecificationController`:**
```ts
class CreateCarSpecificationController {
  async handle(request: Request, response: Response): Promise<Response> {
    // Buscando variáveis na requisição
    const { id } = request.params;
    const { specifications_id } = request.body;
    // instnciando useCase
    const createCarSpecificationUseCase = container.resolve(
      CreateCarSpecificationUseCase
    );
    // Executando useCase
    const car = await createCarSpecificationUseCase.execute({
      car_id: id,
      specifications_id,
    });
    // Retornado car atualizado 
    return response.json(car);
  }
}
export { CreateCarSpecificationController };
```

E para encerrar nossa rota:

```ts
// RESTO DO CÓDIGO
const createCarSpecificationController = new CreateCarSpecificationController();
// RESTO DO CÓDIGO
carsRoutes.post(
  "/specifications/:id",
  ensureAuthenticated,
  ensureAdmin,
  createCarSpecificationController.handle
);
// RESTO DO CÓDIGO
```

## Aula CIX
> Criando migrations de imagens de carro

Vamos criar uma tabela para guardar as imagens dos carros, para isso vamos criar mais uma tabela no nosso banco de dados com as migrations do typeorm.
```bash
yarn typeorm migrations:create -n CreateCarImages
```
Feito isso, vamos criar nossa tabela.

**`CreateCarImages.ts`:**
```ts
export class CreateCarImages1625565503056 implements MigrationInterface {
  public async up(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.createTable(
      new Table({
        name: "cars_image",
        columns: [
          { name: "id", type: "uuid", isPrimary: true },
          { name: "car_id", type: "uuid" },
          { name: "image_name", type: "varchar" },
          { name: "created_at", type: "timestamp", default: "now()" },
        ],
        foreignKeys: [
          {
            name: "FKCarImage",
            referencedTableName: "cars",
            referencedColumnNames: ["id"],
            columnNames: ["car_id"],
            onDelete: "SET NULL",
            onUpdate: "SET NULL",
          },
        ],
      })
    );
  }
  public async down(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.dropTable("cars_image");
  }
}
```
Em seguida executamos o comando `yarn typeorm migration:run` para executarmos nossa migration e criarmos a tabela, cars_image, em nosso banco de dados.

Apenas para nos basear e facilitar, a seguir temos um checklist dos passos que precisam ser seguidos até chegar a criação da nossa rota.

- [x] Migration
- [ ] Entity
- [ ] IRepository
- [ ] Repository
- [ ] Container
- [ ] UseCase
- [ ] Test
- [ ] Controller
- [ ] Router

Dessa maneira, vamos seguir para criação da nossa entidade.

**`CarImage.ts`:**
```ts
// fazendo referencia da entidade para tabela
@Entity("cars_image")
class CarImage {
  @PrimaryColumn()
  id: string;

  @Column()
  car_id: string;

  @Column()
  image_name: string;

  @CreateDateColumn()
  created_at: Date;
  constructor() {
    if (!this.id) {
      this.id = uuidv4();
    }
  }
}
export { CarImage };
```

No diretório de `cars/repositories/` vamos criar:
**`ICarsImagesRepository.ts`:**

```ts
interface ICarsImagesRepository {
  create(car_id: string, image_name: string): Promise<CarImage>;
}
export { ICarsImagesRepository };
```

Implmentação do ICarsImagesRepository em `cars/infra/typeorm/repositories/`.

```ts
import { Repository } from "typeorm";

import { ICarsImagesRepository } from "@modules/cars/repositories/ICarsImagesRepository";

import { CarImage } from "../entities/CarImage";

class CarsImagesRepository implements ICarsImagesRepository {
  private repository: Repository<CarImage>;
  async create(car_id: string, image_name: string): Promise<CarImage> {
    // lembrando que o create não tem await pois ele so está montando nosso objeto
    const carImage = this.repository.create({ car_id, image_name });
    // e aqui tem await pois trata diretamente com nosso banco de dados na hor do salvamento.
    await this.repository.save(carImage);
    // retorndo nosso objeto
    return carImage;
  }
}
export { CarsImagesRepository };
```

## Aula CX
> Caso de uso do cadastro de imagens do carro

Para finalizar o cadastro das imagens dos carros vamos retornar e ver onde paramos na última aula e ver o que está faltando no todo-list abaixo.

- [x] Migration
- [x] Entity
- [x] IRepository
- [x] Repository
- [ ] Container
- [ ] UseCase
- [ ] Controller
- [ ] Router

Então agora vamos configurar a comunicação do nosso repositório com o tsyringe no arquivo index.ts, localizado na pasta `shared/container/`.

**`index.ts`:**
```ts
container.registerSingleton<ICarsImagesRepository>(
  "CarsImagesRepository",
  CarsImagesRepository
);
```
Container ✅

Agora no useCase:

```ts
// interface informando a tipagem
interface IRequest {
  car_id: string;
  images_name: string[];
}
@injectable()
class UploadCarImagesUseCase {
  constructor(
    // fazendo referência para o container do tsyringe
    @inject("CarsImagesRepository")
    private carsImagesRepository: ICarsImagesRepository
  ) {}
  async execute({ car_id, images_name }: IRequest): Promise<void> {
    // já que tems um array, temos que percorrer ele e salvar cada imagem
    images_name.map(async (image) => {
      await this.carsImagesRepository.create(car_id, image);
    });
  }
}
export { UploadCarImagesUseCase };
```
UseCase ✅

**`UploadCarImagesControllers.ts`:**

```ts
// interface como estratégia para poder apontr que será um array de images vindo no request.
interface IFiles {
  filename: string;
}
class UploadCarImagesController {
  async heandle(request: Request, response: Response): Promise<Response> {
    const { id } = request.params;
    const images = request.files as IFiles[];
    // instanciando useCase
    const uploadCarImagesUseCase = container.resolve(UploadCarImagesUseCase);
    // pegando apenas o filename do arquivo e passando para um array
    const images_name = images.map((file) => file.filename);
    // execuado o useCase
    await uploadCarImagesUseCase.execute({ car_id: id, images_name });
    return response.status(201).send();
  }
}
export { UploadCarImagesController };
```
Controller ✅

**`cars.routes.ts`:**
```ts
carsRoutes.post(
  "/images/:id",
  ensureAuthenticated,
  ensureAdmin,
  upload.array("images"),
  uploadCarImagesController.heandle
);
```
Router ✅

## Aula CXI
> Criando migrations do aluguel

Como já fizemos diversas vese o migrations, vamos passar mais rápido por essa questão e deixar apenas o código como fonte de consulta e resalta de uma falta na criação da tabela de `users` na coluna id faltou atribuir a propriedade `isPrimary: true`.

criaando migration:
```sh
yarn typeorm migration: create -n CreateRentals
```
**`CreateRentals.ts`:**
```ts
import { MigrationInterface, QueryRunner, Table } from "typeorm";

export class CreateRentals1625590443953 implements MigrationInterface {
  public async up(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.createTable(
      new Table({
        name: "rentals",
        columns: [
          { name: "id", type: "uuid", isPrimary: true },
          { name: "car_id", type: "uuid" },
          { name: "user_id", type: "uuid" },
          { name: "start_date", type: "timestamp", default: "now()" },
          { name: "end_date", type: "timestamp" },
          { name: "expected_return_date", type: "timestamp" },
          { name: "total", type: "numeric" },
          { name: "created_at", type: "timestamp", default: "now()" },
          { name: "updated_at", type: "timestamp", default: "now()" },
        ],
        foreignKeys: [
          {
            name: "FKCarRental",
            referencedTableName: "cars",
            referencedColumnNames: ["id"],
            columnNames: ["car_id"],
            onDelete: "SET NULL",
            onUpdate: "SET NULL",
          },
          {
            name: "FKUserRental",
            referencedTableName: "users",
            referencedColumnNames: ["id"],
            columnNames: ["user_id"],
            onDelete: "SET NULL",
            onUpdate: "SET NULL",
          },
        ],
      })
    );
  }

  public async down(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.dropTable("rentals");
  }
}
```

Query para adicionar primary key a coluna id da tabela users:
```sql
ALTER TABLE USERS ADD PRIMARY KEY(id)
```

Executando migration:
```sh
yarn typeorm migration:run
```

## Aula CXII
> Criando os testes do aluguel

Assim como fizemos anteriormente, vamos seguir o todo-list com as tasks para nos basearmos e termos uma melhor noção do que falta ser feito.

- [x] Migration
- [ ] Entity
- [ ] IRepository
- [ ] Repository
- [ ] Container
- [ ] UseCase
- [ ] Controller
- [ ] Router

Primeiramente vamos seprar em um módulo a parte de alugueis, os `Rentals`, pois foi observado que essa seri a maneira mais adequada para tratar na nossa aplicação. Ainda, a nossa entidade, não iremos adicionar os decorators do typeorm por hora, apenas a estrutura básica. Então, na pasta do módulo rentals vamos criar o diretório `infra/typeorm/entities/` e nele a nossa enitity, `Rentals`.

```ts
class Rental {
  id: string;
  car_id: string;
  user_id: string;
  start_date: Date;
  end_date: Date;
  expected_return_date: Date;
  total: number;
  created_at: Date;
  updated_at: Date;
  constructor() {
    if (!this.id) {
      this.id = uuidv4();
    }
  }
}
export { Rental };
```
Entity 🚧

Agora vamos declarar alguns métodos que serão usados no nosso repositório. Na pasta do módulo `rentals` vamos adicionar o diretório `repositoies/` e nele adicionar o arquivo `IRentalsRepository.ts` com a seguinte estrutura:

```ts
interface IRentalsRepository {
  findOpenRentalByCar(car_id: string): Promise<Rental>;
  findOpenRentalByUser(user_id: string): Promise<Rental>;
}
export { IRentalsRepository };
```
IRepository 🚧

Criado essa parte do IRepository vamos implementr no nosso repositório de tests e para isso vamos criar no diretório `repositories/` vamos criar uma pasta chamada `in-memory/` onde iremos criar o arquivo `RentalsRepositoryinMemory.ts`.

**`RentalsRepositoryinMemory.ts`:**
```ts
class RentalsRepositoryInMemory implements IRentalsRepository {
  //Criando array vasio para armazenar os rentals
  rentals: Rental[] = [];
  async findOpenRentalByCar(car_id: string): Promise<Rental> {
    // retorne o rental se o seu car_id foi igual ao car_id que passamos e se o end_date estiver fazio
    return this.rentals.find(
      (rental) => rental.car_id === car_id && rental.end_date === null
    );
  }
  async findOpenRentalByUser(user_id: string): Promise<Rental> {
    // retorne o rental se o seu user_id foi igual ao user_id que passamos e se o end_date estiver fazio
    return this.rentals.find(
      (rental) => rental.user_id === user_id && rental.end_date === null
    );
  }
}
export { RentalsRepositoryInMemory };
```
IRepository 🚧

Criado o repositório parcialmente, já podemos ira para o useCase. no módulo `rentals`, vamos criar a pasta `useCases/` onde vamos criar o arquivo `CreateRentalUseCase.ts` e por hora vamos adicionar a seguinte estrutura:

```ts
interface IRequest {
  user_id: string;
  car_id: string;
  expected_return_date: Date;
}
class CreateRentalUseCase {
  constructor(private rentalsRepository: IRentalsRepository) {}
  async execute({
    car_id,
    expected_return_date,
    user_id,
  }: IRequest): Promise<void> {
    // busca aluguel pelo id do carro
    const carUnavailabel = await this.rentalsRepository.findOpenRentalByCar(
      car_id
    );
    // caso tenha um aluguel desse carro, 
    // apresentamos o erro informando que esse carro não está disponível
    if (carUnavailabel) {
      throw new AppError("Car is unavailable");
    }
    // busca u aluguel pelo id do usuário
    const rentalOpenToUser = await this.rentalsRepository.findOpenRentalByUser(
      user_id
    );
    // se o usuário tiver um alugel em nome dele no qual ainda não foi finalizado,
    // apresentamos o erro informando que o usuário possui um aluguel ativo
    if (rentalOpenToUser) {
      throw new AppError("There's a rental in progress for user");
    }
    // retornando nulo apenas para n termos mais erros 😜
    return null;
  }
}
export { CreateRentalUseCase };
```
CreateRentalUseCase 🚧

Agora vamos fazer apens um teste simples para iniciarmos por aqui. Então no diretório do useCase, `createRental/`, vamos adicionar o teste `CreateRentalUseCase.spec.ts`.

```ts
let createRentalUsecase: CreateRentalUseCase;
let rentalsRepositoryInMemory: RentalsRepositoryInMemory;

describe("Create Rental", () => {
  beforeEach(() => {
    rentalsRepositoryInMemory = new RentalsRepositoryInMemory();
    createRentalUsecase = new CreateRentalUseCase(rentalsRepositoryInMemory);
  });
  it("shouuld be able  to create an new rental", async () => {
    await createRentalUsecase.execute({
      car_id: "123212",
      expected_return_date: new Date(),
      user_id: "452365",
    });
  });
});
```
Test 🚧

## Aula CXIII
> Continuação do cadastro do aluguel

Continuando o nosso projeto, vamos retomar a parte na parte repositório onde definir na interface e implementa no repositório do teste o método de criação do rental.


**`IRentalRepository.ts`:**
```ts
interface IRentalsRepository {
  create(data: ICreateRentalDTO): Promise<Rental>;
  // RESTO DO CÓDIGO
}
export { IRentalsRepository };
```

Vamos criar a interface da requisição de create pois muito provavelmente iremos utilizá-la mais a diante na aplicação.

**`ICreateRentalDTO.ts`:**
```ts
interface ICreateRentalDTO {
  user_id: string;
  car_id: string;
  expected_return_date: Date;
}
export { ICreateRentalDTO };
```

Impelementando método de criação no repositório de testes.

**`RentalRepositoryInMemory.ts`:**
```ts
class RentalsRepositoryInMemory implements IRentalsRepository {
  rentals: Rental[] = [];

  async create({
    user_id,
    car_id,
    expected_return_date,
  }: ICreateRentalDTO): Promise<Rental> {
    const rental = new Rental();
    Object.assign(rental, {
      user_id,
      car_id,
      expected_return_date,
      start_date: new Date(),
    });

    this.rentals.push(rental);

    return rental;
  }
  // RESTO DO CÓDIGO
}
export { RentalsRepositoryInMemory };
```

Criando rental no useCase.

**`CreateRentalUseCase.ts`:**
```ts
interface IRequest {
  user_id: string;
  car_id: string;
  expected_return_date: Date;
}
class CreateRentalUseCase {
  constructor(private rentalsRepository: IRentalsRepository) {}

  async execute({
    car_id,
    expected_return_date,
    user_id,
  }: IRequest): Promise<Rental> {
    const carUnavailabel = await this.rentalsRepository.findOpenRentalByCar(
      car_id
    );
    if (carUnavailabel) { throw new AppError("Car is unavailable"); }
    const rentalOpenToUser = await this.rentalsRepository.findOpenRentalByUser( user_id );
    if (rentalOpenToUser) { throw new AppError("There's a rental in progress for user"); }
    // criando e guardando na variável rental 
    const rental = await this.rentalsRepository.create({
      user_id,
      car_id,
      expected_return_date,
    });
    // retornando o rental
    return rental;
  }
}
export { CreateRentalUseCase };
```

Criando testes.

**`CreateRentalUseCase.spec.ts`:**
```ts
let createRentalUsecase: CreateRentalUseCase;
let rentalsRepositoryInMemory: RentalsRepositoryInMemory;

describe("Create Rental", () => {
  beforeEach(() => {
    rentalsRepositoryInMemory = new RentalsRepositoryInMemory();
    createRentalUsecase = new CreateRentalUseCase(rentalsRepositoryInMemory);
  });
  // deve ser capaz de criar um novo aluguel
  it("should be able  to create an new rental", async () => {
    const rental = await createRentalUsecase.execute({
      car_id: "123212",
      expected_return_date: new Date(),
      user_id: "452365",
    });
    expect(rental).toHaveProperty("id");
    expect(rental).toHaveProperty("start_date");
  });
  // não deve ser capaz de criar um novo aluguel se houver outra oportunidade para o mesmo usuário
  it("should not be able to create an new rental if there is another opento to the same user", async () => {
    expect(async () => {
      await createRentalUsecase.execute({
        car_id: "123212",
        user_id: "452365",
        expected_return_date: new Date(),
      });

      await createRentalUsecase.execute({
        car_id: "123212",
        expected_return_date: new Date(),
        user_id: "452365",
      });
    }).rejects.toBeInstanceOf(AppError);
  });
  // não deve ser capaz de criar um novo aluguel se houver outra oportunidade para o mesmo carro
  it("should not be able to create an new rental if there is another opento to the same car", async () => {
    expect(async () => {
      await createRentalUsecase.execute({
        user_id: "341290",
        car_id: "test",
        expected_return_date: new Date(),
      });

      await createRentalUsecase.execute({
        user_id: "452365",
        car_id: "test",
        expected_return_date: new Date(),
      });
    }).rejects.toBeInstanceOf(AppError);
  });
});
```

## Aula CXIV
> Trabalhando com datas com dayjs

Afim de cumprir o requisito do alguel ter uma duração mínima de 24horas, precisamos nos atentar a data no momento do cadastro e a data que ele informa realizar a devolução e assim verificar se se é maior que o tempo mínimo. Para trabalhar com as dastas de um jeito mais ágil, vamos utilizar a biblioteca dayjs, adicionando ela ao projeto com o comando: `yarn add dayjs`.

No useCase, além de importarmos o dayjs vamos importar o utc com `import utc from "dayjs/plugin/utc";` para "padronizar" os horários, não havendo assim erros nos cálculos.

**`CreateRentalUseCase.ts`:**

```ts
// importando dayjs e utc
import dayjs from "dayjs";
import utc from "dayjs/plugin/utc";
// usa utc
dayjs.extend(utc);

interface IRequest {
  // Request
}
class CreateRentalUseCase {
  constructor(private rentalsRepository: IRentalsRepository) {}

  async execute({
    car_id,
    expected_return_date,
    user_id,
  }: IRequest): Promise<Rental> {
    const minimumHour = 24;

    // RESTANTE DAS VALIDAÇÕES

    // O Alguel dever ter duração mínima de 24horas
    // Formatando o horário eperado
    const expectedReturnDateFormmat = dayjs(expected_return_date)
      .utc()
      .local()
      .format();
    // Formatando horário atual
    const dateNow = dayjs().utc().local().format();
    // Comparando horrário
    const compare = dayjs(expectedReturnDateFormmat).diff(dateNow, "hours");
    if (compare < minimumHour) {
      throw new AppError("Invalid return time!");
    }
    // Se estive tudo certo, cria o aluguel
    const rental = await this.rentalsRepository.create({
      user_id,
      car_id,
      expected_return_date,
    });
    // retorna rental
    return rental;
  }
}
export { CreateRentalUseCase };
```

**`CreateRentalUseCase.spec.ts`:**
```ts
describe("Create Rental", () => {
  const dayAdd24Hours = dayjs().add(1, "day").toDate();

  beforeEach(() => {
    rentalsRepositoryInMemory = new RentalsRepositoryInMemory();
    createRentalUsecase = new CreateRentalUseCase(rentalsRepositoryInMemory);
  });
  // não deve ser capaz de criar um novo aluguel com tempo de devolução inválido
  it("should not be able to create a new rental with invalid return time", async () => {
    expect(async () => {
      await createRentalUsecase.execute({
        user_id: "341290",
        car_id: "test",
        expected_return_date: dayjs().toDate(),
      });
    }).rejects.toBeInstanceOf(AppError);
  });
});
```

## Aula CXV
> Criando provider para data

Afim de otimizar o uso do dayjs, facilitar a manutenção, vamos criar um provider, que assim como o repositório, vmos criar a interface e vamos criar o arquivo de implementação utilizando o dayjs. Na pasta `shared/container`, vamos criar o diretório `providers/`, contendo o `DateProvider/`, onde sera criado o arquivo de inerface, `IDateProvider.ts`, com a seguinte estrutura:

```ts
interface IDateProvider {
  compareInHours(start_date: Date, end_date: Date): number;
  convertToUTC(date: Date): string;
  dateNow(): Date;
}
export { IDateProvider };
```

Ainda na pasta `DateProvider/`, vamos criar outro diretório chamado `implematations/` e implementar na class `DayjsDateProvider` que vamos criar nesse diretório a interface **`IDateProvider`**.

```ts
class DayjsDateProvider implements IDateProvider {
  dateNow(): Date {
    return dayjs().toDate();
  }
  compareInHours(start_date: Date, end_date: Date): number {
    const end_date_utc = this.convertToUTC(end_date);
    const start_date_utc = this.convertToUTC(start_date);
    return dayjs(end_date_utc).diff(start_date_utc, "hours");
  }
  convertToUTC(date: Date): string {
    return dayjs(date).utc().local().format();
  }
}
export { DayjsDateProvider };
```
Class implementada, vamos utilizar el agora no nosso use case deixando ele mais organizado e mais simples de entender.
**`CreaterentalUseCase.ts`:**
```ts
// UTILIZANDO O UTC DO DAYJS
dayjs.extend(utc);
// INTERFACE DO REQUEST
interface IRequest {
  user_id: string;
  car_id: string;
  expected_return_date: Date;
}
class CreateRentalUseCase {
  constructor(
    private rentalsRepository: IRentalsRepository,
    private dateProvider: IDateProvider
  ) {}

  async execute({
    car_id,
    expected_return_date,
    user_id,
  }: IRequest): Promise<Rental> {
    const minimumHour = 24;
    // VALIDAÇÃO DO CARRO
    const carUnavailabel = await this.rentalsRepository.findOpenRentalByCar(
      car_id
    );
    if (carUnavailabel) {
      throw new AppError("Car is unavailable");
    }
    // VALIDAÇÃO DO USUÁRIO
    const rentalOpenToUser = await this.rentalsRepository.findOpenRentalByUser(
      user_id
    );
    if (rentalOpenToUser) {
      throw new AppError("There's a rental in progress for user");
    }
    // VALIDAÇÃO POR TEMPO MÍNIMO
    // O alguel dever ter duração mínima de 24horas

    // UTILIZANDO OS MÉTODOS CRIADOS COM O PROVIDER
    const dateNow = this.dateProvider.dateNow();
    const compare = this.dateProvider.compareInHours(
      dateNow,
      expected_return_date
    );
    // VALIDANDO
    if (compare < minimumHour) {
      throw new AppError("Invalid return time!");
    }
    // SALVANDO RENTAL
    const rental = await this.rentalsRepository.create({
      user_id,
      car_id,
      expected_return_date,
    });
    // RETORNANDO RENTAL
    return rental;
  }
}
export { CreateRentalUseCase };
```

**`CreaterentalUseCase.spec.ts`:**
```ts
// Iniciando e tipiando variáveis
let createRentalUsecase: CreateRentalUseCase;
let rentalsRepositoryInMemory: RentalsRepositoryInMemory;
let dayjsDateProvider: DayjsDateProvider;

describe("Create Rental", () => {
  const dayAdd24Hours = dayjs().add(1, "day").toDate();

  beforeEach(() => {
    rentalsRepositoryInMemory = new RentalsRepositoryInMemory();
    // Instanciado Provider
    dayjsDateProvider = new DayjsDateProvider();
    createRentalUsecase = new CreateRentalUseCase(
      rentalsRepositoryInMemory,
      dayjsDateProvider
    );
  });
  // RESTO DO CÓDIGO
});
```

## Aula CXVI
> Criando controller

**Correções**
Antes de darmos continuidade, vamos voltar u pouco no prjeto mais uma vez, para rever alguns pontos.

Migration: Ao criarmos um rental, ou seja, um linha na tabela `rentals`, duas colunas serão inicializadas como nulas e será preenchida posteriormente, são elas as colunas de `end_date` e `total`.
**`CreateRentals`:**
```ts
export class CreateRentals1625590443953 implements MigrationInterface {
  public async up(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.createTable(
      new Table({
        name: "rentals",
        columns: [
          // PARTE ANTERIOR DO CÓDIO
          { name: "end_date", type: "timestamp", isNullable: true },
          { name: "total", type: "numeric", isNullable: true },
          // RESTO DO CÓDIGO
        ],
        foreignKeys: [
          // MAIS CÓDIO
        ],
      })
    );
  }
  public async down(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.dropTable("rentals");
  }
}
```
Entity: Agora vamos preencher rapudidamente as entities com os decorators do typeorm.

**`Rentals`:**

```ts
@Entity("rentals")
class Rental {
  @PrimaryColumn()
  id: string;

  @Column()
  car_id: string;

  @Column()
  user_id: string;

  @Column()
  start_date: Date;

  @Column()
  end_date: Date;

  @Column()
  expected_return_date: Date;

  @Column()
  total: number;

  @CreateDateColumn()
  created_at: Date;

  @UpdateDateColumn()
  updated_at: Date;

  constructor() {
    if (!this.id) {
      this.id = uuidv4();
    }
  }
}
export { Rental };
```

**Continuando aplicação...**

Repository: Antes de criarmos o controller, precisamos criar o repository e implmentar os métodos que criamos na interface `IRentalsRepository`, ir no container e apontar ele para o tsrynge asim como também o `DayjsDateProvider`, e adicionar os decorators do tsrynge no useCase.

**`RentalsRepository.ts`:**

```ts
class RentalsRepository implements IRentalsRepository {
  private repository: Repository<Rental>;

  constructor() {
    // buscndo o repository que a entidde Rental, faz referência 
    this.repository = getRepository(Rental);
  }
  // cria rental
  async create({
    car_id,
    expected_return_date,
    user_id,
  }: ICreateRentalDTO): Promise<Rental> {
    const rental = this.repository.create({
      car_id,
      expected_return_date,
      user_id,
    });
    await this.repository.save(rental);
    return rental;
  }
  // busca rental a partir de id do carro informado
  async findOpenRentalByCar(car_id: string): Promise<Rental> {
    const openByCar = await this.repository.findOne({ car_id });
    return openByCar;
  }
  // busca rental a partir de id de usuário
  async findOpenRentalByUser(user_id: string): Promise<Rental> {
    const openByUser = await this.repository.findOne({ user_id });
    return openByUser;
  }
}
export { RentalsRepository };
```

Providers: Na pasta `providers/` criada em `shared/container/` vamos adicionar  o arquivo `index.ts` com a seguinte estrutura.

**`providers/index.ts`:**

```ts
container.registerSingleton<IDateProvider>(
  "DayjsDateProvider",
  DayjsDateProvider
);
```
Container: Seguindo a mesma estrutura que foi ralizada com os repository anteriores.

**`container/index.ts`:**

```ts
// RESTO DO CÓDIGO
container.registerSingleton<IRentalsRepository>(
  "RentalsRepository",
  RentalsRepository
);
```
UseCase: Vamos adcionar o `@injectable()` e `@inject()` como recomendado.

**`CreateRentalUseCase.ts`:**

```ts
@injectable()
class CreateRentalUseCase {
  constructor(
    @inject("RentalsRepository")
    private rentalsRepository: IRentalsRepository,
    @inject("DayjsDateProvider")
    private dateProvider: IDateProvider
  ) {}

  async execute({
    car_id,
    expected_return_date,
    user_id,
  }: IRequest): Promise<Rental> {
    const minimumHour = 24;

  // RESTO DO CÓDIGO
  }
}
export { CreateRentalUseCase };
```
Controller: No Controller,  vamos seguir a estrutura padrão que vemo adotando, lembrando que vamos pegar o id do `request.user` que será passado por meio do middleware de `ensureAuthenticated`.

**`CreateRentalController.ts`:**

```ts
class CreateRentalController {
  async handle(request: Request, response: Response): Promise<Response> {
    // capturando variáveis do body
    const { expected_return_date, car_id } = request.body;
    // capturando variáveis do middleware ensureAuthenticated
    const { id } = request.user;
    // "instanciando" useCase
    const createRentalUseCase = container.resolve(CreateRentalUseCase);
    // executando useCase
    const rental = await createRentalUseCase.execute({
      car_id,
      expected_return_date,
      user_id: id,
    });
    // retornando status e rental criado em formato Json
    return response.status(201).json(rental);
  }
}
export { CreateRentalController };
```

Routes: Na pasta shared/infra/http/routes/ vamos criar o arquivo `rental.routes.ts` com a seguinte estrura, em seguida, vamos chamar no arquivo `index.ts` do diretório routes.

**`rentl.routes.ts`:**

```ts
const rentalsRoutes = Router();

const createRentalController = new CreateRentalController();

rentalsRoutes.post("/", ensureAuthenticated, createRentalController.handle);

export { rentalsRoutes };
```

`routes/index.ts`

routes:
```ts
router.use("/rentals", rentalsRoutes);
```

## Aula CXVII
> Configurando supertest

Aqui vamos começar  a implantar a supertest na nssa aplicação. Para isso precisamos desacoplar o `app` do nosso `server`. Assim, vamos renomear o arquivo `server.ts` para `app.ts` e depois substituir o `listen(...)` pelo `export{ app }`. e criar um arquivo na msm pasta, `shared/infra/http/`, o arquivo `server.ts`, com o seguinte código:
```ts
import { app } from "./app";

app.listen(3333, () => console.log("Server is running"));
```
Desacoplado nosso app agora pode "interegarir co outras partes da nossa aplicação, no caso, com o supertest que vamos instalar agora.
instala supertest: `yarn add supertest`
instala types/supertest: `yarn add @types/supertest -D`

Vamos iniciar implatar o supertest no createCategory, criando o arquivo `CreateCategoryController.spec.ts` onde vamos iniciar com a seguinte estrutura:
**`CreateCategoryController.spec.ts`:**

```ts
import request from "supertest";

import { app } from "@shared/infra/http/app";

describe("Create category Controller", () => {
  it("test", async () => {
    await request(app).get("/cars/available").expect(200);
  });
});
```

## Aula CXVIII
> Criando o primeiro teste de integração

Vamos começar nosso teste de integração pelo arquivo `CreateCategoryController.spec.ts`:

```ts
describe("Create category Controller", () => {
  it("should be able to create a new category", async () => {
    const response = await request(app).post("/categories").send({
      name: "Category Supertest",
      description: "category Supertest",
    });
    expect(response.status).toBe(201);
  });
});
```

Para trabalharmos com testes, é preciso que ele não modifique o banco de dados da nossa aplicação, com isso, vamos criar um banco de dados para os nossos teste e para isso vamos executr o seguinte comando na query do beekeeper:
```sql
CREATE DATABASE retals_test;
```
Para que nosso test não utilize o banco de dados da nossa aplicação, temos que indicar isso para ele. Então, no arquivo `index.ts` do diretório `shared/infra/typeorm/` vamos fazer a seguinte modificação:

```ts
export default async (host = "database_ignite"): Promise<Connection> => {
  const defaultOptions = await getConnectionOptions();

  return createConnection(
    Object.assign(defaultOptions, {
      // caso o NODE_ENV seja igual a "test" host recebe "localhost", caso contrário host recebe host
      host: process.env.NODE_ENV === "test" ? "localhost" : host,
      // caso o NODE_ENV seja igual a "test", database receberá rentals_test, se não, utilize o padrão
      database:
        process.env.NODE_ENV === "test"
          ? "rentals_test"
          : defaultOptions.database,
    })
  );
};
```

E como vamos passar essa variável e ambiente? Existem várias formas, a que vamos utilizar no momento é pelo script do test no package.json, onde:
```json
{
  "scripts": {
    "test": "NODE_ENV=test jest"
  }
}
```

## Aula CXIX
> Continuando teste de integração

```ts
import { hash } from "bcrypt";
import request from "supertest";
import { Connection } from "typeorm";
import { v4 as uuidv4 } from "uuid";

import { app } from "@shared/infra/http/app";
import createConnection from "@shared/infra/typeorm";

let connection: Connection;

describe("Create category Controller", () => {
  beforeAll(async () => {
    // Antes de tudo vamos criar uma conexão
    connection = await createConnection();
    // esta conexão irá rodar nossas migrations
    await connection.runMigrations();
    // gerando um uuid
    const id = uuidv4();
    // gerando o hash da senha "admin"
    const password = await hash("admin", 8);
    // criando query q adciona um admin
    await connection.query(
      `INSERT INTO USERS(id, name, email, password, "isAdmin", created_at, driver_license )
      values('${id}', 'admin', 'admin@rentalx.com.br', '${password}', true, 'now()', '123456')`
    );
  });
  // Ao final de todo teste será apagado o banco de dados e a conexão será fechada
  afterAll(async () => {
    await connection.dropDatabase();
    await connection.close();
  });

  it("should be able to create a new category", async () => {
    // cria sessão (token)
    const responseToken = await request(app).post("/sessions").send({
      email: "admin@rentalx.com.br",
      password: "admin",
    });
    // Pegando o token criado
    const { token } = responseToken.body;
    // criando a nova categoria uzando o token criado
    const response = await request(app)
      .post("/categories")
      .send({
        name: "Category Supertest",
        description: "category Supertest",
      })
      .set({
        Authorization: `Bearer ${token}`,
      });
    // Espera-se receber o status code 201 da requisição
    expect(response.status).toBe(201);
  });
});
```

## Aula CXX
> Criando teste de listagem de categorias

COntinuando os testes de criação de categorias, vamos criar um test que diga que não é possível criar uma categoria com um nome já exitente para isso vamos adicionar o seguinte código ao arquivo de **`CreateCategoryController.spec.ts`**.
```ts
describe("Create category Controller", () => {
  // Resto do código
  // Com o beforeAll e o afterAll, os nosos dados criados só serão apagados ao final de todo processo, assim vamos tentar criar outra categoria e esperar um erro 400

  it("should not be able to create a new category with name exists", async () => {
    // cria sessão (token)
    const responseToken = await request(app).post("/sessions").send({
      email: "admin@rentalx.com.br",
      password: "admin",
    });
    // Pegando o token criado
    const { token } = responseToken.body;
    // criando a nova categoria uzando o token criado
    const response = await request(app)
      .post("/categories")
      .send({
        name: "Category Supertest",
        description: "category Supertest",
      })
      .set({
        Authorization: `Bearer ${token}`,
      });
    // espera que a categoria não possa sercriada
    expect(response.status).toBe(400);
  });
});
```

Antes de finalizar esse capítulo vamos ver o teste para listar nossas categorias. Etnão, no useCase `listCategories`, vamos criar o arquivo `ListCategoriesController.spec.ts` com a seguinte estrutura:

```ts
let connection: Connection;

describe("List category Controller", () => {
  beforeAll(async () => {
    // Antes de tudo vamos criar uma conexão
    connection = await createConnection();
    // esta conexão irá rodar nossas migrations
    await connection.runMigrations();
    // gerando um uuid
    const id = uuidv4();
    // gerando o hash da senha "admin"
    const password = await hash("admin", 8);
    // criando query q adciona um admin
    await connection.query(
      `INSERT INTO USERS(id, name, email, password, "isAdmin", created_at, driver_license )
      values('${id}', 'admin', 'admin@rentalx.com.br', '${password}', true, 'now()', '123456')`
    );
  });
  // Ao final de todo teste será apagado o banco de dados e a conexão será fechada
  afterAll(async () => {
    await connection.dropDatabase();
    await connection.close();
  });

  it("should be able to list all categories", async () => {
    // cria token
    const responseToken = await request(app).post("/sessions").send({
      email: "admin@rentalx.com.br",
      password: "admin",
    });
    // Pega token
    const { token } = responseToken.body;
    // Cria Categoria
    await request(app)
      .post("/categories")
      .send({
        name: "Category Supertest",
        description: "Category Supertest",
      })
      .set({
        Authorization: `Bearer ${token}`,
      });
    // Lista categorias
    const response = await request(app).get("/categories");
    // Espera status 200
    expect(response.status).toBe(200);
    // espera ter uma lista
    expect(response.body.length).toBe(1);
    // Espera ter a propriedade "id" no primeiro item dentro do body
    expect(response.body[0]).toHaveProperty("id");
    // Espera o nome da categoria "Category Supertest"
    expect(response.body[0].name).toEqual("Category Supertest");
  });
});
```

## Aula CXXI
> Introdução ao cap V

- Implementação de funcionalidades
- Refresh Token
- Envio de email com template customizado
- Correção de testes

## Aula CXXII
> Migration de devolução de carro

Vamos agora continuar com a parte do aluguel, no que tange a parte de devolução do aluguel, lembrando que:

### Devolução do carro

**RF**

  Deve ser possível realizar a devolução de um carro

**RN**

  Se o carro for devolvido com menos de 24 horas, deverá - ser cobrado diária completa.
  Ao realizar a devolução, o carro deverá ser liberado para - outro aluguel.
  Ao realizar a devolução, o usuário deverá ser liberado - para outro aluguel.
  Ao realizar a devolução, deverá ser calculado o total do - aluguel.
  Caso o horário de devolução seja superior ao horário - previsto de entrega, deverá ser cobrado multa - proporcional aos dias de atraso.
  Caso haja multa, deverá ser somado ao total do aluguel.
  O usuário deve estar logado na aplicação

Obersarvamos agora uma pequena falha, na criação do aluguel onde deve ser alterado o estado de carro indisponível assim que criado um aluguel com determinado veículo, coisa que no momento não ocorre, para corrigir isso, vamos pontuar o que iremos fazer:

- Criação de método para fazer update do estado de `available` do carro;
  - Apontar na interface `ICarsRepository`.
  - Criar o método no `CarsRepository`
  - Criar o método no `CarsRepositoryInMemory`
- Usar método no `CreateRentalUseCase`
- Usar método no `CreateRentalUseCase.spec`

**`ICarsRepository`:**

```ts
interface ICarsRepository {
  // Resto do código
  updateAvailable(id: string, available: boolean): Promise<void>;
}
```

**`CarsRepository`:**

```ts
class CarsRepository implements ICarsRepository {
  private repository: Repository<Car>;

  constructor() {
    this.repository = getRepository(Car);
  }

  // Resto do código

  async updateAvailable(id: string, available: boolean): Promise<void> {
    await this.repository
      .createQueryBuilder()
      .update()
      .set({ available })
      .where("id = :id")
      .setParameters({ id })
      .execute();
  }
}
```

**`CarsRepositoryInMemory`:**

```ts
class CarsRepositoryInMemory implements ICarsRepository {
  async updateAvailable(id: string, available: boolean): Promise<void> {
    const findIndex = this.cars.findIndex((car) => car.id === id);
    this.cars[findIndex].available = available;
  }
}
```

**`CreateRentalUseCase`:**

```ts
@injectable()
class CreateRentalUseCase {
  constructor(
    // @injections...
  ) {}

  async execute({
    car_id,
    expected_return_date,
    user_id,
  }: IRequest): Promise<Rental> {
    // Resto do código

    // passando o id e o parâmetro "false"
    await this.carsRepository.updateAvailable(car_id, false);
    return rental;
  }
}
```

**`CreateRentalUseCase.spec`:**

```ts
let createRentalUsecase: CreateRentalUseCase;
let rentalsRepositoryInMemory: RentalsRepositoryInMemory;
// chamando o repositório de carros para testes
let carsRepositoryInMemory: CarsRepositoryInMemory;
let dayjsDateProvider: DayjsDateProvider;

describe("Create Rental", () => {
  const dayAdd48Hours = dayjs().add(2, "day").toDate();

  beforeEach(() => {
    rentalsRepositoryInMemory = new RentalsRepositoryInMemory();
    // instanciando o repositório de carros
    carsRepositoryInMemory = new CarsRepositoryInMemory();
    dayjsDateProvider = new DayjsDateProvider();
    createRentalUsecase = new CreateRentalUseCase(
      rentalsRepositoryInMemory,
      dayjsDateProvider,
      // passando o repositório de carros como paramêtro para o useCase
      carsRepositoryInMemory
    );
  });
  // Resto do código
}
```

## Aula CXXIII
> Caso de Uso de devolução de carro

Nesse momento vamoscriar o caso de uso de devolução de carros. Para isso em `useCase/` do módulo `rentals`, vamos criar o diretório `devolutionRental/` com os arquivos `DevolutionRentalUseCase.ts` e `DevolutionRentalController.ts`.

**`DevolutionRentalUseCase.ts`:**
```ts
interface IRequest {
  id: string;
  user_id: string;
}

@injectable()
class DevolutionRentalUseCase {
  constructor(
    @inject("RentalsRepository")
    // Instaciar repositório de rentals
    private rentalsRepository: IRentalsRepository,
    // Instaciar provider de Date
    @inject("DayjsDateProvider")
    private dateProvider: IDateProvider,
    // Instaciar repositório de cars
    @inject("CarsRepository")
    private carsRepository: ICarsRepository
  ) {}

  async execute({ user_id, id }: IRequest): Promise<Rental> {
    // diária mínimade 1 dia
    const minimum_daily = 1;
    // Vamos criar um método para buscar um rental pelo seu id
    // rental que corresponde a este id
    const rental = await this.rentalsRepository.findById(id);
    // car que corresponde ao id contido na tabela de cars
    const car = await this.carsRepository.findById(rental.car_id);

    // se não existir rental com este id, retorna um erro
    if (!rental) {
      throw new AppError("Rental does not exists!");
    }

    // Pega a data no presente momento
    const dateNow = this.dateProvider.dateNow();
    // diferença em dias do início do aluguel até o presente momento, ou seja o número de diárias
    let daily = this.dateProvider.compareInDays(
      rental.start_date,
      this.dateProvider.dateNow()
    );
    // se a diária for menor ou igual a 0, set o daily em no mínimo de diárias permitida, que é de 1 dia
    if (daily <= 0) {
      daily = minimum_daily;
    }
    // número de dias que atrasou a entrega
    // método que será criado no DayjsdateProvider
    const delay = this.dateProvider.compareInDays(
      dateNow,
      rental.expected_return_date
    );
    // total a ser pago
    let total = 0;
    // se atrasou a entregar o carro, vamos calcular a multa
    if (delay > 0) {
      // dias em atraso * valor da multa por dia
      const calculate_fine = delay * car.fine_amount;
      // gauda em total
      total = calculate_fine;
    }
    // somando o valor da multa com a diária do carro para os retardatários
    // ou simplesmete caclculando o valor da diária, caso o usuário tenha entregue em dia
    total += daily * car.daily_rate;
    // passando o dia de entrega desse aluguel para
    rental.end_date = this.dateProvider.dateNow();
    // passando o valor total do aluguel paa a tabela
    rental.total = total;
    // salvando as informações que passamos
    // aqui vamo fazer um adendo pois atualemnte o nosso rentalsRepository não consegue receber alguns parâmetros que passamos aqui, para isso vamos ter que modificar o ICreateRentalDTO e o Rentalsrepository
    await this.rentalsRepository.create(rental);
    // atualizando o carro como available
    await this.carsRepository.updateAvailable(car.id, true);
    // retonrando o rental
    return rental;
  }
}
```

**`ICreateRentalDTO`:**

```ts
interface ICreateRentalDTO {
  user_id: string;
  car_id: string;
  expected_return_date: Date;
  // ao criar o rental não passamos esses parâmetros pois eles não existem
  // ao atualizarmos utilizando o método create(), presicamos tornar esses paramêtros como opicionais para serem usados tanto na criação quanto no update
  id?: string;
  end_date?: Date;
  total?: number;
}
```

**`IRentalsrepository`:**

```ts
interface IRentalsRepository {
  // Resto do código
  findById(id: string): Promise<Rental>;
}

```

**`Rentalsrepository`:**

```ts
class RentalsRepository implements IRentalsRepository {
  private repository: Repository<Rental>;

  constructor() {
    this.repository = getRepository(Rental);
  }
  // passando os parâmetros
  async create({
    car_id,
    expected_return_date,
    user_id,
    id,
    end_date,
    total,
  }: ICreateRentalDTO): Promise<Rental> {
    const rental = this.repository.create({
      // recebendo os parâmetros caso existam
      car_id,
      expected_return_date,
      user_id,
      id,
      end_date,
      total,
    });
    await this.repository.save(rental);
    return rental;
  }
  // Resto do código
  async findById(id: string): Promise<Rental> {
    const rental = this.repository.findOne(id);
    return rental;
  }
}
```

`IDateProvider`

```ts
interface IDateProvider {
  // Resto do código
  compareInDays(start_date: Date, end_date: Date): number;
}
```

`DayjsDateProvider`

```ts
class DayjsDateProvider implements IDateProvider {
  // Resto do Código
  compareInDays(start_date: Date, end_date: Date): number {
    // padroniza o formato das datas
    const end_date_utc = this.convertToUTC(end_date);
    const start_date_utc = this.convertToUTC(start_date);
    // retorna a diferença em dias entre a data finale a data inicial
    return dayjs(end_date_utc).diff(start_date_utc, "days");
  }
}
```


## Aula CXXIV
> Controller de devolução de carro

Continuando a nossa aplicação vamos passar para o controller onde vamos pegar as request e executar o use case.

**`DevolutionRentalController.ts`:**

```ts
class DevolutionRentalController {
  async handle(request: Request, response: Response): Promise<Response> {
    const devolutionRentalUseCase = container.resolve(DevolutionRentalUseCase);
    // vamos pegar o id do user que vem do middleware e passar como user_id
    const { id: user_id } = request.user;
    // pega o id da url
    const { id } = request.params;
    // fazer a devolução e esperar o retorno do rental
    const rental = await devolutionRentalUseCase.execute({
      id,
      user_id,
    });
    // passar o rental como json e status code, 200
    return response.status(200).json(rental);
  }
}
```

**`rental.routes.ts`:**

```ts
// Resto do código
const createRentalController = new CreateRentalController();
const devolutionRentalController = new DevolutionRentalController();

rentalsRoutes.post("/", ensureAuthenticated, createRentalController.handle);
rentalsRoutes.post(
  // caminho
  "/devolution/:id",
  // autentificação do usuário
  ensureAuthenticated,
  // passando o controller
  devolutionRentalController.handle
);
```

`RentalsRepository.ts`

```ts
class RentalsRepository implements IRentalsRepository {
  // Resto do código
  async findOpenRentalByCar(car_id: string): Promise<Rental> {
    const openByCar = await this.repository.findOne({
      // pega esse rental onde o car_id for esse que te passei e o end_date for nulo
      where: { car_id, end_date: null },
    });
    return openByCar;
  }
  async findOpenRentalByUser(user_id: string): Promise<Rental> {
    const openByUser = await this.repository.findOne({
      // pega esse rental onde o user_id for esse que te passei e o end_date for nulo
      where: { user_id, end_date: null },
    });
    return openByUser;
  }
}
```

## Aula CXXV
> Listagem de aluguéis do usuário

Agora vamos criar a funcionalidade de listar aluguéis por usuários, Nessa intenção, vamos criar um diretório em `useCase/` do módulo `rentals`, chamado `listRentalsByUser` com as classes `ListRentalsByUserUseCase` e `ListRentalsByUserController`.

**`ListRentalsByUserUseCase.ts`:**

```ts
@injectable()
class ListRentalsByUserUseCase {
  constructor(
    // pegando o repositório de rentals
    @inject("RentalsRepository")
    private rentalsRepository: IRentalsRepository
  ) {}
  async execute(user_id: string): Promise<Rental[]> {
    // vamos futuramente criar o método findByUser no repositório de rentals
    // esse método vai buscar os rentals com o usuário que foi passado
    const rentalsByUser = await this.rentalsRepository.findByUser(user_id);
    // retorna os rentals buscados pelo método findByUser
    return rentalsByUser;
  }
}
```
Agora vamos criar o método que ficou faltando ser criado.

**`IRentalsRepository.ts`:**

```ts
interface IRentalsRepository {
  // Resto do código
  findByUser(user_id: string): Promise<Rental[]>;
}
```

**`RentalsRepository.ts`:**

```ts
class RentalsRepository implements IRentalsRepository {
  // Resto do código
  async findByUser(user_id: string): Promise<Rental[]> {
    const rentals = this.repository.find({ user_id });

    return rentals;
  }
}
```
Repositório e UseCase finalizados vamos agora para o controller.

**`ListRentalsByUserController.ts`:**

```ts
class ListRentalsByUserController {
  async handel(request: Request, response: Response): Promise<Response> {
    // pegando o id do middleware
    const { id } = request.user;
    // instanciando o useCase
    const listRentalsByUserUseCase = container.resolve(
      ListRentalsByUserUseCase
    );
    // Executando o useCase
    const rentals = await listRentalsByUserUseCase.execute(id);
    // retornando os rentals
    return response.json(rentals);
  }
}
```

E para finalizar vamos adicionar o controller ao `rental.routes.ts`

**`rental.routes.ts`:**

```ts
// Resto do código
const listRentalsByUserController = new ListRentalsByUserController();
// passando alé do controller o middleware de autentificaçãode usuário
rentalsRoutes.get(
  "/user",
  ensureAuthenticated,
  listRentalsByUserController.handel
);
```


## Aula CXXVI
> Refatorando a listagem de aluguel do usuário

Na listagem de aluguel de imóveis é apresentado o id do carro, mas caso fosse necessário mais que o id o nome e todo as outras informações, ou então para evitar que o usuário faça uma nova requesição, o que podemos fazer? podemos fazer um relacionamento onde vamos estar buscando além do id do carro, todo o objeto. Para isso vamos realizar alterações em nossa entidade de `Rentals` e no `RentalsRepository`.

`Rentals.ts`

```ts
@Entity("rentals")
class Rental {
  @PrimaryColumn()
  id: string;
  // Criando o relacionamento
  @ManyToOne(() => Car)
  @JoinColumn({ name: "car_id" })
  car: Car;
  // Resto do repositório
}
```

`RentalsRepository.ts`

```ts
class RentalsRepository implements IRentalsRepository {
  // Resto do repositório
  async findByUser(user_id: string): Promise<Rental[]> {
    const rentals = this.repository.find({
      where: { user_id },
      // buscando a tabela que possui o relacionamento
      relations: ["car"],
    });
    return rentals;
  }
}
```


## Aula CXXVII
> Criando documentação com autenticação em categoria

Aqui vamos especificar quais são as rotas que precisam de autenticação e coo a rota esperar que seja autenticada.

1 - Definir a forma de autenticação

```json
{
  "openapi": "3.0.0",
  "info": {
    // demais informações
  },
  "paths": {
    // demais informações
  },
  "definitions": {
    // demais informações
  },
  // define a forma de autenticação
  "components": {
    "securitySchemes": {
      "bearerAuth": {
        "type": "http",
        "scheme": "bearer",
        "bearerFormat": "JWT"
      }
    }
  }
}
```

2 - Inserir a autenticação na rota

```json
{
  "paths":{
    "/categories": {
      "post": {
        "tags": ["Category"],
        "summary": "Create a category",
        "description": "Create a new category",
        "security": [
          { "bearerAuth": [] }
        ],
      }
    }
  }
}
```

3 - Criar rota de criação de session (token)

```json
{
  "paths":{
    "/sessions": {
      "post":{
        "tags":["Session"],
        "summary": "Authentication user",
        "description": "Authentication user",
        "requestBody":{
          "content":{
            "application/json": {
              "schema":{
                "type":"object",
                "properties":{
                  "email": {
                    "type": "string"
                  },
                  "password": {
                    "type":"string"
                  }
                }
              }
            }
          }
        },
        "responses": {
          "200": {
            "description": "Sucess"
          },
          "400": {
            "description": "Email or password incorrect!"
          }
        }
      }
    }
  }
}
```


## Aula CXXVIII
> Replicando autenticação para documentação

dando continuidade a nossa documentação, observamos que as rotas de `/categories/import` e o `specifications` dependem de autenticação e não consta isso na documentação. Então vamos agora corrigir isso. adicionando a parte de `"security":[]`

```json
{
  "paths":{
    "/categories/import": {
      "post": {
        "tags": ["Category"],
        "summary": "Upload a new category",
        "description": "Upload a new category",
        "security": [
          { "bearerAuth": [] }
        ],
      }
    },
    "/specifications": {
      "post": {
        "tags": ["Specifications"],
        "summary":"Create a specification",
        "description": "Create a new specification",
        "security": [
          { "bearerAuth": [] }
        ],
      }
    }
  }
}
```

Para uma documentação em produção, precisa-se que ela esteja toda mapeada, para efeito de prática, iremos adicionar agora outras rotas que criamos em nossa aplicação.

```json
{
  "paths": {
    "/cars": {
      "post": {
        "tags": ["Cars"],
        "summary": "Create a new car",
        "description": "Create a new car",
        "security": [
          { "bearerAuth": [] }
        ],
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                // dentro de definitions
                "$ref": "#/definitions/Car"
              }
            }
          }
        },
        "responses": {
          "201": {
            "description": "Created"
          },
          "400": {
            "description": "Car already exists!"
          }
        }
      }
    }
  },
  "definitions": {
    "Car": {
      "type":"object",
      "properties": {
        "name": {
          "type": "string"
        },
        "description": {
          "type":"string"
        },
        "daily_rate": {
          "type": "number"
        },
        "license_plate": {
          "type": "string"
        },
        "fine_amount": {
          "type": "number"
        },
        "brand": {
          "type": "string"
        },
        "category_id": {
          "type": "string"
        }
      }
    }
  }
}
```

## Aula CXXIX
> Documentação para upload de imagens do carro

O que iremos aprender agora:

- Receber parâmetro via rota
- Receber multiplos arquivos dentro do swagger

```json
{
  "paths": {
    // enviando parâmetro "id" pela url
    "/cars/images/{id}": {
      "post": {
        "tags": ["Cars"],
        "sumary": "Upload Images",
        "description": "Upload images",
        "security": [
          { "bearerAuth": [] }
        ],
        // recebendo o prâmetro id da url
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "description": "Car id",
            "reqired": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "requestBody": {
          "content": {
            "multipart/form-data": {
              "schema": {
                "type": "object",
                "properties": {
                  "images": {
                    // habilita mais de um arquivo
                    "type": "array",
                    "items": {
                      "type": "string",
                      "format": "binary"
                    }
                  }
                }
              }
            }
          }
        },
        "responses": {
          "201": {
            "description": "Created"
          }
        }
      }
    }
  }
}
```


## Aula CXXX
> Correção dos testes

Nessa aula acabei vendo que alguns testes não estavam rodando bem, não sei se por conta do computador lento ou com conta do códig msm, apenas passarei de forma resumida.

1 - Implementação no RentlasRepositoryInMemory;
```ts
class RentalsRepositoryInMemory implements IRentalsRepository {
  // Resto do código
  async findById(id: string): Promise<Rental> {
    return this.rentals.find((rental) => rental.id === id);
  }
  async findByUser(user_id: string): Promise<Rental[]> {
    return this.rentals.filter((rental) => rental.user_id === user_id);
  }
}
```
2 - No CreateRentalUseCase.spec, no teste `"should be able to create a new rental"`, vamos criar um carro para daí então criarmos um aluguel de carros;

3 - Setar o jest para rodar os testes separadamente e verificar se existem testes em aberto;
```json
{
  "scripts": {
    "test": "NODE_ENV=test jest --runInBand --detectOpenHandles",
  }
}
```

3 - Alterar o `toBeInstanceOf()`, 
  - deixar no expect apenas a operação que estamos esperando;
  - trocar o `toBeInstanceOf()` por `toEqual(new AppError("mensagem_a_ser_passada"))`
  - Exemplo: 
  ```ts
      await expect(
        createCarUseCase.execute({
        name: "Car2",
        brand: "Brand",
        category_id: "category",
        daily_rate: 100,
        description: "Description Car",
        fine_amount: 60,
        license_plate: "ABC-1234",
      })
    ).rejects.toEqual(new AppError("Car already exists!"));
    ```

## Aula CXXXI
> Refresh Token

para que não seja necessário que um usuário esteja se autenticando e constantemente e e torne essa auteticação de forma mais automática, vamos trabalhar a partir de agora com o conceito de refresh token,

> "Um refresh token é um tipo especial de token usado para obter um token de acesso renovado. Você pode solicitar novos tokens de acesso até que o token de atualização esteja no DenyList. Os aplicativos devem armazenar tokens de atualização com segurança porque eles permitem essencialmente que um usuário permaneça autenticado para sempre."

Vamos utilizar uma tabela para armazenar os tokens dos usuário e para isso vamos criar e rodar nossa migration.

```sh
yarn typeorm migration:create -n CreateUsersToken 
```

```ts
export class CreateUsersToken1626716982571 implements MigrationInterface {
  public async up(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.createTable(
      new Table({
        name: "users_tokens",
        columns: [
          {
            name: "id",
            type: "uuid",
            isPrimary: true,
          },
          {
            name: "refresh_token",
            type: "varchar",
          },
          {
            name: "user_id",
            type: "uuid",
          },
          {
            name: "expires_date",
            type: "timestamp",
          },
          {
            name: "created_at",
            type: "timestamp",
            default: "now()",
          },
        ],
        foreignKeys: [
          {
            name: "FKUserToken",
            referencedTableName: "users",
            referencedColumnNames: ["id"],
            columnNames: ["user_id"],
            onDelete: "CASCADE",
            onUpdate: "CASCADE",
          },
        ],
      })
    );
  }

  public async down(queryRunner: QueryRunner): Promise<void> {
    await queryRunner.dropTable("users_tokens");
  }
}
```
E para  finalizar:

```sh
yarn typeorm migration:run
```

## Aula CXXXII
> Repositório de Refresh token

Com a migration executada vamos agora criar nossa Entity e iniciar nosso repositório. Então, no módulo `accounts` vamos criar a entidade de `UserTokens`

**`UserTokens.ts`:**

```ts
@Entity("users_tokens")
class UserTokens {
  @PrimaryColumn()
  id: string;

  @Column()
  refresh_token: string;

  @Column()
  user_id: string;

  // chamando o a tabela na qual faz referência
  @ManyToOne(() => User)
  @JoinColumn({ name: "user_id" })
  user: User;

  @Column()
  expires_date: Date;

  @CreateDateColumn()
  created_at: Date;

  constructor() {
    if (!this.id) {
      this.id = uuidv4();
    }
  }
}
```

Com a entity criada, vamos ao nosso repositório, antes vamos criar nossa interface, no diretório repositories, vamos criar o arquivo `IUsersTokensRepository.ts`.

**`IUsersTokensRepository.ts`:**

```ts
interface IUsersTokensRepository {
  create({
    expires_date,
    refresh_token,
    user_id,
  }: ICreateUserTokenDTO): Promise<UserTokens>;
}
export { IUsersTokensRepository };
```

Com a interface criada podemos implementar nosso repositório. Agora em `infra/typeorm/repositories/` vamos implementar no arquivo `UsersTokensRepository.ts`.

**`UsersTokensRepository.ts`:**

```ts
class UsersTokensRepository implements IUsersTokensRepository {
  private repository: Repository<UserTokens>;

  constructor() {
    this.repository = getRepository(UserTokens);
  }

  async create({
    expires_date,
    refresh_token,
    user_id,
  }: ICreateUserTokenDTO): Promise<UserTokens> {
    const UserToken = this.repository.create({
      refresh_token,
      user_id,
      expires_date,
    });

    await this.repository.save(UserToken);

    return UserToken;
  }
}
```

E agora vamos finalizar criando DTO que utilizamos no `UsersTokensRepository.ts`. No diretório `dto/` vamos criar a classe `ICreateUserTokenDTO`.
**`ICreateUserTokenDTO.ts`:**

```ts
interface ICreateUserTokenDTO {
  user_id: string;
  expires_date: Date;
  refresh_token: string;
}
```

## Aula CXXXIII
> Refatorando Autenticação do usuário

O que iremos fazer agora é implementar o nosso `UsersTokensRepository` na nossa autenticação. para isso vamos refatorar o seguinte arquivo:

**`AuthenticateUserUseCase`:**

```ts
interface IRequest {
  email: string;
  password: string;
}

interface IResponse {
  user: {
    name: string;
    email: string;
  };
  token: string;
  refresh_token: string;
}

@injectable()
class AuthenticateUserUseCase {
  constructor(
    @inject("UsersRepository")
    private usersRepository: IUsersRepository,
    // chamando o repositório de users_tokens
    @inject("UsersTokensRepository")
    private usersTokensRepository: IUsersTokensRepository,
    // chamando o privider de manipulação de tempo
    @inject("DayjsDateProvider")
    private dateProvider: DayjsDateProvider
  ) {}

  async execute({ email, password }: IRequest): Promise<IResponse> {
    const user = await this.usersRepository.findByEmail(email);
    // desestruturando variáveis que usamos para autenticação 
    // não é melhor forma devido a riscos a segurança da aplicação, nesses casos recomenda-se variáveis de ambiente
    const {
      expires_in_token,
      secret_refresh_token,
      secret_token,
      expires_in_refresh_token,
      expires_refresh_token_days,
    } = auth;

    if (!user) {
      throw new AppError("Email or password incorrect!");
    }
    const passwordMatch = await compare(password, user.password);

    if (!passwordMatch) {
      throw new AppError("Email or password incorrect!");
    }
    const token = sign({}, secret_token, {
      subject: user.id,
      expiresIn: expires_in_token,
    });
    // criando refresh_token
    const refresh_token = sign({ email }, secret_refresh_token, {
      subject: user.id,
      expiresIn: expires_in_refresh_token,
    });
    // criando validade para o refreshtoken
    const refresh_token_expires_date = this.dateProvider.addDays(
      expires_refresh_token_days
    );
    // salvando refresh_token em nosso banco de dados
    await this.usersTokensRepository.create({
      user_id: user.id,
      expires_date: refresh_token_expires_date,
      refresh_token,
    });
    // retorno do usuário
    const tokenReturn: IResponse = {
      token,
      user: {
        name: user.name,
        email: user.email,
      },
      // adicionando ao retorno, o refresh_token
      refresh_token,
    };
    return tokenReturn;
  }
}
```

Como visto, foi criando um arquivo .ts para armazenar alguns dados senssíveis, coisa que não é o recomendável a fazer, em casos assim são usadas variáveis de ambiente. sabendo disso, vamos ignorar por hora e vamos criar na nossa pasta `config/` um arquivo chamado `auth.ts` com o seguinte código:

**`auth.ts`:**

```ts
export default {
  secret_token: "7f0a80fe059648190ad441eff2bf0dae",
  secret_refresh_token: "221267d9ce40254f74d16a5d14c27fed",
  expires_in_token: "15m",
  expires_in_refresh_token: "30d",
  expires_refresh_token_days: 30,
};
```

Além do `auth.ts` que estamos usando no `AuthenticateUserUseCase` faltamos criar o método `addDays()` no dateProvider para adicionar dias ao `refresh_token.expires_date`. Então vamos fazer isso agora, começando pela interface `IDateProvider`.

**`IDateProvider`:**

```ts
interface IDateProvider {
  // Restante do código
  // obersavos que o método retornará o valor em número de dias
  addDays(days: number): Date;
}
```

Agora vamos para implementação do método `addDays()` no `DayjsDateProvider`.

**`DayjsDateProvider`:**

```ts
class DayjsDateProvider implements IDateProvider {
  dateNow(): Date {
    return dayjs().toDate();
  }
  compareInHours(start_date: Date, end_date: Date): number {
    const end_date_utc = this.convertToUTC(end_date);
    const start_date_utc = this.convertToUTC(start_date);

    return dayjs(end_date_utc).diff(start_date_utc, "hours");
  }

  convertToUTC(date: Date): string {
    return dayjs(date).utc().local().format();
  }

  compareInDays(start_date: Date, end_date: Date): number {
    const end_date_utc = this.convertToUTC(end_date);
    const start_date_utc = this.convertToUTC(start_date);

    return dayjs(end_date_utc).diff(start_date_utc, "days");
  }
  addDays(days: number): Date {
    return dayjs().add(days, "days").toDate();
  }
}
```

Agora só está faltando adicionar o repositório users_tokens ao container do tsrynge. então em `shared/container/index.ts` adicionamos o seguinte código:

**`index.ts`:**

```ts
container.registerSingleton<IUsersTokensRepository>(
  "UsersTokensRepository",
  UsersTokensRepository
);
```

## Aula CXXXIV
> Criando caso de uso do refresh token

Requesição para o cliente receber um novo refresh_token baseado no que foi expirado. Vamos começar criando um useCase, `refresh_token`, no módulo de `accounts`. Dentro desse diretório, vamos crair o UseCase e o Controller. Vamos então iniciar criando o arquivo `RefreshTokenUseCase.ts`.

**`RefreshTokenUseCase.ts`:**

```ts
interface IPayload {
  sub: string;
  email: string;
}

@injectable()
class RefreshTokenUseCase {
  constructor(
    @inject("UsersTokensRepository")
    private usersTokensRepository: IUsersTokensRepository,
    @inject("DayjsDateProvider")
    private dateProvider: IDateProvider
  ) {}

  async execute(token: string): Promise<string> {
    // verificando e buscando as iformações do token
    const { email, sub } = verify(token, auth.secret_refresh_token) as IPayload;

    const user_id = sub;
    // buscando token
    const userToken =
    // aqui vamos criar um método em nosso repositório
      await this.usersTokensRepository.findByUserIdAndRefreshToken(
        user_id,
        token
      );
    // validando token
    if (!userToken) {
      throw new AppError("Refresh Token does not exists!");
    }
    // se existir, delete
    // aqui vamos criar um método em nosso repositório
    await this.usersTokensRepository.deleteById(userToken.id);
    // criando novo token
    const refresh_token = sign({ email }, auth.secret_refresh_token, {
      subject: sub,
      expiresIn: auth.expires_in_refresh_token,
    });
    // criando data de expiração
    const expires_date = this.dateProvider.addDays(
      auth.expires_refresh_token_days
    );
    // salvando no banco de dados
    await this.usersTokensRepository.create({
      expires_date,
      refresh_token,
      user_id,
    });
    // retornando novo token
    return refresh_token;
  }
}
```

UseCase criado vamos cria os métodos que faz a validação do nosso token e que posteriormente deleta o token expirado.

**`IUsersTokensRepository`:**

```ts
interface IUsersTokensRepository {
  // resto do código
  findByUserIdAndRefreshToken(
    user_id: string,
    refresh_token: string
  ): Promise<UserTokens>;
  deleteById(id: string): Promise<void>;
}
```
E pra finalizar vamos implementar nossos métodos no repositório.

**`UsersTokensRepository`:**

```ts
class UsersTokensRepository implements IUsersTokensRepository {
  async findByUserIdAndRefreshToken(
    user_id: string,
    refresh_token: string
  ): Promise<UserTokens> {
    // buscamos apenas um pois a tendência é manter apenas um refresh_token já que vamos deletar em seguida
    const usersTokens = await this.repository.findOne({
      user_id,
      refresh_token,
    });
    return usersTokens;
  }

  async deleteById(user_id: string): Promise<void> {
    await this.repository.delete(user_id);
  }
}
```

## Aula CXXXV
> Crontroller refresh token

Seguindo com a implemntação do nosso refresh token vamos nos encaminhar agora para o controller onde teremos a seguinte estrutura:

**`RefreshTokenController.ts`:**

```ts
class RefreshTokenController {
  async handle(request: Request, response: Response): Promise<Response> {
    // pegando o token de diversas rotas
    const token =
      request.body.token ||
      request.headers["x-access-token"] ||
      request.query.token;
    // instanciando o useCase
    const refreshTokenUseCase = container.resolve(RefreshTokenUseCase);
    // executando o useCase
    const refresh_token = await refreshTokenUseCase.execute(token);
    // retorando o token
    return response.json(refresh_token);
  }
}
```
E para finalizar vamos criar uma rota onde estaremos passando este nosso controller.

**`authenticate.routes.ts`:**

```ts
// Resto do código
const authenticateUserController = new AuthenticateUserController();
const refreshTokenController = new RefreshTokenController();
// rotas de utentificação
authenticateRoutes.post("/sessions", authenticateUserController.handle);
authenticateRoutes.post("/refresh-token", refreshTokenController.handle);
```

Nesse momento o middleware de autentificação não reconhece nosso refresh token, apra que ele reconheça nosso refresh token vamos fazer algumas auterações.

**`ensureAutheticated.ts`:**

```ts
interface IPayload {
  sub: string;
}

export async function ensureAuthenticated(
  request: Request,
  response: Response,
  next: NextFunction
): Promise<void> {
  const authHeader = request.headers.authorization;

  // instanciando o repositório do reresh token 
  const userTokensRepository = new UsersTokensRepository();

  if (!authHeader) {
    throw new AppError("Token missing", 401);
  }

  const [, token] = authHeader.split(" ");

  try {
    const { sub: user_id } = verify(
      token,
      // passando a chave secreta do refresh token
      auth.secret_refresh_token
    ) as IPayload;
    // autenticando usuário
    const user = await userTokensRepository.findByUserIdAndRefreshToken(
      user_id,
      token
    );

    if (!user) {
      throw new AppError("User does not exists!", 401);
    }

    request.user = {
      id: user_id,
    };

    next();
  } catch (error) {
    throw new AppError("Invalid token", 401);
  }
}
```


## Aula CXXXVI
> Criando caso de uso recuperação de senha

Vamos criar a função na nossa aplicação de recuperação de senha.
fluxograma
- usuário passando email
- gerar token a partir do email, gerar token com expiração de 3 horas
- enviar link para o usuário com token
- usuário cria nova senha

para essa funcionalidade vamos requer a instalação da lib `nodemailer`, a qual será instalada pelo yarn com o comando: `yarn add nodemailer`.

instalado o `nodemailer` vamos criar o caso de uso responssável por esse processo de recuperação de senha. Então no módule de `accounts` vamos criar em `useCases` o diretório `SendForGotPasswordMail` com a classe `SendForGotPasswordMailUseCase` com a seguinte estrutura:

**`SendForGotPasswordMailUseCase.ts`:**

```ts
@injectable()
class SendForGotPasswordMailUseCase {
  // Repositórios 
  constructor(
    @inject("UsersRepository")
    private usersRepository: IUsersRepository,
    @inject("UsersTokensRepository")
    private usersTokensRepository: IUsersTokensRepository,
    @inject("DayjsDateProvider")
    private dateProvider: DayjsDateProvider
  ) {}
  // recebendo o email
  async execute(email: string): Promise<void> {
    // buscando o usuário pelo email informado
    const user = await this.usersRepository.findByEmail(email);
    // se não existir usuário, retorna mensagem de erro
    if (!user) {
      throw new AppError("User does not exists");
    }
    // criand o token de recuperação de se senha
    const token = uuidv4();
    // criando horário de expira
    // criar método em DayjsdateProvider
    const expires_date = this.dateProvider.addHours(3);
    // salvando token
    await this.usersTokensRepository.create({
      refresh_token: token,
      user_id: user.id,
      expires_date,
    });
  }
}
```

Agora vamos apenas criar o método que adiciona horas usado para criar a `expires_date`. Antes da criação em si, vamos indicar na interface de `IDateProvider` que estamos utilizando.
```ts
interface IDateProvider {
  // resntante do código
  addHours(hours: number): Date;
}
```

```ts
class DayjsDateProvider implements IDateProvider {
  // restante do código
  addHours(hours: number): Date {
    return dayjs().add(hours, "hour").toDate();
  }
}
```


## Aula CXXXVII
> Criando provider de e-mail

Para o envio do email, vamos usar Ethereal para simularmos o envio de emails, para que posteriormente possamos substituir por uma lib para produção, vamos criar um provider no diretório `container/providers/`.

**`IMailProvider.ts`:**

```ts
interface IMailProvider {
  sendMail(to: string, subject: string, body: string): Promise<void>;
}
```
na mesma pasta que foi criada a interface, vamos criar diretório `implementations` com o arquivo `EtherealMailProvider.ts`.

**`EtherealMailProvider.ts`:**

```ts
@injectable()
class EtherealMailProvider implements IMailProvider {
  private client: Transporter;
  // configurando o nodemailer
  constructor() {
    nodemailer
      .createTestAccount()
      .then((account) => {
        const transporter = nodemailer.createTransport({
          host: account.smtp.host,
          port: account.smtp.port,
          secure: account.smtp.secure,
          auth: {
            user: account.user,
            pass: account.pass,
          },
        });

        this.client = transporter;
      })
      .catch((err) => console.error(err));
  }
  async sendMail(to: string, subject: string, body: string): Promise<void> {
    const message = await this.client.sendMail({
      // para
      to,
      // de
      from: "Rentalx <noreplay@rentalx.com.br>",
      // assunto
      subject,
      // mensagem
      text: body,
      // mensagem
      html: body,
    });
    // receber o link
    console.log("Message sent: %s", message.messageId);
    // Preview only available when sending through an Ethereal account
    console.log("Preview URL: %s", nodemailer.getTestMessageUrl(message));
  }
}
```
Com o provider criado vamos usar o tsrynge para "instanciarmos" ele quando for necessário. Então no diretório `container/providers/` vamos adicionar o seguite código ao arquivo `index.ts`:

**`index.ts`:**

```ts
// Resto do código

container.registerInstance<IMailProvider>(
  "EtherealMailProvider",
  new EtherealMailProvider()
);
```

Agora finalmente podemos trabalhar nosso caso de uso e nosso controller antes de ir para rota.

**`SendForGotPasswordMailUseCase.ts`:**

```ts
@injectable()
class SendForGotPasswordMailUseCase {
  constructor(
    @inject("UsersRepository")
    private usersRepository: IUsersRepository,
    @inject("UsersTokensRepository")
    private usersTokensRepository: IUsersTokensRepository,
    @inject("DayjsDateProvider")
    private dateProvider: DayjsDateProvider,
    @inject("EtherealMailProvider")
    private mailProvider: IMailProvider
  ) {}
  async execute(email: string): Promise<void> {
    const user = await this.usersRepository.findByEmail(email);

    if (!user) {
      throw new AppError("User does not exists");
    }

    const token = uuidv4();

    const expires_date = this.dateProvider.addHours(3);

    await this.usersTokensRepository.create({
      refresh_token: token,
      user_id: user.id,
      expires_date,
    });
    // enviando o email pelo provider, passando o email a ser enviado e o token
    await this.mailProvider.sendMail(
      email,
      "Recupereação de Senha",
      `O link para o reset é ${token}`
    );
  }
}
```

**`SendForGotPasswordMailController.ts`:**

```ts
class SendForGotPasswordMailController {
  async handle(request: Request, response: Response): Promise<Response> {
    // pegando o email do body
    const { email } = request.body;
    // "instanciando"
    const sendForGotPasswordMailUseCase = container.resolve(
      SendForGotPasswordMailUseCase
    );
    // executando o caso de uso
    await sendForGotPasswordMailUseCase.execute(email);

    return response.send();
  }
}
```

Para manipularmos melhor as rotas que estaram envolvidas com a recuperação de senha, vamos criar o arquivo `password.routes.ts` na pasta `http/routes/` em `shared/infra/`

**`password.routes.ts`:**

```ts
import { Router } from "express";

import { SendForGotPasswordMailController } from "@modules/accounts/useCases/sendForGotPasswordMail/SendForGotPasswordMailController";

const passwordRoutes = Router();

const sendForGotPasswordMailController = new SendForGotPasswordMailController();

passwordRoutes.post("/forgot", sendForGotPasswordMailController.handle);

export { passwordRoutes };
```

E agora pegamos essa rota no **`routes/index.ts`:**

```ts
const router = Router();

router.use("/categories", categoriesRoutes);
router.use("/specifications", specificationsRoutes);
router.use("/users", usersRoutes);
router.use("/cars", carsRoutes);
router.use("/rentals", rentalsRoutes);
router.use("/password", passwordRoutes);
router.use(authenticateRoutes);

export { router };
```

## Aula CXXXVIII
> Inserindo template engine para envio de e-mail

Agora vamos melhorar nosso email, deixar ele estéticamente mais agradável. Nesse sentido vamos adicionar uma biblioteca, uma template engine chamada `handlebars` aqual vamos adicioanr com o seguinte código: `yarn add handlebars`.

Em seguida no módulo de `accounts` vamos criar o diretório `views/emails/` com o arquivo `forgotPassword.hbs` com a estrutura:

**`forgotPassword.hbs`**

```hbs
<style>
  .container{
    width: 800px;
    font-family: Arial, Helvetica, sans-serif;
    align-items: center;
    display: flex;
    flex-direction: column;
  }
  span{
    margin: 10px;
  }
</style>

<div class="container">
  <span>Oi, {{name}}</span>
  <br/>
  <span>Você solicitou alteração de senha.</span>
  <span>Para realizar  a troca, clique no link
    <a href={{link}}>{{link}}</a>
  </span>

  <span>Caso não tenha sido você que solicitou a alteraçãode senha, basta ignorar o e-mail.</span>

  <strong>Obrigado!</strong>

  <h3>Equipe | <strong>Rentalx</strong></h3>
</div>
```

Para podermos receber esse template no nosso Provider vamos fazer algumas pequenas modificações.

**`IMailProvider.ts`:**

```ts
interface IMailProvider {
  sendMail(
    to: string,
    subject: string,
    path: string,
    variables: any
  ): Promise<void>;
}
export { IMailProvider };
```
E para implementar:

**`EtherealMailProvider.ts`:**

```ts
import fs from "fs";
import handlebars from "handlebars";
import nodemailer, { Transporter } from "nodemailer";
import { injectable } from "tsyringe";

import { IMailProvider } from "../IMailProvider";

@injectable()
class EtherealMailProvider implements IMailProvider {
  private client: Transporter;
  constructor() {
    nodemailer
      .createTestAccount()
      .then((account) => {
        const transporter = nodemailer.createTransport({
          host: account.smtp.host,
          port: account.smtp.port,
          secure: account.smtp.secure,
          auth: {
            user: account.user,
            pass: account.pass,
          },
        });

        this.client = transporter;
      })
      .catch((err) => console.error(err));
  }
  async sendMail(
    to: string,
    subject: string,
    path: string,
    variables: any
  ): Promise<void> {
    const templateFileContent = fs.readFileSync(path).toString("utf-8");

    const templateParse = handlebars.compile(templateFileContent);

    const templateHTML = templateParse(variables);

    const message = await this.client.sendMail({
      to,
      from: "Rentalx <noreplay@rentalx.com.br>",
      subject,
      html: templateHTML,
    });

    console.log("Message sent: %s", message.messageId);
    // Preview only available when sending through an Ethereal account
    console.log("Preview URL: %s", nodemailer.getTestMessageUrl(message));
  }
}
export { EtherealMailProvider };
```

Uzando o Mailprovider no useCase:

**`SendForGotPasswordMailUseCase.ts`:**

```ts
import { resolve } from "path";
// resto dos imports
@injectable()
class SendForGotPasswordMailUseCase {
  constructor(
    @inject("UsersRepository")
    private usersRepository: IUsersRepository,
    @inject("UsersTokensRepository")
    private usersTokensRepository: IUsersTokensRepository,
    @inject("DayjsDateProvider")
    private dateProvider: DayjsDateProvider,
    @inject("EtherealMailProvider")
    private mailProvider: IMailProvider
  ) {}
  async execute(email: string): Promise<void> {
    const user = await this.usersRepository.findByEmail(email);
    // path do template
    const templatePath = resolve(
      __dirname,
      "..",
      "..",
      "views",
      "emails",
      "forgotPassword.hbs"
    );

    if (!user) {
      throw new AppError("User does not exists");
    }

    const token = uuidv4();

    const expires_date = this.dateProvider.addHours(3);

    await this.usersTokensRepository.create({
      refresh_token: token,
      user_id: user.id,
      expires_date,
    });
    // variáveis que serão passadas para o template do handlebars
    const variables = {
      name: user.name,
      // link pro reset
      // variável de ambiente
      link: `${process.env.FORGOT_MAIL_URL}${token}`,
    };

    await this.mailProvider.sendMail(
      email,
      "Recupereação de Senha",
      templatePath,
      variables
    );
  }
}
export { SendForGotPasswordMailUseCase };
```

Agora vamos finalizar criando o arquivo `.env` na raiz do projeto com a variável de ambiente que acabamos de passar para o link do reset.

```
FORGOT_MAIL_URL=http://localhost:3333/password/reset?token=
```


## Aula CXXXIX
> Caso de uso de reset de senha

Agora nosso obejtivo é pegar esse link e recuperar a senha do usuário, Para tal ação, iremos criar mais um useCase no módulo de `accounts/` que iremos chamar de `resetPasswordUser/` com os repectivos arquivos de `UseCase` e `Controller`.

**`ResetPasswordUserUseCase`:**

```ts
interface IRequest {
  token: string;
  password: string;
}

@injectable()
class ResetPasswordUserUseCase {
  constructor(
    @inject("UsersTokensRepository")
    private usersTokensRepository: IUsersTokensRepository,
    @inject("DayjsDateProvider")
    private dateprovider: IDateProvider,
    @inject("UsersRepository")
    private usersRepository: IUsersRepository
  ) {}
  async execute({ password, token }: IRequest): Promise<void> {
    // busca UserToken oelo token
    const userToken = await this.usersTokensRepository.findByRefreshToken(
      token
    );
    // verifica se existe um token
    if (!userToken) {
      throw new AppError("Token invalid!");
    }
    // verifica se o token foi expirado
    if (
      this.dateprovider.compareIfBefore(
        userToken.expires_date,
        this.dateprovider.dateNow()
      )
    ) {
      throw new AppError("Token expired!");
    }
    // busca o usuário daquele token
    const user = await this.usersRepository.findById(userToken.user_id);
    // reescreve a senha
    user.password = await hash(password, 8);
    // Salva senha criada
    await this.usersRepository.create(user);
    // deleta token criado anteriormente
    await this.usersTokensRepository.deleteById(userToken.id);
  }
}
```
Como vimos no useCase acima, nem todos métodos em `UsersTokensRepository` `DayjsDateProvider` usados alí estão criado, nesse caso vamos criá-los agora.

**`IUsersTokensRepository.ts`:**

```ts
interface IUsersTokensRepository {
  // Restante do código
  findByRefreshToken(refresh_token: string): Promise<UserTokens>;
}
```

**`UsersTokensRepository.ts`:**

```ts
class UsersTokensRepository implements IUsersTokensRepository {

  // Resto do código
  async findByRefreshToken(refresh_token: string): Promise<UserTokens> {
    const userToken = await this.repository.findOne({ refresh_token });
    return userToken;
  }
}
```

**`IDateProvider.ts`:**

```ts
interface IDateProvider {
  // Resto do código
  compareIfBefore(start_date: Date, end_date: Date): boolean;
}
```

**`DayjsDateProvider.ts`:**

```ts
class DayjsDateProvider implements IDateProvider {
  // resto do código
  compareIfBefore(start_date: Date, end_date: Date): boolean {
    return dayjs(start_date).isBefore(end_date);
  }
}
```

Com os módulos criados, podemos então dar continuidade com nosso controller.

**`ResetPasswordUserController`:**

```ts
class ResetPasswordUserController {
  async handle(request: Request, response: Response): Promise<Response> {
    const { token } = request.query;
    const { password } = request.body;

    const resetPasswordUserUseCase = container.resolve(
      ResetPasswordUserUseCase
    );
    // garantimos o formato do token em string pois é esse tipo que o método execute() espera
    resetPasswordUserUseCase.execute({ token: String(token), password });

    return response.send();
  }
}
```
Para finalizar vamos criar rapídamente a rota da seguinte maneira.
**`password.routes.ts`:**

```ts
// Resto do código
const resetPasswordUserController = new ResetPasswordUserController();
passwordRoutes.post("/reset", resetPasswordUserController.handle);
```

Daí então, com o link enviado por email a partir da rota `/forgot` podemos enviar nosso novo `password` e estará completo nosso objetivo.


## Aula CXL
> Refatorando testes

Após refatorar essa parte de autentificação e criar na nossa APi a funcionalidade de recuperação de senha nossos testes se formos rodar, veremos que eles tabém vão requerer algumas alterações, que basicamente são:
- Criação do `UsersTokensRepositoryInMemory`;


**`UsersTokensRepositoryInMemory.ts`:**

```ts
class UsersTokensRepositoryInMemory implements IUsersTokensRepository {
  usersTokens: UserTokens[] = [];
  async create({
    expires_date,
    refresh_token,
    user_id,
  }: ICreateUserTokenDTO): Promise<UserTokens> {
    const userToken = new UserTokens();

    Object.assign(userToken, {
      expires_date,
      refresh_token,
      user_id,
    });

    this.usersTokens.push(userToken);

    return userToken;
  }
  async findByUserIdAndRefreshToken(
    user_id: string,
    refresh_token: string
  ): Promise<UserTokens> {
    const userToken = this.usersTokens.find(
      (ut) => ut.id === user_id && ut.refresh_token === refresh_token
    );
    return userToken;
  }
  async deleteById(id: string): Promise<void> {
    const userToken = this.usersTokens.find((ut) => ut.id === id);
    this.usersTokens.splice(this.usersTokens.indexOf(userToken));
  }
  async findByRefreshToken(refresh_token: string): Promise<UserTokens> {
    const userToken = this.usersTokens.find(
      (ut) => ut.refresh_token === refresh_token
    );

    return userToken;
  }
}
```
- Instanciamento do `UsersTokensRepositoryInMemory`, `DayjsDateProvider` no test de `AuthenticateUserUseCase`;

**`AuthenticateUserUseCase.spec.ts`:**

```ts
let authenticateUserUseCase: AuthenticateUserUseCase;
let usersRepositoryInMemory: UsersRepositoryInMemory;
let usersTokensRepositoryInMemory: UsersTokensRepositoryInMemory;
let dateProvider: DayjsDateProvider;

let createUserUseCase: CreateUserUseCase;
describe("Authenticate User", () => {
  beforeEach(() => {
    usersRepositoryInMemory = new UsersRepositoryInMemory();
    usersTokensRepositoryInMemory = new UsersTokensRepositoryInMemory();
    dateProvider = new DayjsDateProvider();
    authenticateUserUseCase = new AuthenticateUserUseCase(
      usersRepositoryInMemory,
      usersTokensRepositoryInMemory,
      dateProvider
    );
    createUserUseCase = new CreateUserUseCase(usersRepositoryInMemory);
  });
  // Rest do código
});

```
- Mudar os parâmetros de `token` para `refres_toke` nos testes de `CreateCategoryController` e `ListCategoriesController`, que não é mais o **token** responssável pela autentificaçãoe sim o **refresh_token**.


## Aula CXLI
> Testando envio de e-mail

Vamos agora criar o teste de envio de email. Para isso vamos criar o arquivo `SendForGotPasswordMailUseCase.spec.ts` na pasta juntamente com o seu caso de uso, mas antes de executarmos nosso teste, precisamos criar o ProviderInMemory no MailProvider. Com essa intenção, na pasta de `providers/MailProvider` vamos criar o diretório `in-memory` com o arquivo **`MailProviderInMemory.ts`**, com a seguinte estrutura:

```ts
class MailProviderInMemory implements IMailProvider {
  private message: any[] = [];
  async sendMail(
    to: string,
    subject: string,
    path: string,
    variables: any
  ): Promise<void> {
    this.message.push({
      to,
      subject,
      path,
      variables,
    });
  }
}
```

E no teste:

`SendForGotPasswordMailUseCase.spec.ts`

```ts
let sendForGotPasswordMailUseCase: SendForGotPasswordMailUseCase;
let usersRepositoryInMemory: UsersRepositoryInMemory;
let dateProvider: DayjsDateProvider;
let usersTokensRepositoryInMemory: UsersTokensRepositoryInMemory;
let mailProvider: MailProviderInMemory;

describe("Send Forgot Mail", () => {
  beforeEach(() => {
    usersRepositoryInMemory = new UsersRepositoryInMemory();
    usersTokensRepositoryInMemory = new UsersTokensRepositoryInMemory();
    dateProvider = new DayjsDateProvider();
    mailProvider = new MailProviderInMemory();

    sendForGotPasswordMailUseCase = new SendForGotPasswordMailUseCase(
      usersRepositoryInMemory,
      usersTokensRepositoryInMemory,
      dateProvider,
      mailProvider
    );
  });

  it("should be able to send a forgot password mail to user", async () => {
    // observa em mailProvider o método sendMail
    const sendMail = jest.spyOn(mailProvider, "sendMail");
    // cria usuário
    await usersRepositoryInMemory.create({
      driver_license: "189723",
      email: "user@rentalx.com",
      name: "User",
      password: "123",
    });
    // executa useCase
    await sendForGotPasswordMailUseCase.execute("user@rentalx.com");
    // espera que sendMail seja chamado
    expect(sendMail).toHaveBeenCalled();
  });

  it("should not be able to send an email if user does not exists", async () => {
    // espera que seja rejetado já que não foi cadastrado usuário com esse email
    await expect(
      sendForGotPasswordMailUseCase.execute("aleatoryEmail@rentalx.com")
    ).rejects.toEqual(new AppError("User does not exists"));
  });

  it("should be able to create an users token", async () => {
    // observa se foi chamado o create da classe usersTokensRepositoryInMemory
    const generateTokenMail = jest.spyOn(
      usersTokensRepositoryInMemory,
      "create"
    );

    await usersRepositoryInMemory.create({
      driver_license: "189723",
      email: "otherUser@rentalx.com",
      name: "User",
      password: "123",
    });

    await sendForGotPasswordMailUseCase.execute("otherUser@rentalx.com");
    // espera que o create de usersTokensRepositoryInMemory tenha sido chamado
    expect(generateTokenMail).toBeCalled();
  });
});
```

## Aula CXLII
> Coverage Report

Vamos configurar o jest para ele nos reportar a cobertura de nossos testes, oq foi testado ou não em toda nossa aplicação. Para isso, no `jest.config.ts` vamos modificar as seguintes propriedades:

```ts
export default{
  collectCoverage: true,

  collectCoverageFrom: ["<rootDir>/src/modules/**/useCases/**/*.ts"],

  coverageDirectory: "coverage",

  coverageProvider: "v8",

  coverageReporters: ["text-summary", "lcov"],
}
```

## Aula CXLIV
> Corrigindo o refresh token

Aqui vamos corrigir o refresh_token para que o token cumpra com a finalidade que foi concebido.

- **Refresh_Token:** vai atualizar o token 
- **Token:** Vai autentificar o usuário

`RefreshTokenUseCase.ts`

```ts
interface IPayload {
  sub: string;
  email: string;
}

interface ITokenResponse {
  token: string;
  refresh_token: string;
}

@injectable()
class RefreshTokenUseCase {
  constructor(
    @inject("UsersTokensRepository")
    private usersTokensRepository: IUsersTokensRepository,
    @inject("DayjsDateProvider")
    private dateProvider: IDateProvider
  ) {}

  async execute(token: string): Promise<ITokenResponse> {
    const { email, sub } = verify(token, auth.secret_refresh_token) as IPayload;

    const user_id = sub;

    const userToken =
      await this.usersTokensRepository.findByUserIdAndRefreshToken(
        user_id,
        token
      );

    if (!userToken) {
      throw new AppError("Refresh Token does not exists!");
    }

    await this.usersTokensRepository.deleteById(userToken.id);

    const refresh_token = sign({ email }, auth.secret_refresh_token, {
      subject: sub,
      expiresIn: auth.expires_in_refresh_token,
    });

    const expires_date = this.dateProvider.addDays(
      auth.expires_refresh_token_days
    );

    await this.usersTokensRepository.create({
      expires_date,
      refresh_token,
      user_id,
    });

    const newToken = sign({}, auth.secret_token, {
      subject: user_id,
      expiresIn: auth.expires_in_token,
    });

    return {
      refresh_token,
      token: newToken,
    };
  }
}
```

`ensureAuthenticated.ts`

```ts
interface IPayload {
  sub: string;
}

export async function ensureAuthenticated(
  request: Request,
  response: Response,
  next: NextFunction
): Promise<void> {
  const authHeader = request.headers.authorization;

  if (!authHeader) {
    throw new AppError("Token missing", 401);
  }

  const [, token] = authHeader.split(" ");

  try {
    const { sub: user_id } = verify(token, auth.secret_token) as IPayload;

    request.user = {
      id: user_id,
    };

    next();
  } catch (error) {
    throw new AppError("Invalid token", 401);
  }
}
```

## Aula CXLV
> Criando conta na AWS

Vamos  precisar de uma conta na aws para podermos dar continuidade com a nossa API, fazendo o armazenamento dela no storage da aws.

Storage - São armarzenamentos específicos dentro da cloud para armazenamento de arquivos. O que será usado nesse projeto será o da amazon, **S3**.

## Aula CXLVI
> Criação do usuário e S3

Agora nosso objetivo é criar um bucket, que seria algo parecido com um diretório onde será armazenado nossos arquivos, mas antes, vamos também criar um usuário, um **IAM**. Para isso:

- Vamos buscar nos services da aws, o `IAM - Manage access to AWS resources`
- Buscar `Usuários` na seção do lado esquerdo e adicionar e clicar no botão de `Adicionar usuário`
- Preencher `Nome de usuário` (qualquer nome)
- Selecionar tipo de acesso: programático
- Em Definir permissões, selecionar, `Anexar políticas existentes de forma direta` e nela marcar a permissão, AmazonS3FullAccess
- Adicionar tags é opicional
- Após revisar as escolhas é possível criar usuário
- Copiar `chave de acesso secreta` e `ID da chave de Acesso`

Com usuário finalizado vamos agora criar nosso bucket.

- Nos serviços da aws vamos buscar por S3 - Scalable Storage in the Cloud
- Clicar em `Criar bucket`
- Criar nome único parao bucket
- Escolher região
- Desabilitar  a opção `Bloquear todo o acesso público`
- Reconhecer as configurações do bloqueio
- *Versionamento* e *Criptografia* desativadas
- Clicar no botão de `Criar bucket`

## Aula CXLVII
> Provider de Upload

Aqui vamos coeçar a configurar nossa aplicação apra fazer o upload no bucket criado. Nesse sentido, vamos iniciar instalando a dependência que será responssável pelo comicação com o bucket da aws: `yarn add aws-sdk`. Além disso, vamos passar agora as chaves do bucket no arquivo `.env` em variáveis como indiva a documentação da aws.
`.env`

```
FORGOT_MAIL_URL=http://localhost:3333/password/reset?token=

# AWS Credentials
AWS_ACCESS_KEY_ID=***********************
AWS_SECRET_ACCESS_KEY=*****************************************
AWS_BUCKET=api-rentalx-s3
```

Afim de deixar o código mais modular podendo trocar a lib/serviço responssável pelo upload além de facilitar nossos testes, vamos criar um provider para o storage. Então no diretório de `providers/`, vamos criar `StorageProvider/` com a interface `IStorageProvider.ts` e a pasta `implementations/` onde, por sua vez,terá o `LocalStorageProvider.ts`, com as seguintes estruturas:

`IStorageProvider.ts`

```ts
interface IStorageProvider {
  // recebe o nome do arquivo e a pasta que será salvo
  save(file: string, folder: string): Promise<string>;
  delete(file: string, folder: string): Promise<void>;
}
```

Antes da implementação do nosso LocalStorage vamos fazer algumas modificações no arquivo `upload.ts` onde utilizamos o multer. para podermos utilizar já que vamos precisar tanto localmente quanto no nosso **S3** da AWS.

`upload.ts`

```ts
const tmpFolder = resolve(__dirname, "..", "..", "tmp");

export default {
  tmpFolder,
  storage: multer.diskStorage({
    destination: tmpFolder,
    filename: (request, file, callback) => {
      const fileHash = crypto.randomBytes(16).toString("hex");
      const fileName = `${fileHash}- ${file.originalname}`;

      return callback(null, fileName);
    },
  }),
};
```

`LocalStorageProvider.ts`

```ts
class LocalStorageProvider implements IStorageProvider {
  async save(file: string, folder: string): Promise<string> {
    // move o arquivo
    await fs.promises.rename(
      // daqui
      resolve(upload.tmpFolder, file),
      // para aqui
      resolve(`${upload.tmpFolder}/${folder}`, file)
    );
    // retorna o nome do arquivo
    return file;
  }
  async delete(file: string, folder: string): Promise<void> {
    // pega o caminho
    const filename = resolve(`${upload.tmpFolder}/${folder}`, file);

    try {
      await fs.promises.stat(filename);
    } catch {
      return;
    }
    // deleta o arquivo
    await fs.promises.unlink(filename);
  }
}
```
Finalizado essa parte vamos usar nosso StorageProvider no `UpdateUserAvatarUseCase.ts`:

```ts
interface IRequest {
  user_id: string;
  avatar_file: string;
}

@injectable()
class UpdateUserAvatarUseCase {
  constructor(
    // implementação dos containers
    @inject("UsersRepository")
    private usersRepository: IUsersRepository,
    @inject("StorageProvider")
    private storageProvider: IStorageProvider
  ) {}

  async execute({ user_id, avatar_file }: IRequest): Promise<void> {
    const user = await this.usersRepository.findById(user_id);

    if (user.avatar) {
      await this.storageProvider.delete(user.avatar, "avatar");
    }
    // salvando arquivo na pasta avatar
    await this.storageProvider.save(avatar_file, "avatar");

    user.avatar = avatar_file;

    await this.usersRepository.create(user);
  }
}
```
Antes de passarmos de finalizarmos com o container do StorageProvider,  vamos alterar um detalhe nas rotas onde usamos o `upload.ts`.

`cars.routes.ts`

```ts
const upload = multer(uploadConfig);
```

`users.routes.ts`

```ts
const uploadAvatar = multer(uploadConfig);
```

E finalmente em `providers/`:

`index.ts`

```ts
container.registerSingleton<IStorageProvider>(
  "StorageProvider",
  LocalStorageProvider
);
```

## Aula CXLVIII
> Upload utilizando S3

Aqui vamos implementr o S3 no StorageProvider:

``

```ts
import { S3 } from "aws-sdk";
import fs from "fs";
import mime from "mime";
import { resolve } from "path";
import upload from "@config/upload";
import { IStorageProvider } from "../IStorageProvider";

class S3StorageProvider implements IStorageProvider {
  private client: S3;

  constructor() {
    this.client = new S3({
      region: process.env.AWS_BUCKET_REGION,
    });
  }
  async save(file: string, folder: string): Promise<string> {
    const originalName = resolve(upload.tmpFolder, file);

    const fileContent = await fs.promises.readFile(originalName);
    // tipagem do arquivo
    const ContentType = mime.getType(originalName);

    await this.client
      .putObject({
        // pasta do no bucket
        Bucket: `${process.env.AWS_BUCKET}/${folder}`,
        Key: file,
        // torna público para leitura
        ACL: "public-read",
        Body: fileContent,
        ContentType,
      })
      .promise();
    await fs.promises.unlink(originalName);

    return file;
  }
  async delete(file: string, folder: string): Promise<void> {
    await this.client
      .deleteObject({
        // diretório
        Bucket: `${process.env.AWS_BUCKET}/${folder}`,
        // arquivo do diretório
        Key: file,
      })
      .promise();
  }
}
```

S3StorageProvider finalizado vamos mudar o provider que será instanciado no useCase ou o local, a dependender da variável de ambiente `disk=` que passarmos.

`providers/index.ts`

```ts
const diskStorage = {
  local: LocalStorageProvider,
  s3: S3StorageProvider,
};

container.registerSingleton<IStorageProvider>(
  "StorageProvider",
  diskStorage[process.env.disk]
);
```

## Aula CXLIX
> Criando URL de acesso do avatar

Antes de tratar a urla do nosso avatar, vamos corrigir o upload de carros adicionando o storage provider a ele.

`UploadCarImagesUseCase.ts`

```ts
interface IRequest {
  car_id: string;
  images_name: string[];
}
@injectable()
class UploadCarImagesUseCase {
  constructor(
    @inject("CarsImagesRepository")
    private carsImagesRepository: ICarsImagesRepository,
    // injetando provider
    @inject("StorageProvider")
    private storageProvider: IStorageProvider
  ) {}
  async execute({ car_id, images_name }: IRequest): Promise<void> {
    images_name.map(async (image) => {
      await this.carsImagesRepository.create(car_id, image);
      // salvando no storage, local ou remota a depender da variável de ambiente
      await this.storageProvider.save(image, "cars");
    });
  }
}
```

Agora vamos criar uma forma do usuário ver usas informações e para isso vamos criar mais um useCase em `accounts` com o diretório `profileUser/` e os arquivo de usecase e Controller, com a seguinte estrutura:

`ProfileUserUseCase.ts`

```ts
@injectable()
class ProfileUserUseCase {
  constructor(
    @inject("UsersRepository")
    private usersRepository: IUsersRepository
  ) {}

  async execute(id: string): Promise<IUserResponseDTO> {
    const user = await this.usersRepository.findById(id);
    // para que possamos retornar ao usuário os dados de uma melhor maneira utilizamos  o mapper que iremmos ver a seguir
    return UserMap.toDTO(user);
  }
}
```

**Mapper**

`User.ts`

```ts
@Entity("users")
class User {
  // Resto do código

  // com o Expose do class-transformer vamos usar acima do método em questão e usando  o name que será usado na aplicação dentro do @Expose({})
  @Expose({ name: "avatar_url" })
  avatar_url(): string {
    switch (process.env.disk) {
      case "local":
        return `${process.env.APP_API_URL}/avatar/${this.avatar}`;
      case "s3":
        return `${process.env.AWS_BUCKET_URL}/avatar/${this.avatar}`;
      default:
        return null;
    }
  }

  constructor() {
    // ...
  }
}
```

`IUserResponseDTO`

```ts
interface IUserResponseDTO {
  email: string;
  name: string;
  id: string;
  avatar: string;
  driver_license: string;
  // indicamos que o avatar_url é uma função que retorna a string
  avatar_url(): string;
}
```

`UserMap`

```ts
class UserMap {
  static toDTO({
    email,
    name,
    id,
    avatar,
    driver_license,
    avatar_url,
  }: User): IUserResponseDTO {
    // método da lib class-transformer que será responssável por capturar o avatar_url na nossa entidade
    const user = classToClass({
      email,
      name,
      id,
      avatar,
      driver_license,
      // para pegar o avatar_url, precisamos utilizar um biblioteca que cria na nossa entidade uma nova propriedade, o class-transformer diretamente na entidade criando uma função que retorna um determinado valor
      avatar_url,
    });
    return user;
  }
}
```
Asssim, passando as informações do usuário devidamente tratadas.

`ProfileUserControler.ts`

```ts
class ProfileUserControler {
  async handle(request: Request, response: Response): Promise<Response> {
    const { id } = request.user;
    const profileUserUseCase = container.resolve(ProfileUserUseCase);

    const user = await profileUserUseCase.execute(id);
    return response.json(user);
  }
}
```
Rotas:

`users.routes.ts`

```ts
// ...
const profileUserControler = new ProfileUserControler();
usersRoutes.get("/profile", ensureAuthenticated, profileUserControler.handle);
// ...
```

Configuração para buscar os arquivos localmente.

`app.ts`

```ts
// ...
app.use("/avatar", express.static(`${upload.tmpFolder}/avatar`));
app.use("/cars", express.static(`${upload.tmpFolder}/cars`));
// ...
```

## Aula CXLX
> Configurando o e-mail em produção

- Obter Domínio
- Obter email
- Validar email e domínio

<h4 align="center"> 
	🚧 🚀 Em construção... 🚧
</h4>
