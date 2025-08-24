this is starter kind of repo for practising the redis ----
like adding the tasks to queue and then letting the workflows to pick tasks -----
It is similar design of leetcode submission queues----



Used docker for making redis locally available -----

Starting redis locally using Docker
docker run --name my-redis -d -p 6379:6379 redis

if you want to interact with redis container---
Connect to your container
docker exec -it container_id /bin/bash

CLI for using redis as DB---
Connecting to the redis cli
redis-cli





