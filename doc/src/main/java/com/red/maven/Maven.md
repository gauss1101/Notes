# Maven学习笔记

## IDEA中使用Maven

### IDEA集成Maven插件

### 使用IDEA创建Maven工程

#### 使用骨架创建

#### 不使用骨架创建

#### 创建maven的web工程

### Demo

servlet跳转jsp

```
req.getRequestDispatcher("/hello.jsp").forward(req,resp);
```

web.xml配置servlet mapping

```java
tomcat7插件	
<plugin>
          <groupId>org.apache.tomcat.maven</groupId>
          <artifactId>tomcat7-maven-plugin</artifactId>
          <version>2.2</version>
          <configuration>
            <port>8888</port>
          </configuration>
        </plugin>
        
servlet依赖          
    <dependency>
      <groupId>javax.servlet</groupId>
      <artifactId>servlet-api</artifactId>
      <version>2.5</version>
      <scope>provided</scope>
    </dependency>
    <dependency>
      <groupId>javax.servlet.jsp</groupId>
      <artifactId>jsp-api</artifactId>
      <version>2.0</version>
      <scope>provided</scope>
    </dependency>
```

配置了<pluginManagement></pluginManagement>标签,会导致右侧显示不了tomcat7插件

## Pom文件