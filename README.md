<h3 align="center">
  Desafio 09: GoRestaurant Web
</h3>

## :rocket: Sobre o desafio

Nesse desafio foi desenvolvida mais uma aplicação, a GoRestaurant. Nela foram praticados os conceitos aprendidos sobre React.js junto com TypeScript, e também o conceito de CRUD (Create, Read, Update, Delete).

Essa é uma aplicação que se conecta a uma fake API e exibe os pratos de comida criados. Também permite a criação, remoção e atualização desses pratos.

## Utilizando a fake API

Para que se tenha os dados para exibir em tela, existe um arquivo na raiz do projeto que é utilizado como uma fake API para prover esses dados. Esses dados podem ser encontrados no arquivo ```server.json```.

Para isso foi utilizada uma dependência chamada ```json-server``` que faz uso do arquivo ```server.json```, e provê os dados através de uma rota ```/foods``` simulando o comportamento de uma API real. Para executar esse servidor é necessário executar o seguinte comando:

```bash
yarn json-server server.json -p 3333
```

## Instalação

Para instalar o projeto localmente na sua máquina basta clonar o repositório:

```bash
git clone https://github.com/gpmarchi/gostack-nova-jornada-desafio-09.git && cd gostack-nova-jornada-desafio-09
```

E rodar o comando abaixo para instalar as dependências necessárias:

```bash
yarn
```

## Funcionalidades da aplicação

Abaixo estão as funcionalidades principais da aplicação:

- **`Listar os pratos de comida da sua API`**: A página ```Dashboard``` exibe uma listagem com os campos ```title```, ```value```, ```description``` e ```available``` de todos os pratos de comida que estão cadastrados na API.

- **`Adicionar novos pratos de comida a sua API`**: Na página ```Dashboard``` é exibido um modal ao clicar no botão ```Novo Prato``` no ```Header```. Esse modal é responsável por cadastrar uma nova ```food``` dentro da API passando os campos ```image```, ```name```, ```description```, ```value```.

- **`Editar pratos de comida da sua API`**: Na página ```Dashboard``` é exibido um modal ao clicar no botão ```Editar Prato```. Esse modal é responsável por editar uma ```food``` dentro da API passando os campos ```image```, ```name```, ```description```, ```value```.

- **`Remover pratos de comida da sua API`**: Na página ```Dashboard``` é removido um prato de comida ao clicar no botão com ícone de lixeira no componente ```Food```.

- **`Alterar disponibilidade dos pratos de comida da sua API`**: Na página ```Dashboard``` é alterada a disponibilidade de um prato de comida ao clicar no switch que é controlado pelo valor de ```available```.

## Especificação dos testes

O desafio foi resolvido seguindo a técnica de TDD. Os testes podem ser encontrados na pasta ```src/__tests__``` e para executá-los rodar o comando:

```bash
yarn test
```

Para cada teste existe uma breve descrição do que a aplicação executa para que o mesmo passe:

- **`should be able to list all the food plates from your api`**: Para que esse teste passe, a aplicação permite que sejam listados todos os pratos de comida que são retornados da fake API.

- **`should be able to add a new food plate`**: Para que esse teste passe, é permitido que um prato de comida seja adicionado à api, adicionando-o também à listagem em tela.

- **`should be able to edit a food plate`**: Para que esse teste passe, você é permitido que um prato de comida seja atualizado na api, editando-o também na listagem em tela.

- **`should be able to remove a food plate`**: Para que esse teste passe, é permitido que um prato de comida seja removido da api, removendo-o também da listagem em tela.

- **`should be able to update the availibility of a food plate`**: Para que esse teste passe, na página ```Dashboard``` é permitido que o status do prato de comida seja alterado entre ```Disponível``` e ```Indisponível```.
