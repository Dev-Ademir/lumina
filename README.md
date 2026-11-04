# Lumina — Website Interativo para Barbearia

Website interativo para salão de cabeleireiro/barbearia, com apresentação de serviços, equipe profissional e experiência de navegação dinâmica. Frontend completo; backend em andamento.

🔗 **Repositório:** https://github.com/Dev-Ademir/lumina

---

## ✨ Funcionalidades

- **Apresentação de serviços** — vitrine dos serviços oferecidos pela barbearia
- **Filtros de serviços** — refino dinâmico da lista exibida
- **Seleção de profissionais** — escolha do profissional desejado
- **Modal de agendamento** — fluxo de agendamento em camada modal
- **Formulário de contato** — canal direto de contato
- **Integração com WhatsApp** — atalho para conversa direta
- **Navegação dinâmica** — UI sincronizada entre filtros, seleção e modal

> ⚠️ Backend em andamento. Por enquanto, o projeto funciona como frontend completo, sem persistência de dados no servidor.

---

## 🛠️ Ferramentas utilizadas

| Ferramenta | Uso |
|---|---|
| **HTML5** | Estrutura da aplicação |
| **React 18** | Biblioteca de UI |
| **JSX** | Sintaxe de componentes |
| **JavaScript ES6+** | Lógica da aplicação |
| **Babel Standalone** | Transpilação do JSX direto no navegador |
| **Tailwind CSS** | Estilização utilitária |
| **SVG** | Ícones e elementos vetoriais |

---

## 🧠 Arquitetura

O projeto roda **React 18 via CDN com Babel Standalone**, o que permite executar a aplicação diretamente no HTML, **sem configuração de ferramentas de build** (sem Webpack, Vite ou npm). Basta abrir o `index.html` em um navegador — ou servir a pasta com qualquer servidor estático.

### Estado da aplicação

O estado compartilhado entre **filtros**, **seleção de profissional** e **modal** é gerenciado com:

- `useState` — estado local dos componentes
- `useEffect` — efeitos colaterais e sincronização
- `useMemo` — memoização de valores derivados, evitando re-renderizações desnecessárias

Essa combinação mantém a UI sempre sincronizada sem custo de performance desnecessário.

---

## 🚧 Obstáculos e soluções

### 1. Rodar React sem build local

**Desafio:** executar uma aplicação React sem configurar ferramentas de build.

**Solução:** uso de **React 18 via CDN** com **Babel Standalone**, permitindo rodar a aplicação diretamente no HTML, sem configuração de ferramentas de build.

### 2. Estado compartilhado entre filtros, seleção de profissional e modal

**Desafio:** manter filtros, seleção de profissional e modal sincronizados sem re-renderizações desnecessárias.

**Solução:** gerenciamento com **`useState`, `useEffect` e `useMemo`**, mantendo a UI sincronizada e evitando re-renderizações desnecessárias.

---

## 🚀 Como executar localmente

Como o projeto não possui build step, há duas formas:

**Opção 1 — Abrir direto no navegador**

Basta abrir o arquivo `index.html` no navegador.

**Opção 2 — Servir com um servidor estático (recomendado)**

```bash
# Python 3
python -m http.server 8000

# ou com Node.js (npx)
npx serve .
