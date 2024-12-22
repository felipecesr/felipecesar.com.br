---
layout: default
title: Entrega Contínua no NPM com Github Actions
tags:
  - github
  - ci
  - npm
  - monorepo
  - javascript
date: 2024-10-25T12:08:00.000Z
---
Fala pessoal, tudo certo?

Neste post, vou mostrar na prática como criar uma Entrega Contínua de pacotes de um monorepo no NPM.

## Criando um token no NPM

Primeiro você precisa ter uma conta no NPM e criar um token para automatizações.

## Permissões do repositório

É necessário dar permissões de leitura e escrita para que os commits dos releases sejam feitos.

Para habilitar isso vá em Settings -> Actions -> General -> Workflow permissions e verifique se "Read and write permissions" estão habilitadas.

## Criando a Action
