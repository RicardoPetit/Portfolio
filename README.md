# 🚀 Portfólio Profissional 

Bem-vindo ao repositório do meu portfólio e currículo interativo! Este projeto foi desenvolvido para apresentar minha transição de carreira
para a área de Tecnologia da Informação, unindo minha sólida bagagem analítica e de gestão com o desenvolvimento de software moderno.

---

## 🛠️ Tecnologias e Ferramentas

O projeto foi construído utilizando tecnologias modernas de front-end para garantir uma experiência limpa, responsiva e acessível:

* **Linguagens & Frameworks:** C#, .NET Core, ASP.NET Core, Minimal APIs, Python
* **Banco de Dados & Dados:** SQL Server, SQLite, EF Core
* **Front-end & Estilização:** HTML5, Tailwind CSS, JavaScript (Vanilla)
* **Ferramentas & Metodologias:** Git, GitHub, Docker, Pytest, Prompt Engineering, Kanban

---

## ✨ Principais Funcionalidades do Portfólio

* **Layout Hero Moderno:** Seção de destaque com foto de perfil em moldura circular e design responsivo.
* **Modo Escuro / Claro (Dark/Light Mode):** Alternância dinâmica de temas integrada com salvamento de preferência.
* **Filtro Interativo de Competências:** Organização por categorias técnicas (Dev, Banco de Dados, Engenharia & IA).
* **Ações Rápidas:** Cópia facilitada de e-mail e botões de atalho para WhatsApp e GitHub.
* **Otimizado para Impressão:** Folha de estilo dedicada para exportação limpa em PDF/Impressão.

---

## ⚙️ Arquitetura e Componentes do Código (index.html)
O código está modularizado em seções lógicas dentro do próprio arquivo index.html para facilitar a manutenção e o deploy direto em servidores estáticos (como o GitHub Pages):

1. Configuração e Estilização (<head>)
   
* **Tailwind Config: Customização da paleta de cores padrão com a extensão da paleta brand baseada em tons de azul (#0284c7, #0369a1, etc.).
* **Dark Mode Strategy: Configurado para o modo baseado em classes (darkMode: 'class').
* **Regras de Impressão (@media print): Regras CSS dedicadas para ocultar elementos de interface (.no-print) como a barra de navegação e botões, além de remover sombras e garantir contraste ideal para exportação em PDF.

2. Interface e Layout (<body>)
   
* **Barra de Navegação (<nav>): Fixa no topo (sticky), contém o logotipo, o botão de alternância de tema e o atalho para impressão.
* **Hero Section (<header>): Seção de destaque com moldura circular (rounded-full), efeito de desfoque decorativo de fundo e informações primárias.
* **Grid de Competências: Organizado em cartões dinâmicos (.skill-card) com tags atributivas para filtragem.

3. Scripts de Comportamento (<script>)

* **O sistema possui funções nativas em JavaScript puro divididas em três blocos principais:

Gerenciamento de Tema (Dark/Light Mode):

  // Verifica a preferência salva no navegador ou do sistema operacional
  if (localStorage.getItem('color-theme') === 'dark' || (!('color-theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
    document.documentElement.classList.add('dark');
  } else {
    document.documentElement.classList.remove('dark');
  }

* **O ouvinte de eventos (addEventListener) escuta cliques no elemento #themeToggle, alternando dinamicamente a classe dark na tag raiz <html> e persistindo a escolha no localStorage.
* **Cópia para Área de Transferência (copyToClipboard):
Utiliza a API moderna navigator.clipboard.writeText combinada com um componente visual de notificação temporária (Toast).
* **Filtragem Dinâmica de Competências (filterSkills):
Permite filtrar os blocos técnicos por categoria (dev, db, eng ou all) manipulando diretamente a propriedade display dos cartões correspondentes.

🚀 Como Executar o Projeto Localmente
Clone o repositório ou baixe os arquivos para o seu computador:

Bash
git clone [https://github.com/RicardoPetit/portfolio.git](https://github.com/RicardoPetit/portfolio.git)
Certifique-se de que os arquivos index.html e a imagem de perfil (foto.jpg.jpg) estão na mesma pasta.

Abra o arquivo index.html diretamente em qualquer navegador moderno (Google Chrome, Firefox, Edge, etc.) ou utilize a extensão Live Server do Visual Studio Code.

📄 Regras de Contribuição e Manutenção
Alterações de estilo devem respeitar as diretrizes utilitárias do Tailwind CSS.

O suporte a novas seções acadêmicas ou profissionais deve seguir o padrão de cartões em grid responsivo (grid-cols-1 md:grid-cols-2 ou md:grid-cols-3).
