# SIPE

> Sistema de solicitação de documentos digitais do IEEP para alunos e servidores.

## Sobre

O **SIPE** (Sistema Integrado de Pedidos Escolares) é o projeto integrador do IEEP.
O objetivo é digitalizar e otimizar a solicitação de documentos para alunos e
servidores, substituindo o fluxo manual por uma aplicação web.

## Funcionalidades

- Login e sessão para alunos, secretários e administradores.
- Abertura e acompanhamento de solicitações de documentos.
- Upload de arquivos e PDFs para as solicitações.
- Respostas e atualização de status pela secretaria.
- Painel de métricas de atendimento com gráficos.
- Gestão de usuários e configurações pelo administrador.
- Navegação SPA com React Router.
- Perfil do usuário e troca de senha.

## Tecnologias

### Frontend

- React + Vite
- Tailwind CSS
- AOS (animações)
- Font Awesome
- Google Sans
- React Router DOM
- Recharts
- LocalStorage e FormData

### Backend e banco

- PHP com PDO
- MySQL (XAMPP)
- MD5 para senhas no projeto acadêmico (para produção, use
  `password_hash`/`password_verify`)
- CORS

## Download e acesso

Não há uma demo pública. O sistema roda localmente com XAMPP; siga os passos abaixo.

## Como rodar

### Requisitos

- Node.js e npm
- XAMPP (Apache + MySQL)
- PHP

### Banco de dados

1. Inicie o MySQL no XAMPP.
2. Importe `sistema-sipe/database/database_sipev3.4.1.sql` no phpMyAdmin.
3. O `conexao.php` usa o banco `projeto_integrador`, usuário `root` e senha vazia;
   ajuste se o seu ambiente for diferente.

### Backend

Copie a pasta `sistema-sipe/backend` para `htdocs/pdgdsa/backend` e inicie o Apache.
O frontend chama a API em `http://localhost/pdgdsa/backend/...`.

### Frontend

```bash
cd sistema-sipe/frontend
npm install
npm run dev
```

Abra a URL exibida pelo Vite (normalmente `http://localhost:5173`).

## Estrutura

```
sistema-sipe/frontend    aplicação React/Vite
sistema-sipe/backend     API PHP
sistema-sipe/database    scripts SQL e modelo do MySQL Workbench
site-institucional       site de apresentação do projeto
organizar/               documentos e materiais do projeto
projeto-escrito/         documento escrito
```

## Licença

Projeto acadêmico do IEEP; sem licença definida.
