1. Start Big Data Cluster

` cd docker-bigdata `
` docker-compose up -d ` 

2. Download exercises

` cd input`
`sudo git clone https://github.com/rodrigo-reboucas/exercises-data.git`

3. Access namenode container
` docker exec -it namenode bash `

4. Create directory structure below with command $ hdfs dfs -ls -R /

<code> 
user/aluno/jessica/data
user/aluno/jessica/recover
user/aluno/jessica/delete
</code>

`mkdir -p aluno/jessica/data`
`mkdir recover`
`mkdir delete`

[exercise4.png](https://github.com/jess197/semantix/blob/main/HDFS/imgs/exercise4.png)

5. Move directory "/input/exercises-data/escola" and file "/input/exercises-data/entrada1.txt" to data

[exercise5.png](https://github.com/jess197/semantix/blob/main/HDFS/imgs/exercise5.png)

6. Move file "entrada1.txt" to recover

[exercise6.png](https://github.com/jess197/semantix/blob/main/HDFS/imgs/exercise6.png)

7. Download file from hdfs "escola/alunos.json" to localsystem /

8. Delete directory recover

[exercise8.png](https://github.com/jess197/semantix/blob/main/HDFS/imgs/exercise8.png)

9. Delete permanentnly directory delete

[exercise9.png](https://github.com/jess197/semantix/blob/main/HDFS/imgs/exercise9.png)

10. Find file "alunos.csv" inside /user

[exercise10.png](https://github.com/jess197/semantix/blob/main/HDFS/imgs/exercise10.png)

11. Show last 1KB from file "alunos.csv"

[exercise11.png](https://github.com/jess197/semantix/blob/main/HDFS/imgs/exercise11.png)

12. Show 2 first lines from file "alunos.csv"

[exercise12.png](https://github.com/jess197/semantix/blob/main/HDFS/imgs/exercise12.png)

13. Checksum information from file “alunos.csv”

[exercise13.png](https://github.com/jess197/semantix/blob/main/HDFS/imgs/exercise13.png)

14. Create a empty file with name “test” in 'student_name' directory

15. Change replication factor from file “test” to 2

[exercise15.png](https://github.com/jess197/semantix/blob/main/HDFS/imgs/exercise15.png)

16. Show information from file "alunos.csv"

[exercise16.png](https://github.com/jess197/semantix/blob/main/HDFS/imgs/exercise16.png)

17. Show free space from 'student-name' directory and disk usage

[exercise17.png](https://github.com/jess197/semantix/blob/main/HDFS/imgs/exercise17.png)
