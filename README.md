<h1 align="center">
  🐾 Geo Pet Care - Plataforma de Gestão para ONGs
</h1>

<p align="center">
  <a href="#-sobre-o-projeto">Sobre</a> •
  <a href="#-funcionalidades">Funcionalidades</a> •
  <a href="#-tecnologias">Tecnologias</a> •
  <a href="#-arquitetura-e-segurança">Arquitetura e Segurança</a> •
  <a href="#-como-executar">Como Executar</a>
</p>

---

## 💻 Sobre o Projeto

O **Geo Pet Care** é um sistema ponta a ponta desenvolvido para modernizar e digitalizar a gestão de Organizações Não Governamentais (ONGs) de proteção animal. 

O projeto centraliza operações críticas como o cadastro e triagem de animais resgatados, gerenciamento de voluntários, controle de doações e, o seu principal diferencial: um motor de "Match" que conecta de forma inteligente o perfil de adotantes aos pets disponíveis, otimizando e acelerando o processo de adoção responsável.

## ✨ Funcionalidades

O sistema é dividido em uma API Restful robusta e um Dashboard Administrativo, contemplando:

- **🔑 Autenticação e Autorização:** Login seguro para administradores e voluntários com controle de sessão.
- **🐶 Gestão de Pets (CRUD):** Cadastro completo de animais, incluindo histórico de saúde, triagem e status atual.
- **🤝 Motor de Match (Match Service):** Lógica inteligente que cruza dados de formulários de adotantes com as características dos animais disponíveis.
- **👥 Gestão de Pessoas:** Módulos dedicados para controle de **Adotantes** e **Voluntários**.
- **📊 Transparência e Doações:** Painel e rotas específicas para registro e acompanhamento de recursos arrecadados.

## 🚀 Tecnologias

Este projeto foi construído utilizando as seguintes tecnologias:

**Backend (API Rest):**
- [Node.js](https://nodejs.org/) & [Express.js](https://expressjs.com/)
- Banco de Dados Relacional estruturado via SQL (`mysql2`)
- Proteção de rotas e tokens com `jsonwebtoken`
- Validação de dados com `express-validator`

**Frontend (Dashboard):**
- HTML5, CSS3 & JavaScript (Vanilla)
- Consumo assíncrono da API Rest

## 🛡️ Arquitetura e Segurança

A estrutura do projeto foi desenhada visando escalabilidade, separação de responsabilidades (MVC) e boas práticas de cibersegurança:

- **Padrão MVC e Services:** Lógicas complexas, como o algoritmo de compatibilidade de adoção, estão isoladas na camada de serviço (`src/services/matchService.js`), separadas dos controladores (`src/controllers/`).
- **Middlewares de Segurança:** Acesso a rotas críticas da API protegido por validação de token JWT (`src/middlewares/auth.js`).
- **Proteção de Credenciais:** As chaves de acesso e conexões com o banco de dados são gerenciadas dinamicamente via variáveis de ambiente (`.env`), garantindo que dados sensíveis não sejam versionados publicamente.

## 🛠️ Como Executar (Ambiente Local)

### Pré-requisitos
- Node.js
- Servidor MySQL rodando localmente

### Passo a Passo

1. **Clone o repositório e instale as dependências:**
   ```bash
   git clone [https://github.com/seu-usuario/ong-geopetcare.git](https://github.com/seu-usuario/ong-geopetcare.git)
   cd ong-geopetcare
   npm install
