<img src="https://res.cloudinary.com/practicaldev/image/fetch/s--nTfuVZvi--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/4qa1g2dsx1hre7hjjlze.png">

# Ignite Desafio 01 trilha node.js

<p align="center">
<img src="https://img.shields.io/github/license/BrunoSSantana/desafio02-trilha-node.js" />
<img src="https://img.shields.io/github/last-commit/BrunoSSantana/desafio02-trilha-node.js" />
</p>

---

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

 - [Desafio: Conceitos do Node.js](https://github.com/BrunoSSantana/desafio01-trilha-node.js/)
 - [Desafio: Trabalhando com Middlewares](https://github.com/BrunoSSantana/desafio02-trilha-node.js/)
 - [Desafio: Corrigindo o código](https://github.com/BrunoSSantana/desafio03-trilha-node.js/)
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

![](https://xesque.rocketseat.dev/1571029149847-attachment.png)

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
> Inserindo tipagem para categoria

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
> criando um Repositório de Categoria

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













