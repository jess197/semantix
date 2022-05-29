1. Criar o diretório “/user/aluno/<nome>/data/nascimento” no HDFS

`hdfs dfs -mkdir /user/aluno/jessica/data/nascimento` 

2. Criar uma tabela externa no Hive com os parâmetros:

a) Tabela: nascimento

b) Campos: nome (String), sexo (String) e frequencia (int)

c) Partição: ano

d) Delimitadores:

i) Campo ‘,’

ii)  Linha ‘\n’

e) Salvar

i) Tipo do arquivo: texto

ii) HDFS: '/user/aluno/student_name/data/nascimento’

``` 
   create external table nascimento ( 
       nome string,
       sexo string,
       frequencia int
   )
   partitioned by (ano int)
   row format delimited
   fields terminated by ','
   lines terminated by '\n'
   stored as textfile
   location '/user/aluno/jessica/data/nascimento';
```

3.Adicionar partição ano=2015

`alter table nascimento add partition(ano=2015); `


4.Enviar o arquivo local “input/exercises-data/names/yob2015.txt” para o HDFS no diretório /user/aluno/student_name/data/nascimento/ano=2015

`hdfs dfs -put /input/exercises-data/names/yob2015.txt /user/aluno/jessica/data/nascimento/ano=2015`

5.Selecionar os 10 primeiros registros da tabela nascimento no Hive

`select * from jessica.nascimento where ano=2015 limit 10;`

6.Repita o processo do 3 ao 5 para os anos de 2016 e 2017.

`alter table nascimento add partition(ano=2016); `
`hdfs dfs -put /input/exercises-data/names/yob2015.txt /user/aluno/jessica/data/nascimento/ano=2016`
`select * from jessica.nascimento where ano=2016 limit 10;`

`alter table nascimento add partition(ano=2017); `
`hdfs dfs -put /input/exercises-data/names/yob2015.txt /user/aluno/jessica/data/nascimento/ano=2017`
`select * from jessica.nascimento where ano=2017 limit 10;`