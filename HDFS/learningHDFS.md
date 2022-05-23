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

5. Move directory "/input/exercises-data/escola" and file "/input/exercises-data/entrada1.txt" to data


6. Move file "entrada1.txt" to recover

7. Download file from hdfs "escola/alunos.json" to localsystem /

8. Delete directory recover

9. Delete permanentnly directory delete

10. Find file "alunos.csv" inside /user

11. Show last 1KB from file "alunos.csv"

12. Show 2 first lines from file "alunos.csv"

13. Checksum information from file “alunos.csv”

14. Create a empty file with name “test” in 'student_name' directory

15. Change replication factor from file “test” to 2

16. Show information from file "alunos.csv"

17. Show free space from 'student-name' directory and disk usage