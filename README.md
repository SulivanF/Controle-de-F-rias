# 📅 Web App de Controle de Férias - Regional Ampére

Este é um sistema web leve e responsivo desenvolvido para gerenciar a escala, o planejamento e a consulta de férias de técnicos e colaboradores, divididos por cidades de atuação na Regional Ampére.

O aplicativo centraliza as principais informações de RH em uma interface moderna no estilo *dark mode*, automatizando o cálculo de conflitos de datas e facilitando o monitoramento de retornos.

---

## ✨ Funcionalidades Principais

*   **👥 Escala de Férias:** Tabela dinâmica com as informações cruciais de cada colaborador (Cidade, Período Aquisitivo, Admissão, Dias Solicitados, Limite de Início, Início e Fim das Férias).
*   **⚠️ Detecção Automática de Conflitos:** O sistema varre o banco de dados em tempo real e emite um alerta visual crítico (além de alterar o status para "Em Conflito") caso dois ou mais técnicos da **mesma cidade** estejam com períodos de férias sobrepostos.
*   **📅 Calendário de Férias Mensal:** Uma aba dedicada que permite filtrar o mês e o ano para visualizar rapidamente quais técnicos estarão ausentes naquele período específico.
*   **🔔 Alerta de Retorno Breve:** Um painel de avisos inteligente que exibe quais técnicos estão prestes a encerrar as férias nos próximos 7 dias, exibindo a contagem regressiva de dias restantes.
*   **➕ Cadastro Dinâmico:** Formulário integrado para adicionar novos técnicos e registrar suas respectivas escalas diretamente na interface.
*   **⚙️ Edição Direta e Exclusão:** Campos como período aquisitivo, dias solicitados e datas podem ser editados diretamente na tabela com salvamento em tempo real (em memória), além da opção de remover registros.

---

## 🚀 Tecnologias Utilizadas

O projeto foi construído em arquitetura de arquivo único (*Single Page Application*), utilizando tecnologias web nativas para garantir máxima performance e portabilidade:

*   **HTML5:** Estruturação semântica da aplicação.
*   **CSS3:** Estilização moderna utilizando Variáveis CSS (Custom Properties), Flexbox, CSS Grid e design responsivo adaptável para dispositivos móveis e desktops.
*   **JavaScript (ES6+):** Manipulação dinâmica do DOM, lógica de validação de períodos (datas), detecção de concorrência/conflitos e filtragem de calendário.

---

## 💻 Como Executar o Projeto

Como o projeto é feito puramente com tecnologias *front-end* nativas, não há necessidade de instalar dependências complexas (como Node.js, Docker, etc.).

1. Faça o clone ou o download deste repositório.
2. Navegue até a pasta do projeto.
3. Dê um duplo clique no arquivo `index.html` para abri-lo diretamente em qualquer navegador moderno (Chrome, Edge, Firefox, Safari).

---

## 📊 Estrutura de Dados Pré-carregada

O sistema já inicia com uma base de dados realista cobrindo as seguintes cidades polos:
*   Ampére
*   Realeza
*   Capanema
*   Capitão
*   Dois Vizinhos

> 📌 **Nota:** Atualmente, as alterações e inserções são salvas temporariamente na memória do navegador (runtime). Atualizar a página (`F5`) resetará os dados para a lista padrão definida no script.

---

## 🗺️ Roadmap / Próximas Melhorias

*   [ ] Implementar persistência de dados local usando `LocalStorage`.
*   [ ] Adicionar botão para exportar a escala em formato Excel (`.xlsx`) ou PDF.
*   [ ] Integração com banco de dados (ex: Firebase ou uma API local) para salvar as alterações permanentemente entre múltiplos usuários.
