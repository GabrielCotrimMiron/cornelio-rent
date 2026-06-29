<div align="center">

# 🏠 Cornelio Rent

### Plataforma de aluguel de imóveis para universitários em Cornélio Procópio, PR

[![Next.js](https://img.shields.io/badge/Next.js-15-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-v4-38bdf8?style=flat-square&logo=tailwindcss)](https://tailwindcss.com/)
[![Deploy](https://img.shields.io/badge/deploy-GitHub%20Pages-222?style=flat-square&logo=github)](https://seu-usuario.github.io/cornelio-rent/)

**[🔗 Ver demo ao vivo](https://seu-usuario.github.io/cornelio-rent/)**

</div>

---

## ✨ Sobre o projeto

**Cornelio Rent** é um protótipo navegável de uma plataforma de aluguel de
imóveis pensada para estudantes universitários de **Cornélio Procópio (PR)**
— próximos à UTFPR, UENP, FACCREI e Dom Bosco.

O projeto nasceu como estudo de caso para uma disciplina de **Engenharia de
Requisitos de Software**, e evoluiu para uma aplicação completa, com fluxos
de cadastro, busca com filtros, anúncio de imóveis e chat entre usuário e
anunciante — tudo com uma identidade visual própria, no estilo que chamamos
de *cyber-luxury*: roxo profundo, glassmorphism e tipografia forte.

> ⚠️ **Importante:** este é um protótipo acadêmico. Não há backend real —
> toda a persistência de dados (login, anúncios, mensagens) acontece via
> `localStorage` do navegador, propositalmente, para focar na demonstração
> de fluxos de UX e requisitos funcionais.

---

## 🎯 Funcionalidades

- 🔍 **Busca com filtros** — preço, pets, república, mobília, garagem, internet
- 🏘️ **Catálogo de imóveis** — cards com carrossel de fotos e custo mensal detalhado
- 📄 **Página de detalhes** — galeria, descrição, regras da casa, imóveis parecidos
- 🔐 **Login e cadastro** — com dois perfis: Usuário e Anunciante
- 📢 **Anunciar imóvel** — formulário multi-step com os mesmos filtros da busca
- 📊 **Painel do anunciante** — gerenciar anúncios (ativar, pausar, excluir)
- 💬 **Chat interno** — conversa entre interessado e anunciante, com respostas simuladas
- 🎨 **Identidade visual própria** — paleta roxa com hierarquia de profundidade (dark UI)

---

## 🛠️ Stack

| Camada | Tecnologia |
|---|---|
| Framework | [Next.js 15](https://nextjs.org/) (App Router) |
| Linguagem | TypeScript |
| Estilo | Tailwind CSS v4 |
| Ícones | [Lucide React](https://lucide.dev/) |
| Estado global | React Context API |
| Persistência | `localStorage` (mock, sem backend) |
| Deploy | GitHub Pages + GitHub Actions |

---

## 📸 Capturas de tela

> _Adicione aqui 2-4 screenshots do site depois de publicado — a Home, a
> página de detalhes e o chat ficam ótimas para mostrar. Pode arrastar as
> imagens direto na issue/PR do GitHub que ele gera o link automaticamente,
> ou subir numa pasta `docs/screenshots/` e referenciar com:_
>
> `![Home](docs/screenshots/home.png)`

---

## 🚀 Rodando localmente

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/cornelio-rent.git
cd cornelio-rent

# Instale as dependências
npm install

# Rode o servidor de desenvolvimento
npm run dev
```

Acesse [`http://localhost:3000`](http://localhost:3000).

---

---

## 🧠 Decisões de arquitetura

- **Dados 100% mock**: imóveis fixos em `lib/properties.ts`; anúncios
  criados pelo usuário em `localStorage` via `lib/listings.ts` — ambos
  seguem a mesma interface `Property`, permitindo tratamento unificado.
- **Autenticação simulada**: `lib/auth.ts` não usa hashing de senha nem
  validação de servidor — é só para demonstrar o fluxo de UX.
- **Chat simulado**: `lib/chat-bot.ts` gera respostas automáticas por
  correspondência de palavras-chave, simulando o anunciante quando ele
  não é um usuário real do sistema.
- **Filtros via Context API**: a sidebar de filtros e o grid de imóveis
  são componentes irmãos, então o estado é compartilhado via
  `FiltersProvider` em vez de prop-drilling.

---

## 📚 Contexto acadêmico

Este projeto foi desenvolvido como estudo de caso prático para a disciplina
de **Engenharia de Requisitos de Software**, com o objetivo de demonstrar:

- Levantamento e modelagem de requisitos funcionais a partir de um cenário real
- Prototipação navegável de alta fidelidade
- Fluxos completos de UX para múltiplos perfis de usuário (usuário vs. anunciante)

---

## 📄 Licença

Este é um projeto acadêmico, livre para fins de estudo e referência.

---

<div align="center">

Feito com 💜 em Cornélio Procópio, PR

</div>
