ETL Pipeline para E-commerce: Google Colab & BigQuery


Descrição do Projeto


Este projeto tem como objetivo a construção de um pipeline de ETL (Extração, Transformação e Carga) que unifica, limpa e transforma dados de clientes, pedidos e pagamentos de uma plataforma de e-commerce. O fluxo de dados é feito em Google Colab utilizando pandas para o processamento e Google BigQuery para o armazenamento final dos dados.

Estrutura do Projeto

O pipeline é dividido nas seguintes etapas principais:

Extração: Carregar os dados dos arquivos CSV fornecidos e salvar localmente no Google Colab.

Transformação: Realizar a limpeza dos dados, tratar dados inconsistentes e realizar transformações para gerar insights úteis.

Carga: Enviar os dados transformados para o Google BigQuery, onde ficam armazenados em um data warehouse para posterior análise.

Arquivos de Dados

Os dados fornecidos são compostos por três arquivos CSV:

clientes.csv: Contém informações sobre os clientes, como ID, nome, e-mail, data de nascimento, gênero e estado.

pedidos.csv: Contém informações sobre os pedidos realizados, como ID do pedido, ID do cliente, data do pedido, valor total e status.

pagamentos.csv: Contém informações sobre os pagamentos feitos, como ID do pagamento, ID do pedido, método de pagamento, valor pago e data do pagamento.

Principais Transformações Realizadas

Tratamento de Dados Faltantes ou Inválidos:

Remoção ou correção de registros com e-mails inválidos ou dados inconsistentes (ex: pagamentos com valores zero ou negativos).

Conversão e Formatação de Datas:

As colunas de data foram convertidas para o formato adequado.

Unificação de Tabelas:

As três bases de dados (clientes, pedidos e pagamentos) foram unificadas em uma única tabela consolidada utilizando operações de merge no pandas.

Criação de Colunas Derivadas:

Idade: A idade dos clientes foi calculada a partir da data de nascimento.

Pedido Pago: Uma nova coluna foi criada para indicar se o valor pago foi maior ou igual ao valor total do pedido.

Padronização de Dados:

As colunas de texto (como nome, e-mail e estado) foram padronizadas para minúsculas e maiúsculas conforme necessário e espaços extras foram removidos.

Armazenamento no Google BigQuery:

Após a limpeza e transformação dos dados, a tabela consolidada foi carregada para o Google BigQuery para armazenamento e posterior análise.

Tecnologias Utilizadas

Google Colab: Ambiente interativo para executar o código Python e processar os dados.

Pandas: Biblioteca Python para manipulação de dados em formato tabular.

Google BigQuery: Armazenamento de dados em Data Warehouse para análises em larga escala.

pandas-gbq: Biblioteca para enviar DataFrames diretamente para o Google BigQuery.


Conclusão

Este pipeline de ETL foi desenvolvido para integrar dados de clientes, pedidos e pagamentos, tratar dados inconsistentes, realizar transformações necessárias e carregar os dados de forma eficiente no Google BigQuery. Esse processo facilita o armazenamento e a análise de dados em grande escala, pronto para a criação de relatórios e dashboards.

