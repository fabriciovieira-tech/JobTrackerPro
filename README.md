# JobTracker Pro - Gestão de Candidaturas & Métricas de Mercado

O **JobTracker Pro** é uma aplicação web *single-page* avançada desenvolvida para organizar, gerenciar e analisar candidaturas a vagas de emprego. Projetado sob a filosofia *offline-first*, o sistema roda inteiramente no navegador utilizando `localStorage`, oferecendo persistência local rápida, ordenação dinâmica de dados, edição de registros, suporte a importação/exportação CSV e um painel analítico avançado de métricas de mercado.

---

## ? Funcionalidades Principais

* **Cadastro & Formulário Expansível:**
  * Formulário de cadastro minimizado por padrão com botão de alternância (`+`/`?`) para maximizar a área útil da tela.
  * Seleção de plataforma de inscrição (*LinkedIn*, *Gupy*, *CenterRH*, *Sólides*, *Infojobs*, etc.) com opção **Outro** para salvar dinamicamente novas plataformas no `localStorage`.
* **Histórico & Gestão Interativa:**
  * **Ordenação Dinâmica de Colunas:** Clique nos cabeçalhos (*ID*, *Cargo*, *Empresa*, *Plataforma*, *Data*, *Status*) para ordenar em ordem ascendente (`?`) ou descendente (`?`).
  * **Atualização Direta de Status:** Menu suspenso (`select`) por linha com alteração imediata de cor de destaque e atualização do histórico.
  * **Edição de Registros:** Janela modal interativa para edição rápida de *Cargo*, *Empresa* e *Plataforma* do registro selecionado.
  * **Reindexação Automática:** Reorganização sequencial de IDs (1, 2, 3...) ao excluir qualquer registro.
* **Métricas & Dashboard Analítico Avançado:**
  * **Indicadores Globais:** Total de Candidaturas, Empresas Distintas e Cargos Distintos.
  * **Ofertas por Empresa & Recorrência de Cargos:** Gráficos com suporte a exibição em Barras ou Pizza com legenda customizada em HTML scrollável.
  * **Taxa de Conversão do Funil:** Gráfico de barras horizontais dividindo as fases de envio, respostas/entrevistas e aprovações.
  * **Taxa de Rejeição Fantasma (*Ghosting*):** Métricas de candidaturas ativas, respondidas ou estagnadas sem retorno há mais de 30 dias.
  * **Eficiência por Plataforma:** Gráfico de barras empilhadas (*stacked bars*) cruzando cada plataforma com seus respectivos status.
  * **Tempo Médio de Resposta:** Cálculo automático em dias desde o envio até a atualização de status da vaga.
  * **Velocidade da Aplicação:** Gráfico de linha de tendência acompanhando o volume de submissões mês a mês.
* **Persistência Offline & Portabilidade de Dados:**
  * Armazenamento local seguro (`localStorage`) sem dependência de servidores.
  * Exportação e importação de backups em formato CSV com suporte retroativo a versões anteriores do arquivo.
  * *Parser* robusto que detecta delimitadores (`,` ou `;`) e trata aspas ou separadores internos.
* **Notificações Automáticas:** Alerta visual em destaque para candidaturas que permanecem no status "Aguardando chamada" por mais de 7 dias.
* **Design Moderno:** Interface construída com Tailwind CSS, cartões elevados (`rounded-2xl`), efeitos de *backdrop-blur*, gradientes sutis e barras de rolagem personalizadas.

---

## ?? Tecnologias Utilizadas

* **HTML5:** Estruturação semântica da aplicação.
* **Tailwind CSS:** Estilização utilitária e design responsivo via CDN.
* **JavaScript (Vanilla ES6+):** Manipulação de DOM, estado local, algoritmos analíticos e `localStorage`.
* **Chart.js:** Renderização interativa da suíte de gráficos analíticos.
* **Chart.js DataLabels Plugin:** Exibição de valores percentuais sobre os gráficos.

---

## ? Como Executar o Projeto

Como a aplicação é construída em um único arquivo (`index.html`), ela não exige instalação de pacotes Node.js, dependências ou servidores de compilação.

1. Clone o repositório:
   ```bash
   git clone [https://github.com/fabriciovieira-tech/JobTrackerPro.git](https://github.com/fabriciovieira-tech/JobTrackerPro.git)
   ```
2. Abra o arquivo `index.html` diretamente em qualquer navegador moderno.

---

## ? Estrutura do Arquivo CSV

Ao importar ou exportar dados, a aplicação gera e processa o arquivo no seguinte formato padronizado:

```csv
id;cargo;empresa;plataforma;data;status;dataAtualizacao
1;Engenheiro de Software;Tech Corp;LinkedIn;2026-08-01;aprovado;2026-08-15
2;Analista de Dados;Data Analytics;Gupy;2026-08-02;em entrevista;2026-08-10
3;Desenvolvedor Frontend;WebSolutions;CenterRH;2026-08-03;aguardando chamada;2026-08-03
```
