<div align="center">

# 📊 OrçaView | Dashboard de Controle Orçamentário 2026

### Do Excel à análise gerencial: orçamento vs. realizado, evolução mensal e identificação de desvios de custos

![Status](https://img.shields.io/badge/status-projeto%20de%20portf%C3%B3lio-0e9875?style=flat-square) ![HTML](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white&style=flat-square) ![CSS](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white&style=flat-square) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black&style=flat-square) ![Excel](https://img.shields.io/badge/Excel-217346?logo=microsoftexcel&logoColor=white&style=flat-square)

**[🌐 Dashboard online (após ativar GitHub Pages)](https://keltonalmeida.github.io/dashboard-controle-orcamentario-2026/) · [💻 Código do dashboard](index.html) · [📥 Planilha original](dados/Base_Orcado_Realizado.xlsx)**

</div>

## 🎯 Visão do projeto

Uma análise de custos precisa responder mais do que **“quanto foi gasto?”**. É necessário identificar **onde ocorreram os desvios**, como eles se comportaram ao longo do tempo e quais categorias merecem atenção.

O **OrçaView** transforma uma planilha de custos previstos e realizados em um painel gerencial interativo, com visão executiva e detalhamento operacional. O projeto foi desenvolvido para demonstrar competências em **análise de dados, controladoria, indicadores financeiros, conciliação de bases, visualização e comunicação de resultados**.

## 💡 Destaques da análise

| Indicador | Jan–Set/2026 |
| :--- | ---: |
| Orçado acumulado | **~R$ 3,46 milhões** |
| Realizado acumulado | **~R$ 3,45 milhões** |
| Desvio (realizado − orçado) | **−R$ 11.048,55** |
| Desvio relativo ao orçamento | **−0,32%** |

> Os números são do recorte **janeiro a setembro de 2026**, escolhido como padrão para evitar que meses ainda não encerrados sejam interpretados como realizados consolidados. As métricas variam de acordo com os filtros aplicados no painel. Os valores arredondados acima são informativos.

## 🧭 Funcionalidades

- **KPIs financeiros:** custo orçado, realizado, desvio em reais e desvio percentual.
- **Evolução mensal:** gráfico comparativo entre os valores previstos e realizados.
- **Evolução acumulada:** acompanhamento do comportamento do orçamento e dos gastos no período.
- **Análise dos desvios mensais:** identificação visual de meses com sobrecusto ou economia.
- **Visão por centro de custo:** comparação entre áreas de negócio.
- **Visão por categoria:** detalhamento e participação dos grupos de despesa.
- **Principais direcionadores:** destaque das categorias que mais contribuíram para estouros ou economias.
- **Filtros interativos:** período, centro de custo e categoria.
- **Exportação CSV:** download dos registros conforme os filtros selecionados.
- **Layout responsivo e uso offline:** funciona no navegador, sem instalação de bibliotecas externas.

## 🗂️ Fonte de dados e tratamento

A planilha de referência está disponível em [`dados/Base_Orcado_Realizado.xlsx`](dados/Base_Orcado_Realizado.xlsx).

| Aba | Conteúdo | Volume |
| :--- | :--- | ---: |
| `Orçado` | Despesas previstas para 2026 | 576 registros |
| `Realizado` | Valores registrados na base de 2026 | 576 registros |

As abas possuem os campos **Data, Centro de Custo, Categoria, Fornecedor, Descrição, Valor (R$) e ID Item**. Os dados são reconciliados pela chave **`ID Item`**, permitindo comparar valores correspondentes entre as abas. O painel consolida **6 centros de custo** e **21 categorias**.

**Fórmulas de negócio:**

```text
Desvio (R$) = Realizado − Orçado
Desvio (%) = (Realizado − Orçado) / Orçado × 100
```

Para custos, **desvio positivo** indica gasto acima do orçamento (desfavorável), e **desvio negativo** indica gasto abaixo do orçamento (favorável). A interpretação gerencial também exige contexto: gastar menos não significa necessariamente melhor desempenho operacional.

> **Atenção à competência:** a planilha contém registros de realizado em outubro, novembro e dezembro de 2026, inclusive datas futuras em relação a 22/10/2026. Por isso, o painel inicia em **jan–set/2026**. A opção de ano completo mostra os dados tal como fornecidos, **sem afirmar que meses futuros estejam encerrados**.

## 🛠️ Tecnologias utilizadas

| Tecnologia | Aplicação no projeto |
| :--- | :--- |
| **Excel (.xlsx)** | Base de custos orçados e realizados |
| **HTML5** | Estrutura do dashboard |
| **CSS3** | Identidade visual, cards, layout e responsividade |
| **JavaScript (vanilla)** | Agregações, filtros, indicadores, gráficos SVG e exportação CSV |
| **SVG** | Gráficos renderizados diretamente no navegador |

O dashboard é um arquivo estático independente: os dados utilizados na interface estão incorporados ao `index.html`, dispensando backend e acesso à internet. **A planilha Excel incluída neste repositório é a fonte de referência; editar a planilha não atualiza automaticamente o HTML.**

## 🚀 Como executar

1. Faça o download do repositório em **Code → Download ZIP** ou clone-o:

   ```bash
   git clone https://github.com/KeltonAlmeida/dashboard-controle-orcamentario-2026.git
   ```

2. Abra o arquivo `index.html` em um navegador atualizado.
3. Use os filtros para analisar períodos, centros de custo e categorias.
4. Clique em **Exportar CSV** para obter os registros filtrados.

**Para publicar na web:** acesse [Settings → Pages](https://github.com/KeltonAlmeida/dashboard-controle-orcamentario-2026/settings/pages), em **Build and deployment** selecione **Deploy from a branch**, escolha **main** e **/(root)** e salve. Não há necessidade de build. Após a publicação, o endereço esperado é `https://keltonalmeida.github.io/dashboard-controle-orcamentario-2026/`. **O link só ficará acessível quando o GitHub Pages estiver ativo.**

## 📁 Estrutura do repositório

```text
dashboard-controle-orcamentario-2026/
├── README.md
├── index.html
└── dados/
    └── Base_Orcado_Realizado.xlsx
```

## 🧠 Competências demonstradas

**Controle orçamentário · Análise de desvios · Indicadores financeiros · Conciliação por chave de negócio · Segmentação e agregação de dados · Data storytelling · Desenvolvimento front-end · Visualização de dados · Experiência do usuário**

## 🔐 Observação sobre a publicação

O projeto contém a planilha disponibilizada como referência. Antes de torná-lo público, **confirme que fornecedores, valores e demais informações estão autorizados para divulgação**. A publicação de um repositório público disponibiliza tanto a planilha quanto os dados incorporados ao HTML.

---

<div align="center">

**📈 Transformando dados de orçamento em informações para decisões melhores.**

Projeto de portfólio | Exercício de 2026

</div>
