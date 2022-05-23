1. Docker Installation - ok 
2. Download images from Big Data Cluster - ok 
3. Start Hadoop cluster through docker-compose
    - `docker-compose up -d` 
4. List images on execution 
    - `docker ps` 
5. Verify docker-compose container logs
    - `docker-compose logs`
6. Verify namenode container logs
    - `docker logs namenode`
7. Access namenode container
    - `docker exec -it namenode bash`
8. List directory from namenode container
   - `ls` 
9. Stop Cluster Big Data's containeres
   - `docker-compose stop`