guid
======================

生成唯一id填充redis的指定key list. 使用bloomfilter做重复性判断.

命令行帮助:

```
Usage of ./guid:
Commands:
   start       - start service
   import      - import id list to bloomfilter from a file
   top         - get top 10 id in redis
   clear-redis - truncate id list in redis
   has         - test id in bloomfilter

More: guid help <command>
```

-------------------------

```
./guid start <options>
options:
  -idlen uint
    	id长度. (default 20)
  -index string
    	id唯一性校验索引文件 (default "guid.idx")
  -key string
    	redis id-key (default "guid-20")
  -password string
    	redis password
  -redis string
    	redis服务器地址 (default "127.0.0.1:6379")
```

-------------------------

```
./guid import <options>
options:
  -file string
    	导入文件
  -index string
    	id唯一性校验索引文件 (default "guid.idx")
```

-------------------------

```
./guid top <options>
options:
  -key string
    	redis id-key (default "guid-20")
  -password string
    	redis password
  -redis string
    	redis服务器地址 (default "127.0.0.1:6379")
```

-------------------------

```
./guid clear-redis <options>
options:
  -key string
    	redis id-key (default "guid-20")
  -password string
    	redis password
  -redis string
    	redis服务器地址 (default "127.0.0.1:6379")
```

-------------------------

```
./guid has <options> <test>
options:
  -index string
    	id唯一性校验索引文件 (default "guid.idx")
```
