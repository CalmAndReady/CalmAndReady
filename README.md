- 👋 Hi, I’m @CalmAndReady
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
CalmAndReady/CalmAndReady is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
# 一、MySql服务器数据库服务器介绍：

1.MySql服务器来自于甲骨文公司
2.MySql服务器可以操作【表文件】，帮助用户进行远程的【数据服务】
3.MySql服务器目前是国内使用频率最高的数据库服务器

# 二、MySql服务器内部结构

1.表文件:
1)表文件以".frm"结尾文件
2)表文件用来存储数据。以行为单位存储数据
3)表文件包含一个标题行，描述数据行特征
4)表文件包含若干个数据行，描述具体信息

2.数据库: 
1)英文称为DataBase
2)专门存放表文件的文件夹

# 三、MySQL服务器安装位置信息

如果安装路径没有更改
1.MySql服务器安装位置: C:\\Program Files (x86)\\MySQL\\MySQL Server 5.5
2.MySql服务器管理的数据库存放位置：C:\\ProgramData\\MySQL\MySQL Server 5.5\\data
3.MySql服务器核心配置文件位置：C:\\Program Files (x86)\\MySQL\\MySQL Server 5.5\\my.ini

# 四、MySql服务器配置

1.MySql服务器中管理命令位置: C:\\Program Files (x86)\\MySQL\\MySQL Server 5.5\\bin
2.配置：为了能够在windows系统中正确使用MySql服务器中管理命令来操作MySql服务器所以必须将MySql服务器中管理命令的存储地址交给windows中path环境变量

1.SQL编程语言帮助开发人员与数据库服务器进行沟通
2.SQL编程语言全称 Struct Query Language, 结构化查询语言
3.SQL编程语言分类:
1) [[#一、DDL|DDL]]:DataBase  Defined  Language,数据库定义语言/数据库维护命令
2) DML:Data Modify Language，       数据行维护命令（insert/update/delete）
3) DQL:Data Query  Language,           数据行查询命令

# 五、DDL（非重点）

可以使用图形化工具快速部署。
作用:
1.通知MySql服务器管理【数据库】
2.通知MySql服务器管理【数据库中表文件】
3.通知MySql服务器管理【数据库中表文标题行】

## Ⅰ 通知MySql服务器管理【数据库】

1.询问MySql服务器,其管理的数据库名称

```SQL
mysql> show databases;
```

2.要求MySql服务器新建一个数据库

```SQL
mysql> create database 数据名;#数据库名不能用中文命名
```

3.要求MySql服务器删除指定数据库

```sql
mysql> drop database 数据库名;
```

![[DDL-01.png]]



## Ⅱ 通知MySql服务器管理【数据库中表文件】

1)要求MySql服务器展示某个数据库下所有表文件名称

```SQL
mysql> use 数据库名; # 接下来操作针对哪一个数据库进行操作
```

2)要求MySql服务器在指定的数据库下创建表文件

```sql
create table  表文件名(
字段名  数据类型,
字段名  数据类型
);
```

3.要求MySql服务器对指定数据库下表文件删除

```sql
mysql> drop table 表名;
```

![[DDL-02.png]]

## Ⅲ 通知MySql服务器管理【数据库中表文件标题行】

1.要求MySql服务器将指定表文件结构信息展示

```sql
mysql> show create table 表名;
```

2.要求MySql服务器为指定的表文件增加新字段

```java
mysql> alter table 表名  add   新增字段名  数据类型;
```

![[DDL-03.png]]
3.要求MySql服务器为指定表文件中的字段删除

```sql
mysql> alter table 表名 drop 字段名;
```

# 六、DML

1.作用: 要求MySql服务器对表文件中数据行进行维护
2.分类:
insert命令：要求MySql服务器对表文件进行数据行新增

update命令: 要求MySql服务器对表文件中数据行内容进行更新

delete命令: 要求MySql服务器对表文件中数据行进行删除
