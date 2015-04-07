#SRedis插件
依赖phpredis扩展 https://github.com/nicolasff/phpredis/

# 主要特性 #


# 使用方法 #

```
//初始化对像
$s = new SRedis;

//设置配置文件地址
$s->setConfigFile("../samples/config/redis.ini");

//设置配置文件节点
$s->useConfig("default");

//掉用Redis类的方法，详细 https://github.com/ukko/phpredis-phpdoc/blob/master/src/Redis.php
var_dump($s->set("D","ww"));
var_dump($s->get("D"));
var_dump($s->zAdd('k1', 0, 'val0'));
var_dump($s->zAdd('k1', 1, 'val1'));


```

# 配置文件 #
  * 配置文件模板样例
```conf

#配置一共有2个字段
#host 主机IP，或者主机名
#port 端口号
#default 是默认的配置，可以配置1到多个

#default
default{ host localhost; port 6379; }
default{ host localhost; port 6380; }

#user
default{ host localhost; port 6381; }
default{ host localhost; port 6382; }


```