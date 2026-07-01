# 📅 Controle de Férias - Regional Ampére

Uma aplicação web moderna, responsiva e de alta performance para a gestão, visualização e controle de escalas de férias da equipe técnica da Regional Ampére. Desenvolvida no formato *Single Page Application* (SPA), ela centraliza a estrutura, a estilização e a inteligência em um único arquivo de código limpo.

---

## 🎨 Nova Identidade Visual (Design Atualizado)

O sistema passou por uma reformulação visual completa, adotando uma estética premium inspirada em *Dark Mode* moderno com contrastes marcantes:
*   **Fundo Dark Absoluto:** Base construída em tons de cinza escuro e preto (`#0d0d11`) para garantir o conforto visual em monitoramentos prolongados.
*   **Acentos em Vermelho Vibrante:** Botões de ações principais e destaques estruturais utilizam vermelho cirúrgico (`#e63946`) para direcionar o olhar do usuário.
*   **Alertas Contextuais:** Cores semânticas aplicadas rigorosamente nas caixas de notificação (Verde para retornos iminentes e Laranja para saídas em breve).
*   **Tipografia:** Integração com a fonte *Inter* via Google Fonts, conferindo um aspecto limpo e excelente legibilidade em tabelas de dados.

---

## 🛠️ Funcionalidades e Regras de Negócio Implementadas

### 1. Ordenação Automática por Cidades (Ordem Alfabética)
O motor de renderização organiza os registros de forma estrita e automática em tempo de execução:
*   Qualquer novo técnico inserido ou registro editado faz a tabela inteira ser reorganizada de **A a Z pelo nome da Cidade**.
*   **Critério de Desempate:** Se dois ou mais técnicos pertencerem à mesma cidade, o sistema realiza uma subordinação alfabética secundária baseada no **Nome do Colaborador**.

### 2. Painel Dinâmico de Notificações
Monitoramento inteligente baseado no dia atual configurado no sistema (`01/07/2026`):
*   **Retornando em Breve:** Lista de forma automatizada colaboradores que faltam 7 dias ou menos para encerrar o período de descanso.
*   **Saindo em Breve:** Alerta antecipadamente os técnicos com saídas programadas para os próximos 30 dias.

### 3. Calendário Automatizado por Mês
Geração dinâmica de cartões informativos ao final da página que funcionam como uma linha do tempo, agrupando as férias vigentes mês a mês para prever a cobertura da equipe.

---

## 📁 Estrutura do Projeto

Por conveniência de implantação e compatibilidade total com plataformas como o **CodePen**, o código foi arquitetado de maneira unificada:

```text
├── index.html
    ├── [HEAD]   - Configurações globais e fontes externas (Inter).
    ├── [STYLE]  - CSS moderno construído através de Variáveis Nativas.
    ├── [BODY]   - Componentes visuais (Formulário, Tabela de Dados e Cards).
    └── [SCRIPT] - Motor JavaScript (CRUD, lógica de ordenação e tratamento de datas).
