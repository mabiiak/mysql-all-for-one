# Boas vindas ao projeto All For One

  Projeto feito durante o curso de desenvolvimento web na trybe.

  Esse projeto foi feito para praticar alguns conceitos do SQL, 
  utilizando um banco de dados ja implementado chamado `Northwind`.

## Habilidades
  - Entender o que são bancos de dados

  - Entender como a linguagem de consulta estruturada (SQL)

  - Compreender como as tabelas se encaixam no conceito de banco de dados

  - Entender como usar o MySQL Workbench

  - Compreender o que é uma query SQL e quais são seus tipos de comando

  - Criar queries utilizando:
    - `SELECT`
    - `AS`
    - `CONCAT`
    - `DISTINCT`
    - `COUNT`
    - `LIMIT`
    - `OFFSET`
    - `ORDER BY`
    - `WHERE`
    - `LIKE`
    - `IN` e `BETWEEN`
    - `INSERT`
    - `UPDATE`
    - `DELETE`


# Desenvolvimento

  <details>
    <summary>
      <h3>
        Antes de começar a desenvolver
      </h3>
      </summary>

  1. Clone o repositório
    * `git clone https://github.com/mabiiak/mysql-all-for-one.git`.
    * Entre na pasta do repositório que você acabou de clonar:
      * `cd sd-016-a-mysql-all-for-one`

  2. Instale as dependências
    * `npm install`

  3. Crie uma branch a partir da branch `master`
    * Verifique que você está na branch `master`
      * Exemplo: `git branch`
    * Se não estiver, mude para a branch `master`
      * Exemplo: `git checkout master`
    * Agora, crie uma branch onde você vai guardar os `commits` do seu projeto
      * Você deve criar uma branch no seguinte formato: `nome-de-usuario-nome-do-projeto`
      * Exemplo: `git checkout -b nome-mysql-all-for-one`

  4. Para cada exercício você deve criar um novo arquivo sql seguindo a seguinte estrutura:
    * desafio1.sql, desafio2.sql...desafioN.sql

  5. Adicione as mudanças ao _stage_ do Git e faça um `commit`
    * Verifique que as mudanças ainda não estão no _stage_
      * Exemplo: `git status` (deve aparecer o arquivo que você alterou como desafio1.sql)
    * Adicione o novo arquivo ao _stage_ do Git
        * Exemplo:
          * `git add .` (adicionando solução para desafio 1)
          * `git status` (deve aparecer listado o arquivo _desafio1.sql_ em verde)
    * Faça o `commit` inicial
        * Exemplo:
          * `git commit -m 'descrição do commit'`
          * `git status` (deve aparecer uma mensagem tipo _nothing to commit_ )

  6. Adicione a sua branch com o novo `commit` ao repositório remoto
    * Usando o exemplo anterior: `git push -u origin nome-mysql-all-for-one`

  7. Crie um novo `Pull Request` _(PR)_
    * Vá até a página de _Pull Requests_ do [repositório no GitHub](https://github.com/mabiiak/a-mysql-all-for-one/pulls)
    * Clique no botão verde _"New pull request"_
    * Clique na caixa de seleção _"Compare"_ e escolha a sua branch **com atenção**
    * Clique no botão verde _"Create pull request"_
    * Adicione uma descrição para o _Pull Request_ e clique no botão verde _"Create pull request"_
    * **Não se preocupe em preencher mais nada por enquanto!**
    * Volte até a [página de _Pull Requests_ do repositório](https://github.com/mabiiak/a-mysql-all-for-one/pulls) e confira que o seu _Pull Request_ está criado
  </details>

<details>
  <summary>
    <h3>
      Instruções para restaurar o banco de dados `Northwind`
    </h3>
    </summary>

  1. Faça o download do arquivo de backup [aqui](northwind.sql) clicando em "Raw", depois clicando com botão direito e selecionando "Salvar como" para salvar o arquivo em seu computador.
  2. Abra o arquivo com algum editor de texto, e selecione todo o conteúdo do arquivo usando `CTRL-A`.
  3. Abra o MySQL Workbench.
  4. Abra uma nova janela de query e cole dentro dela todo o conteúdo do arquivo `northwind.sql`.
  5. Selecione todo o código com o atalho `CTRL-A` e depois clique no icone de raio para executar a query.

      ![Restaurando o banco Northwind](images/restore_northwind.png)
  6. Aguarde alguns segundos (espere em torno de 30 segundos antes de tentar fazer algo).
  7. Clique no botão apontado na imagem a seguir para atualizar a listagem de banco de dados.

      ![Tabelas do banco Northwind](images/refresh_databases.png)
  7. Verifique se o banco restaurado possui todas as seguintes tabelas:

      ![Tabelas do banco Northwind](images/northwind.png)
  8. Clique com botão direito em cada tabela e selecione "Select Rows" e certifique-se que todas as tabelas possuem registros. Caso tenha alguma faltando, faça o passo a seguir. Caso contrário, pode ir para próxima seção.
  9. Caso existam tabelas faltando, drope o banco de dados, clicando com o botão direito em cima do banco de dados northwind e selecionando "Drop Schema", e refaça os passos novamente, dessa vez aguardando um tempo maior quando executar o script de restauração.

    ![Drop Schema](images/drop_database.png)

</details>

## Requisitos

    ✅ 1 - Exiba apenas os nomes dos produtos na tabela `products`.

    ✅ 2 - Exiba os dados de todas as colunas da tabela `products`.

    ✅ 3 - Escreva uma query que exiba os valores da coluna que representa a primary key da tabela `products`.

    ✅ 4 - Conte quantos registros existem na coluna `product_name` da tabela `products`.
    
    ✅ 5 - Monte uma query que exiba os dados da tabela `products` a partir do quarto registro até o décimo terceiro.

    ✅ 6 - Exiba os dados das colunas `product_name` e `id` da tabela `products` de maneira que os resultados estejam em ordem alfabética dos nomes.

    ✅ 7 - Mostre apenas os ids dos 5 últimos registros da tabela `products` (a ordernação deve ser baseada na coluna `id`).
    
    ✅ 8 - Faça uma consulta que retorne três colunas, respectivamente, com os nomes 'A', 'Trybe' e 'eh', e com valores referentes a soma de '5 + 6', a string 'de', a soma de '2 + 8'. 

### Desafios sobre filtragem de dados

    ✅ 9 - Mostre todos os valores de `notes` da tabela `purchase_orders` que não são nulos.

    ✅ 10 - Mostre todos os dados da tabela `purchase_orders` em ordem decrescente, ordenados por `created_by` em que o `created_by` é maior ou igual a 3.

    ✅ 11 - Exiba os dados da coluna `notes` da tabela `purchase_orders` em que seu valor de `Purchase generated based on Order` é maior ou igual a 30 e menor ou igual a 39.

    ✅ 12 - Mostre as `submitted_date` de `purchase_orders` em que a `submitted_date` é do dia 26 de abril de 2006.

    ✅ 13 - Mostre o `supplier_id` das `purchase_orders` em que o `supplier_id` seja 1 ou 3.

    ✅ 14 - Mostre os resultados da coluna `supplier_id` da tabela `purchase_orders` em que o `supplier_id` seja maior ou igual a 1 e menor ou igual 3.

    ✅ 15 - Mostre somente as horas (sem os minutos e os segundos) da coluna `submitted_date` de todos registros da tabela `purchase_orders`.

    ✅ 16 - Exiba a `submitted_date` das `purchase_orders` que estão entre `2006-01-26 00:00:00` e `2006-03-31 23:59:59`.

    ✅ 17 - Mostre os registros das colunas `id` e `supplier_id` das `purchase_orders` em que os `supplier_id` sejam tanto 1, ou 3, ou 5, ou 7.

    ✅ 18 - Mostre todos os registros de `purchase_orders` que tem o `supplier_id` igual a 3 e `status_id` igual a 2.

    ✅ 19 - Mostre a quantidade de pedidos que foram feitos na tabela `orders` pelo `employee_id` igual a 5 ou 6, e que foram enviados através do método(coluna) `shipper_id` igual a 2.

### Desafios de manipulação de tabelas

    ✅ 20 - Adicione à tabela `order_details` um registro com `order_id`: 69, `product_id`: 80, `quantity`: 15.0000, `unit_price`: 15.0000, `discount`: 0, `status_id`: 2, `date_allocated`: NULL, `purchase_order_id`: NULL e `inventory_id`: 129.

    ✅ 21 - Adicione com um único `INSERT`, duas linhas à tabela `order_details` com os mesmos dados do requisito 20.

    ✅ 22 - Atualize os dados de `discount` do `order_details` para 15. (Não é necessário utilizar o SAFE UPDATE em sua query).

    ❌ 23 - Atualize os dados da coluna `discount` da tabela `order_details` para 30, onde o valor na coluna `unit_price` seja menor que 10.0000.

    ❌ 24 - Atualize os dados da coluna `discount` da tabela `order_details` para 45, onde o valor na coluna `unit_price` seja maior que 10.0000 e o id seja um número entre 30 e 40.

    ❌ 25 - Delete todos os dados em que a `unit_price` da tabela `order_details` seja menor que 10.0000.

    ❌ 26 - Delete todos os dados em que a `unit_price` da tabela `order_details` seja maior que 10.0000.

    ❌ 27 - Delete todos os dados da tabela `order_details`.
