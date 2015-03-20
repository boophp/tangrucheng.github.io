---
layout: post
title: PHP常用资源
category: 资源
tags: PHP
keywords: PHP
description: 
---

## 常用扩展

1. [phpDocumentor](http://www.phpdoc.org)
2. [PHPUnit](https://phpunit.de)
3. [Guzzle](https://github.com/guzzle/guzzle)

## 常用工具

1. [httpie](https://github.com/jakubroztocil/httpie)
2. [Postman](http://www.getpostman.com/)

## 好文

1. [PHP之道](http://laravel-china.github.io/php-the-right-way/)
2. [HTTP接口设计指北](https://github.com/bolasblack/http-api-guide)

## 其它

### 判断是否为空

```
+--------------+-----------+---------+-----------+---------+--------+
| 真值表        | gettype() | empty() | is_null() | isset() | (bool) |
+--------------+-----------+---------+-----------+---------+--------+
| $x = ""      | string    | true    | false     | true    | false  |
| $x=null      | NULL      | true    | true      | false   | false  |
| var $x       | NULL      | true    | true      | false   | false  |
| $x = array() | array     | true    | false     | true    | false  |
| $x = false   | boolean   | true    | false     | true    | false  |
| $x = 15      | integer   | false   | false     | true    | true   |
| $x = 1       | integer   | false   | false     | true    | true   |
| $x = 0       | integer   | true    | false     | true    | false  |
| $x = -1      | integer   | false   | false     | true    | true   |
| $x = '15'    | string    | false   | false     | true    | true   |
| $x = '1'     | string    | false   | false     | true    | true   |
| $x = '0'     | string    | true    | false     | true    | false  |
| $x = '-1'    | string    | false   | false     | true    | true   |
| $x = 'foo'   | string    | false   | false     | true    | true   |
| $x = 'true'  | string    | false   | false     | true    | true   |
| $x = 'false' | string    | false   | false     | true    | true   |
+--------------+-----------+---------+-----------+---------+--------+
```
