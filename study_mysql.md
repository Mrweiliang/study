#### 通过sql语句删除重复行
平时在使用mysql难免会插入重复内容,之前一直使用python脚本删除,耗时长,删除100w条数据中的重复行,往往需要很长时间,今天突然看到网上的案例,用起来快!
使用案例
```
delete t1 from book_data t1 inner join book_data t2 where t1.id<t2.id and t1.chapter_id = t2.chapter_id;
```
参数详解:
delete t1 from 表名 t1 inner join 表名 t2 where t1.id<t2.id and t1.重复字段=t2.重复字段;

