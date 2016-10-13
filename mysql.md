登录mysql
mysql -h 127.0.0.1 -u 用户名 -p
mysql -D 所选择的数据库名 -h 主机名 -u 用户名 -p
mysql> exit #退出
mysql> quit #退出

数据库定义语言
show databases;
CREATE DATABASE test;
use test;
select DATABASE();
drop databases if exists test;

创建数据库表
create table 表名称(列声明)

## COUNT 让我们能够数出在表格中有多少笔资料被选出来。 
语法：SELECT COUNT("字段名") FROM "表格名";

CREATE TABLE `user_accounts` (
  `id`             int(100) unsigned NOT NULL AUTO_INCREMENT primary key,
  `password`       varchar(32)       NOT NULL DEFAULT '' COMMENT '用户密码',
  `reset_password` tinyint(32)       NOT NULL DEFAULT 0 COMMENT '用户类型：0－不需要重置密码；1-需要重置密码',
  `mobile`         varchar(20)       NOT NULL DEFAULT '' COMMENT '手机',
  `create_at`      timestamp(6)      NOT NULL DEFAULT CURRENT_TIMESTAMP(6),
  `update_at`      timestamp(6)      NOT NULL DEFAULT CURRENT_TIMESTAMP(6) ON UPDATE CURRENT_TIMESTAMP(6),
  -- 创建唯一索引，不允许重复
  UNIQUE INDEX idx_user_mobile(`mobile`)
)
ENGINE=InnoDB DEFAULT CHARSET=utf8
COMMENT='用户表信息';
增删改查
SELECT 语句用于从表中选取数据。 
语法：SELECT 列名称 FROM 表名称 
语法：SELECT * FROM 表名称

Update 语句用于修改表中的数据。 
语法：UPDATE 表名称 SET 列名称 = 新值 WHERE 列名称 = 某值

INSERT INTO 语句用于向表格中插入新的行。 
语法：INSERT INTO 表名称 VALUES (值1, 值2,....) 
语法：INSERT INTO 表名称 (列1, 列2,...) VALUES (值1, 值2,....)

DELETE FROM 表名称 WHERE 列名称 = 值

ALTER TABLE 表名字 ADD INDEX 索引名字 ( 字段名字 )

-- –直接创建索引
CREATE INDEX index_user ON user(title)
-- –修改表结构的方式添加索引
ALTER TABLE table_name ADD INDEX index_name ON (column(length))
-- 给 user 表中的 name字段 添加普通索引(INDEX)
ALTER TABLE `table` ADD INDEX index_name (name)
-- –创建表的时候同时创建索引
CREATE TABLE `table` (
    `id` int(11) NOT NULL AUTO_INCREMENT ,
    `title` char(255) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL ,
    `content` text CHARACTER SET utf8 COLLATE utf8_general_ci NULL ,
    `time` int(10) NULL DEFAULT NULL ,
    PRIMARY KEY (`id`),
    INDEX index_name (title(length))
)
-- –删除索引
DROP INDEX index_name ON table

普通索引
语法：ALTER TABLE 表名字 ADD INDEX 索引名字 ( 字段名字 )
主键索引 
ALTER TABLE 表名字 ADD PRIMARY KEY ( 字段名字 )
唯一索引
ALTER TABLE 表名字 ADD UNIQUE (字段名字)
全文索引
ALTER TABLE 表名字 ADD FULLTEXT (字段名字)
添加多列索引
ALTER TABLE table_name ADD INDEX index_name ( column1, column2, column3)
建立索引的时机
在WHERE和JOIN中出现的列需要建立索引，但也不完全如此：

* MySQL只对<，<=，=，>，>=，BETWEEN，IN使用索引
* 某些时候的LIKE也会使用索引。
* 在LIKE以通配符%和_开头作查询时，MySQL不会使用索引。
索引的注意事项
    索引不会包含有NULL值得列
    使用短索引
    不要在列上进行运算 索引会失效
创建后表的修改
添加列
alter table 表名 add 列名 列数据类型 [after 插入位置];
修改列
alter table 表名 change 列名称 列新名称 新数据类型;
删除列
alter table 表名 drop 列名称;
重命名表
alter table 表名 rename 新表名;
清空表数据
方法一：delete from 表名;
方法二：truncate from "表名";
DELETE:1. DML语言;2. 可以回退;3. 可以有条件的删除;
TRUNCATE:1. DDL语言;2. 无法回退;3. 默认所有的表内容都删除;4. 删除速度比delete快。
删除整张表
-- 删除 workmates 表: 
drop table workmates
删除整个数据库
语法：drop database 数据库名;

tinyint:127 to -128
smallint:32768 to -32767
medium int: 8388608 to -8388608
int: 2^31 to -2^31-1

char:character string with a fixed length
varchar:a character string with a length that's variable
blob: can contain 2^16 bytes of data
bigint:2^63 to -2^63-1
float:decimal spaces,1.1E38 to -1.1E38
DOUBLE:decimal spaces,1.7E308 to -1.7E308

ENUM:a character string that has a limited number of total values,which you must define.
set:alist of legal possible character strings. Unlike ENUM,a set can contain multiple values in
    comparision to the the one legal value with ENUM.

describe tb_admin;

insert 
select 
alter table test add column maxscore int not null after 列
                modify column maxscore

abs()
degrees()
mod()
sqrt()
acos(),asin(),atan(),atan2(),cos(),sin(),tan()
avg()
ceiling()
count()
exp()
floor()
log()
max()
min()
PI()
power()
padians()
rand()
round()
std()
sum()
truncate




installing and upgrading mysql
mysql programs
mysql server administration
security
backup and recovery
optimization
language structure
globalization
data types
functions and operators
sql statement syntax
the innoDB storage engine
hign availability and scalability
replication
mysql cluster
partitioning
stored programs and views
information_schema tables
mysql performance schema
connectors and apis
restrictions and limits
indexes
Errors,Error Codes,and Common Problems


