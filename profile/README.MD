# Ecossistema de Gestão Centralizada

Este repositório unifica a visão geral da nossa organização, consolidando o desenvolvimento de uma aplicação completa dividida entre uma API robusta de backend e uma interface single-page application (SPA) de frontend. Os projetos foram criados para gerenciar o fluxo operacional de clientes, colaboradores e agendamentos.

---

## 🏗️ Repositórios do Ecossistema

A arquitetura da solução está dividida em dois pilares principais que se integram via chamadas HTTP seguras:

### 1. Backend (`projeto_es_backend`)
Desenvolvido em Python com o ecossistema Django, esta camada gerencia a persistência dos dados relacionais, as regras de negócio e o controle de acessos da aplicação.
* **Frameworks:** Django 5.2 e Django REST Framework 3.16.
* **Segurança:** Autenticação baseada em tokens JWT (`djangorestframework-simplejwt`).
* **Documentação:** Mapeamento automático da API seguindo o padrão OpenAPI 3.0 via `drf-spectacular`.
* **Modelagem Corrente:** Entidades isoladas para `Client` (informações de contato de clientes) e `Employee` (dados profissionais e cargo/role da equipe interna).

### 2. Frontend (`projeto_es_frontend`)
Interface rica criada em Vue.js para garantir que o usuário final tenha uma navegação fluida, rápida e tipada.
* **Core:** Vue 3 rodando sobre o Vite como ferramenta de build ultra-rápida.
* **Linguagem:** TypeScript configurado de forma estrita para evitar quebras em tempo de execução.
* **Roteamento e Consumo:** Controle de histórico de navegação com `vue-router` e comunicação assíncrona com o Django feita pelo `axios`.
* **Componentes Construídos:** Telas e modais isolados para `ClientCRUD`, `FuncionarioCRUD` e gerenciamento dinâmico de `Agendamento`.

