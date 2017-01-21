FROM jamtur01/redis
ENTRYPOINT [ "redis-server","--logfile /var/log/redis/redis-replica.log","--slaveof redis_primary 6379" ]
