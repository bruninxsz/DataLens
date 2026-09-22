# DataLens

Plataforma de inteligência comercial para limpeza, análise e visualização de dados B2B. O DataLens centraliza a carteira de clientes de uma empresa, padroniza planilhas importadas e gera indicadores e insights estratégicos para times de vendas e consultoria.

## Sumário

- [Sobre o projeto](#sobre-o-projeto)
- [Tecnologias](#tecnologias)
- [Como executar](#como-executar)
- [Estrutura do projeto](#estrutura-do-projeto)
- [Telas e rotas](#telas-e-rotas)
- [Equipe](#equipe)

## Sobre o projeto

O DataLens é dividido em duas áreas:

- **Área pública** — página inicial de apresentação do produto e tela de login.
- **Área interna** — dashboard, importação de planilhas, análises e demais módulos de gestão da carteira de clientes, acessados após o login.

Este repositório contém o front-end da aplicação, construído com dados simulados enquanto a integração com a API ainda está em desenvolvimento.

## Tecnologias

- [Vue 3](https://vuejs.org/) (Composition API / `<script setup>`)
- [Vite](https://vite.dev/)
- [Vue Router](https://router.vuejs.org/)
- [Tailwind CSS 4](https://tailwindcss.com/)
- [Chart.js](https://www.chartjs.org/) via [vue-chartjs](https://vue-chartjs.org/)
- [Lucide Icons](https://lucide.dev/) (`lucide-vue-next`)

## Como executar

Pré-requisitos: [Node.js](https://nodejs.org/) `^22.18.0` ou `>=24.12.0`.

```sh
# Instalar as dependências
npm install

# Ambiente de desenvolvimento (com hot-reload)
npm run dev

# Build de produção
npm run build

# Pré-visualizar o build de produção
npm run preview
```

## Estrutura do projeto

```
src/
├── assets/          # Estilos globais, logos e imagens
├── components/       # Componentes reutilizáveis (Header, Sidebar, Topbar, Footer, cards)
│   └── charts/        # Wrappers de gráficos (Chart.js) — Donut, Bar, Area
├── data/             # Dados simulados (mock) usados enquanto não há API
├── layouts/          # Layouts de página (área interna com Sidebar + Topbar)
├── plugins/          # Configuração de bibliotecas (registro do Chart.js)
├── router/           # Definição das rotas da aplicação
├── utils/            # Funções utilitárias (formatação, exportação CSV)
└── views/            # Telas da aplicação
```

## Telas e rotas

| Tela | Rota | Descrição |
|---|---|---|
| Home | `/` | Página pública de apresentação do produto |
| Login | `/login` | Autenticação de acesso à área interna |
| Dashboard (Visão Geral) | `/dashboard` | KPIs, insights estratégicos e gráficos da carteira |
| Importação de Dados | `/importacao` | Upload de planilhas com validação e progresso |
| Análises | `/analises` | Relatório de clientes com filtros, ordenação e exportação |
| Clientes, Consultores, Segmentos, Serviços, Insights, Qualidade dos Dados, Configurações | — | Módulos previstos no menu, ainda em construção |

A autenticação e a importação de planilhas são simuladas nesta versão, já que a API ainda não está disponível.

## Equipe

- Enzo Alves Turcovic
- Henrique de Paula Valim Melo
- Bruno Henrique da Silva Pereira
- Maicon Oliveira De Santana
- Gabrielle Júlia Andrade da Silva
