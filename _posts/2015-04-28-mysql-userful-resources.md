---
layout: post
title: MySQL常用资源
category: 资源
tags: mysql
keywords: mysql
description: 
---

## 数据库设计

### 字段类型的选择原则

列的数据类型一方面影响数据存储空间的开销，另一方面也会影响数据查询性能。当一个列可以选择多种数据类型时，应该优先考虑数字类型，其次是日期或二进制类型，最后是字符类型。对于相同级别的数据类型，应该优先选择占用空间小的数据类型。

<table>
<tr><th>列类型</th><th>存储空间</th></tr>
<tr><td>TINYINT</td><td>1字节</td></tr>
<tr><td>SMALLINT</td><td>2字节</td></tr>
<tr><td>MEDIUMINT</td><td>3字节</td></tr>
<tr><td>INT</td><td>4字节</td></tr>
<tr><td>BINGINT</td><td>8字节</td></tr>
<tr><td>DATE</td><td>3字节</td></tr>
<tr><td>DATETIME</td><td>8字节</td></tr>
<tr><td>TIMESTAMP</td><td>4字节</td></tr>
<tr><td>CHAR(M)</td><td>M字节，1 <= M <= 255</td></tr>
<tr><td>VARCHAR(M)</td><td>L+1字节，L <= M 且 1 <= M <=255</td></tr>
</table>

以上选择原则主要是从下面两个角度考虑：

1. 在对数据进行比较（查询条件、JOIN条件及排序）操作时，同样的数据，字符串处理往往比数字处理慢。

2. 在数据库中，数据处理以页为单位，列的长度越小，利于性能提升。

#### char与varchar如何选择

1. 如果列中要存储的数据长度差不多是一致的，则应该考虑用char，否则应该考虑varchar。

2. 如果列中的最大数据长度小于50Byte，则一般也考虑用char。（当然，如果这个列很少用，则基于节省空间和减少I/O的考虑，还是可以选择用varchar）

3. 一般不宜定义大于50Byte的char类型列。

mysql中utf8每个字符占用3个字节

#### decimal与float如何选择

1. decimal用于存储精确数据，而float只能用于存储非精确数据。

2. float的存储空间开销一般比decimal小（float精确到7位小数只需要4个字节，而精确到15位小数只需要8个字节）。

#### 时间类型如何存储

1. 使用int来存储时间字段的优缺点

  * 优点：字段长度比datetime小。
  
  * 缺点：使用不方便，要进行函数转换。
  
  * 限制：只能存储到2038-1-19 11:14:07 即 2^32 为 2147483648
  
2. 需要存储的时间粒度

年 月 日 时 分 秒 周

### 优化

#### 存储优化

* 永久存储（分表、分库）

* 不永久存储（归档、清理规则）