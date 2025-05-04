# Análise Exploratória de Dados - Vendas Online

## Descrição do Projeto

Uma análise exploratória realizada em um conjunto de dados público de vendas online. O projeto abrange desde o carregamento e limpeza dos dados até a identificação de padrões em clientes, produtos e tendências de vendas utilizando Python e bibliotecas como Pandas, NumPy, Matplotlib e Seaborn. O período analisado vai de 01/12/2010 a 09/12/2011.

## Dataset

* **Nome:** Online Retail Dataset
* **Fonte Original:** UCI Machine Learning Repository
* **Disponibilidade:** Kaggle (entre outras fontes)
* **Link para os Dados no Kaggle:** https://www.kaggle.com/code/fabiendaniel/customer-segmentation
* **Observação:** O arquivo `.csv` original não foi incluído neste repositório por questões de licença/tamanho, mas pode ser obtido no link acima.

## Etapas da Análise

O processo de análise seguiu as seguintes etapas principais:

1.  **Carregamento e Inspeção Inicial:** Leitura do arquivo CSV (tratando encoding), verificação inicial de formato, tipos de dados e valores ausentes (`.info()`, `.head()`, `.shape`, `.isna().sum()`).
2.  **Limpeza e Pré-processamento:**
    * Tratamento de valores ausentes (remoção de linhas sem `CustomerID`).
    * Conversão de tipos de dados (`InvoiceDate` para datetime, `Quantity` e `CustomerID` para int).
    * Identificação e filtro de transações potencialmente inválidas (Quantidades negativas indicando devoluções, Preços unitários zero).
    * Criação de novas features (`ValorTotal` por linha, `Ano`, `Mes`, `Dia`, `Hora`).
3.  **Análise Exploratória de Dados (EDA) e Visualização:**
    * Análise de vendas por País (agregação com `groupby`, visualização com gráfico de barras).
    * Identificação dos Produtos mais vendidos por quantidade (agregação com `groupby`, visualização com gráfico de barras).
    * Identificação dos Clientes mais valiosos por valor total gasto (agregação com `groupby`).
    * Análise de tendência de vendas mensais (agregação com `groupby`, visualização com gráfico de linha).
    * Análise da distribuição dos Preços Unitários (visualização com histograma).

## Principais Insights (Resumo)

* **Concentração Geográfica:** As vendas são predominantemente originadas do Reino Unido (UK).
* **Produtos Chave:** Identificados os produtos com maior volume de vendas (liderados por "PAPER CRAFT , LITTLE BIRDIE").
* **Clientes Valiosos:** Identificados os principais clientes por valor total de compra (liderados por "14646").
* **Tendência Temporal:** Observou-se um pico expressivo nas vendas no final de 2011 (Out/Nov), sugerindo potencial sazonalidade pré-Natal (necessita confirmação com mais dados).
* **Perfil de Preços:** O catálogo é composto majoritariamente por itens de baixo valor unitário, mas com presença de produtos de valor significativamente mais alto.

## Tecnologias Utilizadas

* Python 3
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

## Como Usar (Opcional)

1.  Clone este repositório.
2.  Baixe o dataset original do link fornecido na seção "Dataset".
3.  Coloque o arquivo `.csv` na mesma pasta do notebook.
4.  Execute o notebook Jupyter (`Customer Segmentation.ipynb`).
