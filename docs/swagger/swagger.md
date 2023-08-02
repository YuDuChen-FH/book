springboot整合swagger3.0

1.引入依赖

```xml
<dependency>
  <groupId>io.springfox</groupId>
  <artifactId>springfox-boot-starter</artifactId>
  <version>3.0.0</version>
</dependency>
```

2.启动类开启@EnableWebMvc注解

3.创建config配置文件

```java
@EnableOpenApi
@Configuration
public class SwaggerConfig {

}
```

4.访问路径:ip:port/swagger-ui/index.html



如果启动报错

```java
Type javax.servlet.http.HttpServletRequest not present
```

将springboot的版本改为2.7.8即可