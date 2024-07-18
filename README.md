# Projeto: ShelterHub

![WhatsApp Image 2024-06-17 at 23 09 39](https://github.com/elc1090/project3-2024a-shelterhub/assets/20145947/b36a9b75-4dfd-4bc6-9556-7cdc843147f7)


Acesso: https://shelterhub-front.vercel.app/home

API: shelterhub-api.koyeb.app/

Repositórios

Front-end: https://github.com/brucvei/shelterhub-front

Back-end: https://github.com/pizzutta/shelterhub-api

## Desenvolvedores

Bruna Caetano da Veiga e Vitória Regina Pizzutti Moraes | Sistemas de Informação

## Nosso produto

Recentemente, fortes chuvas causaram severas enchentes no Rio Grande do Sul, resultando em danos materiais significativos e deixando muitas famílias desabrigadas. A situação emergencial evidenciou a necessidade de sistemas eficientes para gerenciar recursos e prestar suporte às vítimas de forma organizada.

Em resposta, foi criado o ShelterHub, um sistema web inovador para simplificar o controle de estoque dos abrigos. Ele permite uma gestão precisa dos recursos disponíveis e oferece estimativas de necessidades, garantindo que cada abrigo possa atender às demandas de maneira eficaz.

## Funcionalidades

As funcionalidades básicas do ShelterHub incluem cadastrar, editar, excluir e visualizar Abrigos, Itens, Categorias, e Unidades de medida.

No Abrigo, é possível adicionar os itens que estão em seu estoque e efetuar transações de Entrada e Saída destes itens.

## API

Há 5 entidades presentes na API:

- ``Shelter`` - Representação de um abrigo
- ``Category`` - Representação de uma categoria, relacionada ao ``Item``
- ``MeasurementUnit`` - Representação de uma unidade de medida, relacionada ao ``Item``
- ``Item`` - Representação de um item que pode ser recebido pelos abrigos
- ``ItemShelter`` - A relação entre o item e o abrigo, que compõe o estoque do abrigo
- ``Transaction`` - Representação de uma transação, que pode ser feita ao receber doações ou ao utilizar os itens que se encontravam no estoque

Para todas estas entidades, existem os endpoints descritos abaixo:

- ``GET /entidade`` - Retorna todos os registros existentes da entidade
- ``GET /entidade/{id}`` - Retorna o registro correspondente ao identificador enviado
- ``POST /entidade`` - Salva um novo registro na entidade
- ``PUT /entidade`` - Atualiza um registro existente na entidade
- ``DELETE /entidade/{id}`` - Remove o registro correspondente ao identificador enviado

Para as entidades ``ItemShelter`` e ``Transaction``, há também o seguinte endpoint:

- ``GET /entidade/shelter/{shelter_id}`` - Retorna todos os registros relacionados ao abrigo correspondente ao identificador enviado

## Tecnologias

- Java
- Spring Boot
- Hibernate
- PostgreSQL
- Angular
- Angular Material
- Bootstrap

## Ambiente de desenvolvimento

- IntelliJ IDEA
- WebStorm

## Casos de teste

### 1. Usuário Admin

#### 1.1. Cadastro

- Clique no botão **Cadastrar**
- Informe seus dados
- Clique no botão **Cadastrar** novamente

#### 1.2. Login

- Informe o CPF e Senha cadastrados anteriormente
- Clique no botão **Entrar**

A página inicial deve ser mostrada

#### 1.3. Página inicial

Você poderá visualizar:
- Abrigos cadastrados
- Relatórios
- Configuração de itens

#### 1.4. Abrigos

**Cadastro:**
- Clique no botão **Novo**
- Preencha as informações
- Clique no botão **Criar**

O novo abrigo deve aparecer na listagem

**Edição:**
- Clique no segundo botão azul do card do Abrigo
- Altere as informações desejadas
- Clique no botão **Editar**

O abrigo deve ser atualizado

**Remoção:**
- Clique no botão vermelho do card do Abrigo

O abrigo deve ser removido

**Visualização:**
- Clique no primeiro botão azul do card do Abrigo

Você poderá visualizar os Itens e as Transações do Abrigo

**Adicionar Item no Abrigo:**
- Ao visualizar um Abrigo, na aba **Itens**, clique no botão **Novo item**
- Preencha as informações
- Clique no botão **Criar**

O Item deverá aparecer na listagem

**Fazer uma Transação no Abrigo:**
- Ao visualizar um Abrigo, na aba **Transações**, clique no botão **Nova transação**
- Preencha as informações
- Clique no botão **Criar**

A Transação deverá aparecer na listagem e a quantidade deverá estar atualizada na aba **Itens**

#### 1.4. Relatórios

Após os passos anteriores, os relatórios deverão estar atualizados

##### 1.4. Configuração de itens

##### Itens

Ao clicar em **Itens**, uma tabela com os itens cadastrados será apresentada

**Cadastro:**
- Clique no botão **Novo**
- Preencha as informações
- Clique no botão **Criar**

O novo item deve aparecer na listagem

**Edição:**
- Clique no botão azul na linha do respectivo Item
- Altere as informações desejadas
- Clique no botão **Editar**

O item deve ser atualizado

**Remoção:**
- Clique no botão vermelho na linha do respectivo Item

O item deve ser removido

**Transferência entre Abrigos:**
- Clique no botão **Nova transferência**
- Preencha as informações
- Clique no botão **Transferir**

Ao visualizar os Abrigos envolvidos, a Transação deverá aparecer na listagem e a quantidade deverá estar atualizada na aba **Itens**

##### Categorias

Ao clicar em **Categorias**, uma tabela com as categorias cadastradas será apresentada

**Cadastro:**
- Clique no botão **Novo**
- Preencha o nome
- Clique no botão **Criar**

A nova categoria deve aparecer na listagem

**Edição:**
- Clique no botão azul na linha da respectiva Categoria
- Altere o nome
- Clique no botão **Editar**

A categoria deve ser atualizada

##### Unidades de medidas

Ao clicar em **Unidades de medidas**, uma tabela com as unidades de medidas cadastradas será apresentada

**Cadastro:**
- Clique no botão **Novo**
- Preencha o nome
- Clique no botão **Criar**

A nova unidade de medida deve aparecer na listagem

**Edição:**
- Clique no botão azul na linha da respectiva Unidade de medida
- Altere o nome
- Clique no botão **Editar**

A unidade de medida deve ser atualizada

---
Projeto entregue para a disciplina de [Desenvolvimento de Software para a Web](http://github.com/andreainfufsm/elc1090-2024a) em 2024a
