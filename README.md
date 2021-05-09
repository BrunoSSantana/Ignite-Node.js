<img src="https://res.cloudinary.com/practicaldev/image/fetch/s--nTfuVZvi--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/4qa1g2dsx1hre7hjjlze.png">

# Ignite Desafio 01 trilha node.js

<p align="center">
<img src="https://img.shields.io/github/license/BrunoSSantana/desafio02-trilha-node.js" />
<img src="https://img.shields.io/github/last-commit/BrunoSSantana/desafio02-trilha-node.js">
</p>

---

* [Chapter I](#chapter-i)
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
* [Chapter II](#chapter-ii)
  * [Aula XXI](#aula-xxi)

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


## Aula XXVII
> Criando saque na conta

## Aula XVIII
> Listar extrato bancário por data

## Aula XIX
> Atualizar conta

## Aula XX
> Remover conta

## CHAPTER II

## Aula XXI
