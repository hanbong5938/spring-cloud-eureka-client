# spring-cloud-eureka-client


### gradle 의존성
```
    implementation("org.springframework.boot:spring-boot-starter-web")
    // https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-actuator
    implementation("org.springframework.boot:spring-boot-actuator:2.6.1")
    // https://mvnrepository.com/artifact/org.springframework.cloud/spring-cloud-starter-netflix-eureka-client
    implementation("org.springframework.cloud:spring-cloud-starter-netflix-eureka-client:3.1.0")
```

### yml
```
server:
  port: 10000

spring:
  application:
    name: msa

eureka:
  client:
    service-url:
      defaultZone: http://localhost:9999/eureka/
    register-with-eureka: true
    fetch-registry: true

```

### 어노테이션
메인클래스 위에
```
@EnableEurekaClient
```
