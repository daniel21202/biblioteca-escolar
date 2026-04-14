# 📚 BiblioEscola

Sistema web de gerenciamento de biblioteca escolar. Permite que escolas cadastrem seu acervo de livros e que alunos visualizem o catálogo e agendem empréstimos — tudo em tempo real via Firebase.

## ✨ Funcionalidades

### 🏫 Painel da Escola
- Cadastro e login com senha exclusiva por escola
- Adicionar e remover livros do acervo (com foto de capa)
- Gerenciar empréstimos: confirmar devoluções e ajustar prazos
- Dashboard com estatísticas (livros, empréstimos ativos, atrasos)
- Alertas de livros em atraso
- Histórico de atividades recentes
- Gerenciamento de alunos cadastrados
- Configuração do prazo padrão de empréstimo
- Exportação de dados de alunos em CSV e PDF

### 👨‍🎓 Painel do Aluno
- Login com nome, série e nome da escola
- Primeiro acesso cria uma senha pessoal
- Catálogo de livros com busca por título ou autor
- Agendamento de empréstimos com data de retirada e devolução
- Acompanhamento dos próprios empréstimos

## 🛠 Tecnologias

- **HTML5 / CSS3 / JavaScript** — aplicação single-page sem frameworks
- **Firebase Firestore** — banco de dados em tempo real
- **Google Fonts** — Playfair Display + DM Sans

## 🗂 Estrutura do Firestore

```
escolas/
  {escolaId}/
    (doc raiz)     → senha, prazo padrão
    livros/        → acervo de livros
    emprestimos/   → registro de empréstimos
    atividade/     → log de atividades recentes

alunos/
  {alunoKey}       → nome, série, senha (global entre escolas)
```

## 🚀 Como usar

Por ser uma aplicação de arquivo único, não há instalação necessária.

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/biblioescola.git
   ```

2. Abra o arquivo `index.html` diretamente no navegador, **ou** faça o deploy em qualquer serviço de hospedagem estática (Vercel, Netlify, GitHub Pages).

> ⚠️ O Firebase já está configurado no projeto. Para usar com seu próprio banco de dados, substitua o objeto `firebaseConfig` no final do arquivo pelas credenciais do seu projeto Firebase.

## ⚙️ Configurando seu próprio Firebase

1. Acesse [console.firebase.google.com](https://console.firebase.google.com)
2. Crie um projeto e ative o **Firestore Database**
3. Vá em **Configurações do projeto → Seus apps → Web**
4. Copie o objeto `firebaseConfig` gerado e substitua no `index.html`
5. No Firestore, configure as **regras de segurança** conforme sua necessidade

## 📁 Estrutura do Projeto

```
biblioescola/
└── index.html   # Aplicação completa (HTML + CSS + JS)
```

## 📄 Licença

Este projeto está sob a licença MIT. Sinta-se livre para usar, modificar e distribuir.
