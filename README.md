# Utopia
使用springboot+sqlite实现CRUD练习

### 说明
为了节省配置时间，使用JPA连接Sqlite，JPA默认实现规范为Hibernate

<br>pom.xml中需要加上sqlite-jdbc的依赖，剩下的安装交给IDEA

<br>Sqlite方言写在：SQLiteDialect.java，ps.直接拿来用的

<br>运行方法：运行com.day1.springboot.Application主方法

<br>重点提一下Application.xml的配置
```
spring.mvc.view.prefix=/WEB-INF/jsp/
spring.mvc.view.suffix=.jsp
#spring.datasource.url=jdbc:mysql://127.0.0.1:8080/xxxx?characterEncoding=UTF-8
#spring.datasource.username=root
#spring.datasource.password=admin
#spring.datasource.driver-class-name=com.mysql.jdbc.Driver
#spring.jpa.properties.hibernate.hbm2ddl.auto=update

#表结构由hibernate根据实体类创建
spring.jpa.database-platform=com.day1.sqlite.SQLiteDialect
#自动根据Entity配置创建表
spring.jpa.generate-ddl=true
spring.jpa.hibernate.ddl-auto=update

#数据库文件位置
spring.datasource.url=jdbc:sqlite:how2j.db
#驱动名称
spring.datasource.driver-class-name=org.sqlite.JDBC
```


