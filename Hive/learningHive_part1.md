1. Send local file "/input/exercises-data/populacaoLA/populacaoLA.csv" to directory on HDFS "/user/aluno/student_name/data/populacao"

`hdfs dfs -mkdir /user/aluno/jessica/data/population `
`hdfs dfs -put /input/exercises-data/populacaoLA/populacaoLA.csv  /user/aluno/jessica/data/population`

2. List databases on Hive
`show databases;`

3. Create database 'student_name'
`create database jessica` 

4. Create Hive table on database 'student_name'

Intern table: pop
Fields:
zip_code - int
total_population - int
median_age - float
total_males - int
total_females - int
total_households - int
average_household_size - float
Propriedades
Delimiters: Field ',' | Line '\n'
Without partition
Filetype: Text
tblproperties("skip.header.line.count"="1")'

```
 create table pop(
 zip_code int, 
 total_population int,
 median_age float,
 total_males int,
 total_females int,
 total_households int,
 average_household_size float
 )
 row format delimited
 fields terminated by ','
 lines terminated by '\n'
 stored as textfile
 tblproperties("skip.header.line.count"=1");
 ```

5. Visualizar a descrição da tabela pop

`desc pop;`
`desc formatted pop`

6.Selecionar os 10 primeiros registros da tabela pop

`select * from pop limit 10`

7.Carregar o arquivo do HDFS “/user/aluno/student_name/data/população/populacaoLA.csv” para a tabela Hive pop
 `load data inpath 'user/aluno/jessica/data/population' overwrite into table pop`

8.Contar a quantidade de registros da tabela pop
`select count(*) from pop`