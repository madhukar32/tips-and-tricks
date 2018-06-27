## Here I will be storing all the good to know information related to logs for docker container

* How to clear logs of a particular container

```shell
echo "" > $(docker inspect --format='{{.LogPath}}' <container_name_or_id>)
```

* Taking backup of a container log file

```shell
sudo cp $(docker inspect --format='{{.LogPath}}' <container_name_or_id>) /path/to/backup/file.log
```
