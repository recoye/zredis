# zredis
redis extension for php7

[![Build Status](https://secure.travis-ci.org/recoye/zredis.svg?branch=master)](http://travis-ci.org/recoye/zredis)

# checkout source
~~~
git clone --recursive https://github.com/recoye/zredis
~~~

or 

~~~
git clone https://github.com/recoye/zredis
git submodule update --init
~~~
# compile && install
~~~

  phpize
  
  ./configure
  
  make
  
  make install
  
  enable zrediso.so in php.ini(extension=zredis.so)
  ~~~
  
#demo
  ```php
    $redis = new zredis();
    $redis->connect();    //tcp， 127.0.0.1:6379
    //$redis->connect('/tmp/redis.sock');  //unix socket
    //$redis->connect('127.0.0.1', 6379, 3); //args: ip, prot, timeout
    //$redis->pconnect();    // persistent connection,default: 127.0.0.1:6379
    //$redis->pconnect('/tmp/redis.sock');  //unix sockett, persistent connection,
    //$redis->pconnect('127.0.0.1', 6379, 3); //persistent connection, args:ip, port, timeout
    $redis->set("key", $val);  //command：http://redis.io/commands
    echo $redis->get("key");
    $redis->close();   //close
  ```
  
  
#鸣谢：
  0) hiredis c client lib  （官方提供的c client库）
  
  1) Adam （在他的工作基础上进行完善） 
  
  
  
