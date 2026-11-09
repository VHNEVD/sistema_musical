# 🎵 Sistema Musical - Protótipo Front-end

> Projeto desenvolvido como parte das atividades de avaliação e aprendizado no curso de Tecnologia da Informação (TI).

---

## 👤 Autor
* **Nome:** Victor Hugo Franck Voltarelli
* **Curso:** Tecnologia da Informação (TI)

---

## 📌 Sobre o Projeto

O **Sistema Musical** é um protótipo de aplicação web voltado para a gestão de acervos musicais, artistas e álbuns. O objetivo central deste projeto foi criar uma interface moderna, intuitiva e totalmente responsiva utilizando HTML5 e CSS3 nativos, aplicando boas práticas de estruturação de código, variáveis de CSS e técnicas de layout avançadas (Flexbox e CSS Grid).

---

## 🚀 Funcionalidades da Interface

- **Tela de Login (`login.html`):**
  - Centralização responsiva do formulário de autenticação.
  - Campos estruturados para usuário e senha com validações HTML nativas.
  - Caixa explicativa com credenciais de teste para navegação fácil.

- **Menu Principal (`index.html`):**
  - Dashboard centralizado com navegação em formato de cards.
  - Atalhos diretos para o cadastro de artistas, cadastro de músicas e consulta à biblioteca.

- **Gestão de Artistas (`cadastro_artista.html`):**
  - Formulário em grade (`form-grid`) para entrada de dados dos artistas.
  - Suporte a upload de fotos/arquivos de imagem (`enctype="multipart/form-data"`).
  - Tabela com lista de artistas cadastrados e ações rápidas (Editar, Excluir e Acesso às Músicas).

- **Gestão de Músicas (`cadastro_musica.html`):**
  - Relacionamento visual através da seleção de artistas cadastrados (`select`).
  - Campos de entrada para título, álbum, gênero, link do YouTube, upload da capa do álbum e campo amplo (`full`) para a letra da música.
  - Tabela listando as músicas do artista com opção de atalho direto para o vídeo no YouTube.

- **Biblioteca Musical (`listagem_musicas.html`):**
  - Painel de filtros gerais (busca por texto, filtro por artista e gênero).
  - Visualização em tabela com miniaturas de capas/placeholder para itens sem imagem.
  - Links para assistir ao conteúdo em nova aba (`target="_blank"`).

---

## 💻 Tecnologias Utilizadas

- **HTML5:** Estruturação semântica da página, formulários com validação integrada (`required`, `type="url"`, `type="file"`, etc.) e acessibilidade (`lang="pt-br"`, rótulos `label`).
- **CSS3:** Estilização global centralizada em um único arquivo (`styles.css`), utilizando:
  - **Variáveis CSS (`:root`):** Padronização de paleta de cores, sombras e tipografia.
  - **Flexbox & CSS Grid:** Construção da estrutura das páginas, alinhamentos e formulários em colunas.
  - **Design Responsivo (@media queries):** Adaptação completa da interface para dispositivos móveis e tablets.

---

## 🛠️ Como Foi Fazer Este Código? (Processo de Desenvolvimento)

O desenvolvimento deste sistema foi estruturado de forma incremental, dividindo o aprendizado em aulas e etapas práticas:

### 1. Planejamento de Layout e Estilo Global (Aula 1)
O primeiro passo foi construir o arquivo central de estilos `styles.css`. A ideia foi definir variáveis para todas as cores (como azul para ações principais, verde para navegação de músicas, vermelho para perigo/exclusão e tons neutros para fundo e cartões). 
Em seguida, foram implementados os componentes básicos reutilizáveis:
- Reset de CSS (`box-sizing: border-box`).
- Formulários em formato de cartões com foco estilizado nos campos (`input:focus`).
- Padronização de botões (`.btn-primary`, `.btn-back`, etc.).
- Centralização da tela de login e grid de cards do menu principal.

### 2. Criação de Tabelas, Ações e Filtros (Aula 2)
Na segunda etapa, o foco foi a exibição de dados e a criação do visual da **Biblioteca Musical**.
- Implementação de tabelas com cabeçalhos escuros e linhas interativas ao passar o mouse (`tbody tr:hover`).
- Criação dos componentes visuais para "Sem foto" / "Sem capa" quando não há imagem.
- Construção da barra de filtros no topo das listagens.

### 3. Formulários Avançados e Organização em Grade (Aula 3)
Nesta fase, foram criadas as páginas `cadastro_artista.html` e `cadastro_musica.html`. 
- Organização dos campos do formulário em duas colunas através de `.form-grid`.
- Implementação de botões de navegação específicos para ligar o cadastro de um artista diretamente às suas músicas.

### 4. Campos Especiais, Utilitários e Responsividade (Aula 4)
A etapa final envolveu o refinamento técnico da aplicação:
- Adição da classe `.full` ao CSS para permitir que a caixa da letra da música (`textarea`) ocupe toda a largura da grade.
- Uso de novos tipos de inputs (`type="url"`, `type="number"`, `type="date"`).
- Aplicação de regras de **Media Queries (`@media (max-width: 768px)`)** no final do CSS para garantir que todas as tabelas, formulários e cartões fiquem legíveis e adaptados para telas pequenas (celulares).

---

## 📁 Estrutura de Arquivos

```text
.
├── index.html              # Menu principal do sistema
├── login.html              # Tela de autenticação
├── cadastro_artista.html   # Cadastro e listagem de artistas
├── cadastro_musica.html    # Cadastro e listagem de músicas
├── listagem_musicas.html   # Biblioteca musical com busca e filtros
└── styles.css              # Folha de estilos única para todas as telas
