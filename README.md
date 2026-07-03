# 📅 Controle de Férias — Regional Ampére

O **Controle de Férias** é uma aplicação web de página única (SPA) projetada para otimizar, gerenciar e monitorar as escalas de descanso da equipe técnica da Regional Ampére e suas respectivas cidades de atuação. Desenvolvido com um design moderno e elegante no padrão *dark mode* (paleta em preto, grafite e detalhes em vermelho premium), o sistema automatiza a identificação de furos de escala e concorrência de períodos.

---

## ✨ Funcionalidades Principais

*   **⚡ Gerenciamento Dinâmico (CRUD):** Interface intuitiva para adicionar, carregar para edição ou excluir escalas de técnicos em tempo real.
*   **🔤 Ordenação Alfabética Inteligente:** A tabela e a base de dados mantêm-se permanentemente ordenadas em ordem alfabética por **Cidade de atuação**. Caso existam múltiplos técnicos na mesma cidade, o sistema realiza um segundo nível de ordenação automática pelo **Nome do colaborador**.
*   **⚠️ Gestão Desbloqueada de Conflitos:** Identifica e sinaliza em vermelho na listagem se houver sobreposição de datas entre colaboradores da mesma localidade. **Mesmo em estado de conflito, o técnico permanece visível e totalmente disponível para edição imediata** do período diretamente na escala.
*   **📅 Calendário Mensal Integrado:** Distribui os períodos de gozo em blocos cronológicos por mês. Exibe de forma clara e ao lado do nome do técnico a sua cidade e o intervalo completo de datas (`DD/MM/AAAA a DD/MM/AAAA`).
*   **🔔 Painéis de Alerta Rápidos:**
    *   *Retornando em Breve:* Alerta os técnicos que voltam às atividades nos próximos 7 dias.
    *   *Saindo em Breve:* Destaca os colaboradores que iniciam o recesso nos próximos 30 dias.

---

## 🛠️ Tecnologias Utilizadas

O projeto foi construído de forma nativa e autônoma, sem dependências ou frameworks externos, o que garante excelente performance e portabilidade:

*   **HTML5** — Estruturação semântica da aplicação.
*   **CSS3** — Customização com variáveis globais (`:root`), transições fluidas e Grid/Flexbox para total responsividade (desktop e mobile).
*   **JavaScript (ES6+)** — Mecanismo lógico em memória, algoritmos de ordenação composta (`localeCompare`) e checagem de intersecção de datas.

---

## 🚀 Como Executar o Projeto

1.  **Copie o código** do arquivo principal (ex: `index.html`).
2.  **Salve o arquivo** localmente na sua máquina.
3.  **Abra o arquivo diretamente** em qualquer navegador moderno (Chrome, Edge, Firefox, Safari).
    *   *Nota: Por gerenciar os dados dinamicamente na memória da página, nenhuma configuração de banco de dados ou servidor web é requerida para o uso.*

---

## 📂 Arquitetura Lógica

### Principais engrenagens do motor JavaScript:
*   `renderizarApp()`: Função centralizadora que limpa e reconstrói a interface. Aplica a ordenação alfabética por Cidade ➡️ Técnico, recalcula os painéis informativos e reconstrói o calendário mensal.
*   `verificarSobreposicao(ini1, fim1, ini2, fim2)`: Algoritmo booleano que valida matematicamente se duas janelas de tempo se cruzam.
*   `carregarParaEdicao(id)`: Captura o ID do objeto clicado (independente de estar em conflito ou não), transporta os dados de volta para o formulário no topo da página com rolagem suave (`smooth scroll`) e altera o comportamento do botão para salvar as modificações.

---

## 🎨 Design System (Paleta de Cores)

| Elemento | Aplicação Visual | Hexadecimal |
| :--- | :--- | :--- |
| Fundo Geral | Plano de fundo da aplicação | `#0b0b0b` |
| Cards / Paineis | Superfície dos blocos de conteúdo | `#161616` |
| Cor Primária | Botões principais e destaques de marca | `#e50914` |
| Alerta / Perigo | Badges de conflito e exclusão | `#ff3333` |
| Elementos Neutros | Botões secundários e bordas internas | `#444444` |

---

## 📌 Notas de Atualização
> 💡 **Aprimoramento do Fluxo:** A ordenação estruturada garante que o gestor visualize as cidades agrupadas em blocos contínuos. O ajuste na escala remove restrições de clique nos itens com alertas vermelhos, agilizando a correção e a resolução de conflitos de agenda imediatamente.
