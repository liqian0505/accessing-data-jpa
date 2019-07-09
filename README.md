# accessing-data-jpa学习记录
## 看文档
* 用时约40分钟 [官方地址](https://spring.io/guides/gs/accessing-data-jpa/)
## 写代码并运行
* 用时约2小时

## 总结
* 使用H2 Database作为内嵌数据库
```
    <dependency>
            <groupId>com.h2database</groupId>
            <artifactId>h2</artifactId>
    </dependency>
```
* 用法与mongodb相似
```
public interface CustomerRepository extends CrudRepository<Customer, Long> {

    List<Customer> findByLastName(String lastName);
}
```