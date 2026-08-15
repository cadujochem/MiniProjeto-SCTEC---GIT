Mini Projeto Prático SCTEC / SENAI
Carlos Eduardo dos Santos Jochem 
Analise de Dados com Python Turma T3



## Sobre o Projeto

* **Objetivo:**
      Analise exploratória, limpeza, tratamento de dados e Retirada de Insights.
  
* **Contexto:**
      Análise Exploratória do aqruivo base_varejo.csv, adquirido através do Kaggle - Base Varejo](https://www.kaggle.com/datasets/namespaiva/base-varejo/data

  
      

##  Tecnologias e Ferramentas
* **Linguagem:** Python 3.12
* **Bibliotecas principais:** Pandas, NumPy.

##  Estrutura do Repositório
* base_varejo.csv: Arquivos bruto com os dados que serão tratados.
* 'analise-base-varejo.ipynb' : Arquivos Jupyter com o passo a passo da limpeza e exploração.
* 'Base_Varejo_Atualizada.csv': Arquivo CSV Atualizado após Analise e limpeza do arquivo 'base_varejo.csv'


## Como Executar
* Clone este Repoisitorio - Abra a pasta no VSCODE com a extensão Jupiter Notebook instalada,
* execute as células do arquivo 'analise-base-varejo.ipynb' uma a uma inicinando pela primeira e seguindo na sequencia


## Principais Conclusões e Insights

* **A Base de Dados Original posuia um CSV com 14 Colunas e 830.000 linhas com informações Reais de Compras no Varejo
* **Após breve analise exploratória já percebeu-se que existiam 4 colunas sem nenhum dado preenchido e  foram excluídas por não agregar na analise.
* ** Foi alterado os noems das colunas para facilitar a identificação das informações
* ** Coluna 'Data' foi altera para Datetime - e foi criada com base no Datetime as colunas 'Ano', 'Mes' e 'Dia'
* ** Colunas com Tipo de Dados Texto receberam tratamentos para padronização de dados, str.strip() str.title().
* ** Colunas com tipos de dados numéricos conversão para pd.to_numeric() e Coerce para dados preenchidos fora do padrão ficar nulo.
* ** Os Dados de Estado Civil em formato de numerais foram transformados em Categorias: 'Solteiro', 'Casado', 'Divorciado', 'Separado' .ETC
* ** Foi criado uma váriavel para 'valores_invalidos'('#N/D', '#n/a', entre outras) e esses dados foram substituídos para não comprometer métrica da analise.
* ** Após as alterações verificamos não ter mais dados nulos não tratados no DataFrame.
* ** Ao buscar por dados duplicados encontrou-se 96.553 duplicadas, porem por se tratar de uma tabela sem coluna de quantidade,
  o mesmo produto pode ter sido comprado duas vezes. Dessa forma ignoramos os duplicados.
* ** Foram Encontrados 18471 - Identificadores de Compras - NF
* ** Verificado dados de Estatística dos filhos sendo que a maioria dos clientes possui pelo menos 1 filho. Média de 1.15 por Cliente_ID
* ** Ao analisar Compras por Genero dos Clientes - Percebeu-se um cadastro maior de compras por mulheres: Feminino: 52.12%
*  ** Alimentos foi a Categoria com maior registro de compras: 434.767 vezes. Seguido por Higiene, limpeza e Bebidas
*  ** O Produto mais vendido registrado foi "Presunto Cozido" com 14.381 registro quase o dobro dos demais itens na sequencia.
*  ** Não percebeu-se tendencia de um genero ter uma proporção de compras maior por alguma categoria específica.
*  ** Buscando pelo ano de maior quantidade de itens vendidos, 2021 foi o que apresentou o melhor resultado com 245.259 registro de vendas.
*  ** Constatado como uma tendencia maior de vendas nos meses de Janeiro com 83.963 registros de vendas
*  ** Constatado como pior mês de vendas o mês de Novembro com metade do faturamento de Janeiro.


Esse Projeto seguiu o Padrão de  ETL (Extract, Transform, Load) -  Ele funciona como uma linha de produção que transforma 
dados brutos e desorganizados em informações valiosas para a tomada de decisões. O ETL limpa e padroniza as informações, 
garantindo que os analistas trabalhem com dados confiáveis

A Extração ocorreu através da Importação dos dados com a Biblioteca Pandas
para do arquivo CSV para o Formato de DataFrame.

A Tranformação ocorreu atráves da limpeza, normalização, e transformação dos Dados Facilitando o entendimento das informações.
Os dados brutos raramente vêm prontos para uso. Eles contêm duplicatas, valores nulos, formatos inconsistentes (como datas escritas de formas diferentes) 
e erros de digitação. . Dados ruins geram análises ruins

E o Carregamento ocorreu ao final do Script onde neste caso salvamos em um novo arquivo CSV atualizado. Porém poderia ser carregado em bancos de dados SQL,
planilhas de Excel, Warehouses, etc.




