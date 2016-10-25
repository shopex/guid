guid
======================

Generate uniq-id and RPUSH redis list, testing with bloomfilter.

Install:
---------------------

```
go install github.com/flaboy/guid
```

Commands:
---------------------

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
    	id length. (default 20)
  -index string
    	bloomfilter index file (default "guid.idx")
  -key string
    	redis id-key (default "guid-20")
  -password string
    	redis password
  -redis string
    	redis server address (default "127.0.0.1:6379")
```

-------------------------

```
./guid import <options>
options:
  -file string
    	file to import
  -index string
    	bloomfilter index file (default "guid.idx")
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
    	redis server address (default "127.0.0.1:6379")
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
    	redis server address (default "127.0.0.1:6379")
```

-------------------------

```
./guid has <options> <test>
options:
  -index string
    	bloomfilter index file (default "guid.idx")
```
