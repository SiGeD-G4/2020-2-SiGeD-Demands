# API de Demandas
[![License: GPL-3.0](https://img.shields.io/badge/License-GPL3-blue.svg)](https://opensource.org/licenses/gpl-3.0.html)
[![codecov](https://codecov.io/gh/fga-eps-mds/2020-2-SiGeD-Demands/branch/master/graph/badge.svg?token=I08UG1R8HC)](https://codecov.io/gh/fga-eps-mds/2020-2-SiGeD-Demands)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=fga-eps-mds_2020-2-G4-Demands&metric=alert_status)](https://sonarcloud.io/dashboard?id=fga-eps-mds_2020-2-G4-Demands)
[![Maintainability](https://api.codeclimate.com/v1/badges/9e950d2214a735d2ba4b/maintainability)](https://codeclimate.com/github/fga-eps-mds/2020-2-SiGeD-Demands/maintainability)

Essa API faz parte da arquitetura de microsserviços do projeto [`SiGeD`](https://github.com/fga-eps-mds/2020-2-SiGeD), sua funcionalidade é possibilitar o controle dos dados das demandas. 

## Como contribuir?

Gostaria de contribuir com nosso projeto? Acesse o nosso [guia de contribuição](https://fga-eps-mds.github.io/2020-2-SiGeD/CONTRIBUTING/) onde são explicados todos os passos.
Caso reste duvidas você também pode entrar em contato conosco criando uma issue.

## Documentação

A documentação do projeto pode ser acessada pelo nosso site em https://fga-eps-mds.github.io/2020-2-SiGeD/ ou você pode acessar pela [SiGeD Documentação](https://fga-eps-mds.github.io/2020-2-SiGeD/home/)

## Como rodar?

Para rodar a API é preciso usar os seguintes comandos usando o docker:

Crie uma network para os containers da API, caso não exista:

```bash
docker network create siged_backend
```

Suba o container com o comando:

```bash
docker-compose up
```
A API estará rodando na [porta 3003](http://localhost:3003).

## Rotas

**GET: `/category/`**

Para receber os dados de todas as categorias listadas.

**GET: `/category/:id`**

Para receber os dados de uma categoria específica utilizando o `id`.

**POST: `/category/create`**

Para criar uma nova categorias, envie os dados nesse formato:

```json
{
    "name": "Nome da categoria",
    "description": "Descrição da categoria",
    "color": "#000000"
}
```

**PUT: `/category/update/:id`**

Para atualizar os dados de uma categoria, envie os dados atualizados seguindo o padrão:

```json
{
    "name": "Nome da categoria",
    "description": "Descrição da categoria",
    "color": "#000000"
}
```

**DELETE: `/category/delete/:id`**

Para deletar uma categoria pelo `id`.
