# DLE IN DOCKER
```
chmod 777 ~/dle-docker/data/project/app/{templates,engine/{data,cache}}
chmod -R 777 ~/dle-docker/data/project/app/{backup,uploads}
chmod -R 777 ~/dle-docker/data/project/app/engine/data/emoticons/
```
### Init DB
```
docker exec -it db bash
mysql -u root -p"passpass"
create database testdb character set utf8 collate utf8_bin;
grant all privileges on testdb.* to testuser@'%' identified by 'passpass';
\q
exit
```