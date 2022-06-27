使用如下三个表进行SQL语句练习。 ^d4b5bd

导入方式：[点击跳转](00-resource/建表.sql)全选复制到执行命令窗口，并执行命令。


emp表--员工信息表
![emp表](../00-resource/assets/emp表.png)
dept表--工作地点
![dept表](../00-resource/assets/dept表.png)
salgrade表--工资等级
![salgrade表](../00-resource/assets/salgrade表.png)

| 英文缩写 | 中文         | 关键字               |
| -------- | ------------ | -------------------- |
| **DQL**  | 数据查询语言 | select               |
| **DML**  | 数据操纵语言 | insert,delete,update |
| DDL      | 数据定义语言 | create,drop,alter    |
| DCL      | 数据控制语言 | grant,revoke         |
| TCL      | 事务控制语言 | commit,rollback      |

# 一、DQL

## Ⅰ.简单查询：

```sql
select ename,sal*12 '薪水' from emp;
```

## Ⅱ.条件查询：

查询job为MANAGER的员工

```sql
select ename , job from emp where job = 'manager';
```



查询薪水不等于5000的员工

```sql
select ename , sal from emp where sal <>5000;
```



查询薪水为1600到3000的员工

左闭右闭

```sql
select ename , sal from emp where sal between 1600 and 3000;
```



查询津贴为空/不为空的员工

```sql
select * from emp where comm is null;
select * from emp where comm is not null;
```



查询工作为manager并且工资等于2450或等于3500的信息

```sql
select * from emp where job='MANAGER' and (sal = 2975 or sal=2450);
select * from emp where job = 'MANAGER' and (sal in (2975,2450));
```

查询工作为manager或工资大于2500的信息

```sql
select * from emp where job='MANAGER' or job='SALESMAN';
select * from emp where job in('MANAGER','SALESMAN');
```



查询姓名以M开头所有的员工

```sql
select * from emp where ename like 'M%';
```

查询姓名中包含O的所有的员工

```SQL
select * from emp where ename like '%O%';
```

查询姓名中第二个字符为A的所有员工

```SQL
select * from emp where ename like '_A%';
```



## Ⅲ. 排序查询：

根据工资正/倒排DEPTNO=20的用户

```sql
select * from emp where deptno = 20 order by sal;
select * from emp where deptno = 20 order by sal desc;
```

现根据薪资倒排再根据生日正排

```sql
select * from emp order by sal desc , hiredate;
```



## Ⅳ.分组函数

又名：聚合函数/多行处理函数

分组函数自动忽视空值

分组函数不能直接使用在where关键字后面。

|       |          |
| ----- | -------- |
| count | 返回数字 |
| sum   | 求和     |
| avg   | 求平均   |
| max   | 求最大数 |
| min   | 求最小数 |



查询COMM不为null的数据条数

```sql
select count(comm) from emp;
```

去重 查询工作种类

```sql
select count(distinct job) from emp;
```

取得薪水的合计（sal+comm）

因为comm字段有null 而分组函数会屏蔽null，则comm不会参与运算，需要ifnull操作。

```sql
select ename,sum(sal+ifnull(comm,0)) from emp;
```

取得平均薪水

```sql
select avg(sal) from emp;
```

取得最高薪水

```sql
select max(sal) from emp;
```

取得最晚入职得员工

```sql
select max(str_to_date (hiredate, '%Y-%m-%d')) from emp;
```



## Ⅴ. 分组查询

