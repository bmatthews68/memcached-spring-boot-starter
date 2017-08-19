Memcached Spring Boot Starter
=============================

A convenient dependency descriptor that you can include in your [Spring
Boot](http://projects.spring.io/spring-boot/) appication to configure a
[Memcached](http://memcached.org/) client.
 
Usage
-----

```
memcached.servers=
```

```java
@SpringBootApplication
@EnableMemcached
class Application {
    .
    .
}
```

Configuration
-----
If you want to use a specific connection settings, you can define a bean for it :

```java
@SpringBootApplication
@EnableMemcached
class Application {

    @Bean
    public ConnectionFactory memcachedConnection() {
        return new ConnectionFactoryBuilder()
                    .setDaemon(true)
                    .setFailureMode(FailureMode.Cancel)
                .build();
    }

}
```


Maven Central Coordinates
-------------------------

The **Memcached Spring Boot Starter** has been published in 
[Maven Central](http://search.maven.org).

### Maven

The [Maven](http://maven.apache.org/) coordinates are:

```xml
<dependency>
  <groupId>com.btmatthews.springboot</groupId>
  <artifactId>memcached-spring-boot-starter</artifactId>
  <version>1.1.0-SNAPSHOT</version>
</dependency>
```

### Gradle

The [Gradle](http://gradle.org/) coordinates are:

```groovy
compile('com.btmatthews.springboot:memcached-spring-boot-starter:1.1.0-SNAPSHOT')
```

License & Source Code
---------------------
The **Memcached Spring Boot Starter** is made available under the 
[Apache License](http://www.apache.org/licenses/LICENSE-2.0.html)
and the source code is hosted on [GitHub](http://github.com) at 
https://github.com/bmatthews68/memcached-spring-boot-starter.