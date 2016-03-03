# Simple Interactive Wrapper of CLI with sub-commands

Nowdays, we have lots of CLI tools with many sub-commands, eg. hdfs, etcdctl...
When we use these tools continuously， we may input main-command again by again.

This little wrapper will help you to reduce that useless input.

## Usage

```bash
# install test cli(hdfs), just for example
go get github.com/colinmarc/hdfs/cmd/hdfs
# config to connect to your hadoop
export HADOOP_NAMENODE="wxnn:8020"

./interactive hdfs
```

The hdfs cli is not interactive cli tool, you need to type hdfs every time.
With this simple wrapper, you can use it like this.
```
./interactive hdfs
> ls -l /
drwxr-xr-x hbase       hbase  0 Feb 23 14:15 hbase
drwxrwxrwx  hdfs  supergroup  0 Feb 23 14:23 tmp
drwxrwxrwx  hive        hive  0 Feb 23 17:00 user
> ls -l /user
drwxr-xr-x anonymous   anonymous  0 Feb 23 17:01 anonymous
drwxrwxrwx    mapred      hadoop  0 Feb 23 10:26 history
drwxrwxrwx      hive        hive  0 Mar  1 15:58 hive
drwxrwxr-x       hue         hue  0 Feb 23 10:38 hue
drwxrwxrwx      root  supergroup  0 Feb 23 15:22 root
> quit
```

"quit" will quit the session.
