# JobTracker Pro - Gestão de Candidaturas

O **JobTracker Pro** é uma aplicação web *single-page* desenvolvida para organizar, acompanhar e analisar candidaturas a vagas de emprego. Projetado com uma arquitetura *offline-first*, o sistema opera diretamente no navegador utilizando `localStorage`, oferecendo persistência local rápida, dashboards interativos e suporte robusto para importação e exportação de dados em CSV.

---

##  Funcionalidades Principais

* **Formulário Expansível:** Cartão de cadastro "Nova Candidatura" minimizado por padrão com botão de alternância (`+`/``) para otimizar o espaço em tela.
* **Seleção de Plataforma de Inscrição:** Campo para indicar onde ocorreu a candidatura com opções predefinidas (*LinkedIn*, *Gupy*, *CenterRH*, *Sólides*, *Infojobs*) e a opção **Outro**, que permite digitar e salvar dinamicamente novas plataformas personalizadas no `localStorage`.
* **Atualização Dinâmica de Status:** Alteração do status diretamente na tabela por meio de menus suspensos (`select`), sincronizando a cor do indicador visual, o armazenamento local e os gráficos em tempo real.
* **Índices Sequenciais Automáticos:** Reorganização automática dos IDs (1, 2, 3...) ao excluir qualquer registro, eliminando lacunas de numeração na visualização.
* **Persistência Offline (`localStorage`):** Armazenamento local seguro das candidaturas e plataformas personalizadas, garantindo funcionamento 100% offline.
* **Importação e Exportação CSV Robustas:**
  * Exportação e importação de backups completos.
  * Compatibilidade retroativa com arquivos de 5 colunas e suporte ao novo formato de 6 colunas (incluindo plataforma).
  * *Parser* inteligente com detecção automática de delimitadores por vírgula (`,`) ou ponto e vírgula (`;`).
  * Tratamento de campos com aspas e separadores internos para evitar desalinhamento de colunas.
  * Conversão automática de formatos de data (`DD/MM/AAAA` para `AAAA-MM-DD`).
* **Dashboard e Métricas de Mercado:**
  * Indicadores numéricos de **Total de Candidaturas**, **Empresas Distintas** e **Cargos Distintos**.
  * Visualização gráfica interativa com alternância entre **Gráfico de Barras** e **Gráfico de Pizza**.
  * Algoritmo de geração de cores vibrantes únicas (proporção áurea HSL) para evitar repetição de tonalidades.
  * Rótulos percentuais exibidos diretamente sobre as fatias do gráfico de pizza via `ChartDataLabels`.
  * Legenda customizada em HTML com barra de rolagem (*scroll*) para exibir todos os itens sem cortar texto ou poluir o gráfico.
* **Notificações de Estagnação:** Alerta visual automático destacado para candidaturas que permanecem no status "Aguardando chamada" por mais de 7 dias.
* **Interface Moderna com Tailwind CSS:** Layout responsivo construído com cartões elevados (`rounded-2xl`), efeitos de *backdrop-blur*, gradientes sutis e barras de rolagem personalizadas.

---

##  Tecnologias Utilizadas

* **HTML5:** Estruturação semântica da aplicação.
* **Tailwind CSS:** Estilização utilitária e design responsivo via CDN.
* **JavaScript (Vanilla ES6+):** Lógica de manipulação de DOM, estado local, manipulação de CSV e suporte ao `localStorage`.
* **Chart.js:** Biblioteca de renderização dos gráficos de métricas.
* **Chart.js DataLabels Plugin:** Exibição de rótulos de porcentagem sobre as fatias e barras dos gráficos.

---

##  Como Executar o Projeto

Como a aplicação é construída em um único arquivo (`index.html`), não é necessária a instalação de dependências, Node.js ou servidores de compilação.

1. Clone este repositório:
   ```bash
   git clone [https://github.com/fabriciovieira-tech/JobTrackerPro.git](https://github.com/fabriciovieira-tech/JobTrackerPro.git)
   ```
2. Abra o arquivo `index.html` diretamente em qualquer navegador moderno.

---

##  Estrutura do Arquivo CSV

Ao importar ou exportar dados, a aplicação gera e aceita arquivos no seguinte formato padronizado:

```csv
id;cargo;empresa;plataforma;data;status
1;Engenheiro de Software;Tech Corp;LinkedIn;2026-08-01;aprovado
2;Analista de Dados;Data Analytics;Gupy;2026-08-02;em entrevista
3;Desenvolvedor Frontend;WebSolutions;CenterRH;2026-08-03;aguardando chamada
```
