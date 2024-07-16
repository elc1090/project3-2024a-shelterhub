# Projeto: ShelterHub

![WhatsApp Image 2024-06-17 at 23 09 39](https://github.com/elc1090/project3-2024a-shelterhub/assets/20145947/b36a9b75-4dfd-4bc6-9556-7cdc843147f7)


Acesso: https://shelterhub-front.vercel.app/home

API: shelterhub-api.koyeb.app/

Repositórios

Front-end: https://github.com/brucvei/shelterhub-front

Back-end: https://github.com/pizzutta/shelterhub-api

### Desenvolvedores

Bruna Caetano da Veiga e Vitória Regina Pizzutti Moraes | Sistemas de Informação

### Nosso produto

Recentemente, fortes chuvas causaram severas enchentes no Rio Grande do Sul, resultando em danos materiais significativos e deixando muitas famílias desabrigadas. A situação emergencial evidenciou a necessidade de sistemas eficientes para gerenciar recursos e prestar suporte às vítimas de forma organizada.

Em resposta, foi criado o ShelterHub, um sistema web inovador para simplificar o controle de estoque dos abrigos. Ele permite uma gestão precisa dos recursos disponíveis e oferece estimativas de necessidades, garantindo que cada abrigo possa atender às demandas de maneira eficaz.

#### Funcionalidades

As funcionalidades básicas do ShelterHub incluem cadastrar, editar, excluir e visualizar Abrigos, Itens, Categorias, e Unidades de medida.

No Abrigo, é possível adicionar os itens que estão em seu estoque e efetuar transações de Entrada e Saída destes itens.

#### API

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

#### Tecnologias

- Java
- Spring Boot
- Hibernate
- PostgreSQL
- Angular
- Angular Material
- Bootstrap

#### Ambiente de desenvolvimento

- IntelliJ IDEA
- WebStorm

---
Projeto entregue para a disciplina de [Desenvolvimento de Software para a Web](http://github.com/andreainfufsm/elc1090-2024a) em 2024a
