1. Usar o banco de dados 'student_name'

`use jessica;`

2. Selecionar os 10 primeiros registros da tabela pop

`select * from pop limit 10;` 

3. Criar a tabela pop_parquet no formato parquet para ler os dados da tabela pop

`create table pop_parquet(
    zip_code int, 
    total_population int,
    median_age float,
    total_males int,
    total_females int,
    total_households int,
    average_household_size float
 )
 stored as parquet; `

4. Inserir os dados da tabela pop na pop_parquet
` insert into pop_parquet select * from pop;`

5. Contar os registros da tabela pop_parquet

`select count(*) from pop_parquet;`

6. Selecionar os 10 primeiros registros da tabela pop_parquet

`select * from pop_parquet limit 10;`

7. Criar a tabela pop_parquet_snappy no formato parquet com compressão Snappy para ler os dados da tabela pop

`create table_pop_parquet_snappy(

    zip_code int, 
    total_population int,
    median_age float,
    total_males int,
    total_females int,
    total_households int,
    average_household_size float
 )
 stored as parquet
 tblproperties('parquet.compress'='SNAPPY'); `

8. Inserir os dados da tabela pop na pop_parquet_snappy

` insert into pop_parquet_snappy select * from pop;`

9. Contar os registros da tabela pop_parquet_snappy

`select count(*) from pop_parquet_snappy;`

10. Selecionar os 10 primeiros registros da tabela pop_parquet_snappy

`select * from pop_parquet_snappy limit 10;`

